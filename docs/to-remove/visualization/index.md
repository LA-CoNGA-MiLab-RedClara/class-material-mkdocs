<style>
img {
  float: left;
}
</style>

# Módulo 1:
## Instructor: Homero Martinez
<p>
  <img src="../profile-photo/homero-martinez.jpg" alt="Homero-Martinez" style="width:50%;margin-right:15px;">
  License in Physics, Universidad de Los Andes, Merida-Venezuela (2008). High Energy Physics LatinAmerican-European Network (HELEN) fellow (2006-2007).Electric engineering degree, Universidad de Los Andes, Merida-Venezuela (2009). PhD in particle physics, University Paris Diderot (Paris 7), France (2013).  Post-doc researcher at University of Pavia-INFN, Italy (2013-2016) for the ATLAS experiment. Software Engineer in Alstom, Paris, France (2017-present).
</p>

## Clase
This is the C++ analysis code that may be used to analyse the data of the ATLAS published dataset.
<!--
<iframe width="100%" height="420" src="https://www.youtube.com/embed/LiEaDU-OG1M?start=2186?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" rel="0" allowfullscreen></iframe>
-->

<iframe src="https://drive.google.com/file/d/0ByCHs8gf0A9sWHlmRmxQSmFqT1E/preview" width="100%" height="570" frameBorder="0"></iframe>

More information in the 8 TeV ATLAS Open Data PUB notes:

<video width="100%" controls>
 <source src="../videos/Clase_0-modulo_1-IFP-CEVALE2VE-2018.mp4" type="video/mp4">
<!-- <source src="../videos//opendata-demo-26F-2020.mov" type="video/mp4"> -->
 Your browser does not support the video tag.
</video>

<iframe src="../PDFs/IFP_modulo1_clase1_HomeroM_v3_sinpausas.pdf" width="100%" height="480" frameborder="0"></iframe>


<iframe src="https://nbviewer.jupyter.org/github/atlas-outreach-data-tools/notebooks-collection-opendata/blob/master/13-TeV-examples/python/ATLAS_OpenData_13-TeV_simple_python_example_histogram.ipynb" width="100%" height="4000" frameborder="0" allowfullscreen></iframe>


* https://cds.cern.ch/record/2203649/files/ATL-OREACH-PUB-2016-001.pdf
* https://cds.cern.ch/record/2624572/files/ATL-OREACH-PUB-2018-001.pdf

This code is made of two parts of codes: analysis codes and plotting codes.

## **GitLab repository**
* [atlas-outreach-cpp-framework-13tev](https://gitlab.cern.ch/lserkin/atlas-outreach-cpp-framework-13tev)

* ```git clone https://gitlab.cern.ch/lserkin/atlas-outreach-cpp-framework-13tev.git ```

## **Setup**
After checking out the repository, you need to setup ROOT framework and gcc compiler. The current version was compiled using gcc v6.20 and root v6.10.04

## **Samples**
For now, the analysis code can be run using samples located in eos:
```
/eos/project/a/atlas-outreach/projects/open-data/OpenDataTuples/
```

## **Analysis Code**
The analysis code is located in the **Analysis** folder. It will be used to write out histograms for the individual input files which will be used for plotting purposes later.

There are currently 7 available analyses stored as "```NNAnalysis```", where ```NN = WBoson, ZBoson, TTbar, WZDiBoson, ZZDiBoson, HWW, ZPrime```

Each analysis code contains
- the analysis header (```NNAnalysis.h```) which defines the histograms and gives access to the variables stored in the input samples
- the histogram header (```NNAnalysisHistograms.h```) which defines the name of output histograms
- the analysis code (```NNAnalysis.C```) which makes all the selection and stores the output histograms
- the analysis main (```main_NNAnalysis.C```) controls which samples are being used
- the output directory (```Output_NNAnalysis```) is where the output histograms (one per each input sample) will be stored

First setup the code using:
* ```./welcome.sh```
or
* ```source welcome.sh```


To run the code:
* ```./run.sh```
or
* ```source run.sh```

Shared libraries will be created and the analysis will run over each input sample.
Estimated time it takes to run an analysis code: **15 seconds per 1M events**

To clean all shared libraries:
* ```./clean.sh```
or
* ```source clean.sh```

## **Plotting**
The plotting code is located in the **Plotting** folder.
* Compile the plotting code with the command: ```make```

- Run the code with:
```
./plot [WBosonAnalysis, ZBosonAnalysis, TTbarAnalysis, DiBosonAnalysis, HWWAnalysis, ZPrimeAnalysis]  [location of OutputDir_AnalysisName]
```

Here you have to choose
* 1.) which analysis you will run
* 2.) where is the output of the analysis code you produced

**Examples**

```./plot ZBosonAnalysis ../Analysis/ZBosonAnalysis/OutputDir_ZBosonAnalysis```

- The plots are saved inside the directory "**histograms**", don't forget to rename in case you run over several analyses

- Which histograms are being produced? This is controlled by the input file "*HistoList_ANALYSISNAME.txt*" inside *list_histos*

- Do you want to add a new plot? just add the name of it in this file (of course it has to exist in the output from the analysis code)

- In case you changed the ```Plotting``` code, clean first: ```make clean; make```

- Auxiliary: ```Files.txt``` contains the name, cross-section, sum of weights and efficiency for each of the MC samples. **DO NOT CHANGE**

## **How to add a new variable and plot it**
1. Add in the header (```NNAnalysis.h```) the new histogram:
```
TH1F *h_new = 0;
```

2. Add in the main analysis code (*NNAnalysis.C*) the calculation of the new variable:
```
float new_variable = jet_n;
```

3. Add in *NNAnalysisHistograms.h*
- in define_histograms():
```
  h_new = new TH1F("h_new", "Description of the new variable; X axis name ; Y axis name ", number of bins , min bin , max bin);
```

- in FillOutputList()
```
  GetOutputList()->Add(h_new);
```

- in WriteHistograms()
```
  h_new->Write();
```

- in FillHistograms()
```
  if (s.Contains("h_new")) h_new->Fill(m,w);
```

4. Now finally add in ```NNAnalysis.C``` the connection between the new variable and the new histogram
```
FillHistograms( new_variable, weight, "h_new");
```
where "new_variable" is the new variable you calculated in 2.

5. now run the code again over all the samples

6. Go to ```PlottingCode/list_histos```
- in ```HistoList_NNAnalysis.txt``` add one new line:
```
  h_new
```

7. run the plotting code and you will find the new histogram in ```histograms/h_new.png```!
