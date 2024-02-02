# Emotions in Drama

This is a GitHub-repository for the research project <a href="https://dfg-spp-cls.github.io/projects_en/2020/01/24/TP-Emotions_in_Drama/">Emotions in Drama</a> (EmoDrama).

The repository is used to store data and other material that was created during the project and meant to be published or serves as additional material for papers.

Please refer to the reference section for information about all publications and scientific contributions. 

Some general information about the repository:
<ul>
  <li>All data larger than 100 MB is either zipped or linked via Google Drive or Seafile.</li>
  <li>English/German-translation information can be found <a href="https://github.com/lauchblatt/Emotions_in_Drama/blob/main/Annotations/emodrama_translation_set.pdf">here</a>.</li>
  <li>Some vocabulary in naming conventions of data may differ from the papers: tag_type = sub-emotions, base_polarity = (positive, negative, being moved, eventually no annotation), polarity = (only positive/negative)</li>
  <li>Despite great care, errors in the data or folder structure can always occur. If you think you noticed a problem, feel free to reach out: thomas.schmidt@ur.de</li>
</ul>

The main components of this repository are described as follows:

## Annotations

The annotation folder contains the final annotations of 18 plays according to our guidelines <a href="https://doi.org/10.5281/zenodo.6228152
">(Dennerlein, Schmidt & Wolff, 2022c)</a> and has the following structure:
<ul>
  <li><b>Emotions</b>: Emotion annotations for 18 plays including implicit source/target annotations.</li>
  <ul>
    <li><b>Raw_Emotion_Annotations</b>: Unfiltered (raw) emotion annotations by two annotators each.</li>
    <li><b>Filtered_Emotion_Annotations_withNoAnnotation</b>: Emotion annotations filterd by disagreements and including the no annotation class (non-annotated material).
    These are the annotations used to train the final classification model.</li>
   </ul>
    <li><b>Source_Target</b>: Implicit and explicit source/target annotations for 18 plays and for all plays summed up.</li>
  </ul>
  Some information regarding the annotations:
    <ul>
      <li>Please refer to <a href="https://doi.org/10.5281/zenodo.6228152">Dennerlein, Schmidt and Wolff (2022c)</a>, <a href="https://doi.org/10.17175/2023_010">Dennerlein, Schmidt and Wolff (2023b)</a> and <a href="https://doi.org/10.1093/llc/fqad046">Dennerlein, Schmidt and Wolff (2023a)</a> for explanations of annotation data, processes and German/English translations.</li>
      <li>Main annotation attributes are: tag_type (sub-emotions), main_emotion_class, base_polarity (positive, negative, being moved, eventually no annotation)</li>
      <li>Annotations of different annotators are seperable via the annotator attribute and consist of 2-letter-abbreviations (e.g. VH, LS)</li>
      <li>The annotations were performed under guidance (technical issues: Thomas Schmidt, history of drama: Katrin Dennerlein) by the following students: Carlina Eizenberger, Viola Hippler, Nadine Kastenhofer, Julia Jäger, Emma Russ, Leon Sautter, Lisa Schattmann.</li>
    </ul>

## Classification_Model
This folder contains a link to the transformer-based large language model used in <a href="https://doi.org/10.1093/llc/fqad046">Dennerlein, Schmidt and Wolff (2023a)</a> and Dennerlein, Schmidt and Wolff (2024) as well as evaluation information. This model (based on gbert-large by <a href="https://www.deepset.ai/">deepset</a>t) achieves am average F1-score for sub-emotion classification of 72% and was fine-tuned for four epochs with a batch size of 32, a learning rate of 4e-5, and the Adam optimizer, utilizing a Tesla P100 GPU with the filtered annotations. 

Please refer to the <a href="https://huggingface.co/">hugging face library</a> on how to use the unzipped model and the models in this repository in general. We also included a link to a <a href="https://colab.research.google.com/drive/1c8so9bADbwluPC4M1bT351L5qpRCHp--?usp=sharing">google colab</a> for a basic usage example in this folder.

## Classification_Results

This folder contains the results of the application of the classification model on the sentences of 313 plays. Subsets of these results are used in <a href="https://doi.org/10.1093/llc/fqad046">Dennerlein, Schmidt and Wolff (2023a)</a> and Dennerlein, Schmidt and Wolff (2024). The original plays are from <a href="https://dracor.org/ger">GerDracor</a>, <a href="https://textgrid.de/">TextGrid</a> or based on our own work.

Some information regarding the classification results:
<ul>
  <li>To get the concrete corpora used in papers please refer to the <b>Additional_Data_Per_Paper</b> section.</li>
  <li>Main annotation attributes are: pre1_tag_type (sub-emotions), pre1_main_emotion_class (main emotion class), pre1_base_polarity (positive, negative, being moved, eventually no annotation).</li>
  <li>The type attribute differs between character speeches (spoken text) and stage directions (Dennerlein, Schmidt & Wolff, 2024)</a></li>
  <li>Additional metadata is derived from the data in the <b>Metadata</b> folder.</li>
  <li>Only plays of the GerDracor corpus contain consistent gender information and character ids.</li>
</ul>

## Metadata

Metadata about the plays used for the classification process. Plays can be identified via the file attribute. The metadata was acquired during the corpus preparation process of the project.

Some information regarding the metadata:
<ul>
  <li>The correct publication year (as used for Dennerlein, Schmidt & Wolff, 2024) is stored in the "Sortierdatum"-attribute. Other year attributes offer additional information.</li>
  <li>Genre is stored in "genre classification": S=Schauspiel, T=Tragedy, K=Comedy. Via the subgenre attribute, satirical typecomedies ("Sächsische Typenkomödien") are marked as they are used in <a href="https://doi.org/10.1093/llc/fqad046">Dennerlein, Schmidt and Wolff (2023a)</a>.</li>
</ul>

## Additional_Data_Per_Paper

This folder contains additional data seperated by papers and publications:
<ul>
  <li><b>2021_vDHd_Using_Deep_Learning_For_Emotion_Analysis</b>: Evaluation results, models and further data for <a href="https://doi.org/10.26298/melusina.8f8w-y749-udlf ">Schmidt, Dennerlein and Wolff (2021c)</a>.</li>
  <li><b>2021_LDK_Towards_A_Corpus_Historical_German_Plays_With_Emotion_Annotations</b>: All relevant data for <a href="https://doi.org/10.4230/OASIcs.LDK.2021.9">Schmidt, Dennerlein and Wolff (2021b)</a> can be found in the <b>Annotations</b>-folder in the main branch.</li>
  <li><b>2021_LaTeCHCLfL_Emotion_Classification_In_German_Plays</b>: Evaluation results, models, and further data for <a href="https://doi.org/10.18653/v1/2021.latechclfl-1.8">Schmidt, Dennerlein and Wolff (2021a)</a>.</li>
  <li><b>2022_DHd_Emotionen_Im_Kulturellen_Gedaechtnis_bewahren</b>: Additional annotation trend results (tables and visualizations) for <a href="https://doi.org/10.5281/zenodo.6327957">Dennerlein, Schmidt and Wolff (2022b)</a>. </li>
  <li><b>2022_DHd_Evaluation_Computergestuetzter_Verfahren_der_Emotionsklassifikation</b>: Additional data (evaluation results, models etc.) for <a href="https://doi.org/10.5281/zenodo.6328169">Schmidt, Dennerlein and Wolff (2022)</a> can be found in the folder <b>2021_vDHd_Using_Deep_Learning_For_Emotion_Analysis</b>.</li>
  <li><b>2022_DH_Emotion_Courses_In_German_Historical_Comedies_And_Tragedies</b>: Additional material including annotation and classification trend results (tables and visualizations), models, distribution data, graphs, and classification results for <a href="https://dh-abstracts.library.cmu.edu/works/11929">Dennerlein, Schmidt and Wolff (2022a)</a></li>
  <li><b>2023_DH_Results_Of_Emotion_Annotation</b>: All relevant data for <a href="https://doi.org/10.5281/ZENODO.8107952">Schmidt, Dennerlein and Wolff (2023)</a> can be found in the <b>Annotations</b>-folder in the main branch.</li>
  <li><b>2023_DSH_Computational_Emotion_Classification_For_Genre_Corpora</b>: All additional material for <a href="https://doi.org/10.1093/llc/fqad046">Dennerlein, Schmidt and Wolff (2023a)</a> including distribution analysis, visualizations, and classification results. The model used in this study can be found in the <b>Classification_Model</b> folder of the main branch.</li>
  <li><b>2023_ZfdG_EmoDrama_Ein_Korpus_mit_Emotionsinformationen</b>: All relevant data for <a href="https://doi.org/10.5281/ZENODO.8107952">Dennerlein, Schmidt and Wolff (2023b)</a> can be found in the <b>Annotations</b>-folder in the main branch.</li>
  <li><b>2024_CDA_Emotions_in_Stage_Directions</b>: All additional material for Dennerlein, Schmidt and Wolff (2024) including distribution tables, visualizations, classification results, and word frequency data like word clouds. Please note that data regarding stage directions uses the abbreviation _stages and character speeches (spoken text) cp. The model used in this study can be found in the <b>Classification_Model</b> folder of the main branch. </li>
</ul>

## CLS_Meetings
In this folder, you can find all presentation slides that were used for meetings of the <a href="https://dfg-spp-cls.github.io/">priority program computational literary studies</a> including meetings of the working group annotation and sentiment analysis.

## Publications

Brandes, Ph., Dennerlein, K., Jacke, J., Marshall, S., Pielström, St., Schneider, F. (2022). Modelling and Operationalizing Concepts in Computational Literary Studies. In DH2022 Local Organizing Committee (Ed.), Responding to Asian Diversity. Digital Humanities 2022 Conference Abstracts. (pp. 70–73). Alliance of Digital Humanities Organizations (ADHO). https://dh-abstracts.library.virginia.edu/works/11818 

Dennerlein, K., Schmidt, T., & Wolff, C. (2022a). Emotion courses in German historical comedies and tragedies. In DH2022 Local Organizing Committee (Ed.), Responding to Asian Diversity. Digital Humanities 2022 Conference Abstracts. (pp. 193–197). Alliance of Digital Humanities Organizations (ADHO). https://dh-abstracts.library.cmu.edu/works/11929 

Dennerlein, K., Schmidt, T., & Wolff, C. (2022b). Emotionen im kulturellen Gedächtnis bewahren. In M. Geierhos, P. Trilcke, I. Börner, S. Seifert, A. Busch, & P. Helling (Eds.), DHd 2022 Kulturen des digitalen Gedächtnisses. 8. Tagung des Verbands “Digital Humanities im deutschsprachigen Raum” (DHd 2022) (pp. 93–98). Zenodo. https://doi.org/10.5281/zenodo.6327957 

Dennerlein, K., Schmidt, T., & Wolff, C. (2023a). Computational emotion classification for genre corpora of German tragedies and comedies from 17th to early 19th century. Digital Scholarship in the Humanities, 38(4), 1466–1481. https://doi.org/10.1093/llc/fqad046 

Dennerlein, K., Schmidt, T., & Wolff, C. (2023b). EmoDrama. Ein Korpus mit Emotionsinformationen in Dramen von 1650-1815. Zeitschrift für digitale Geisteswissenschaften (ZfdG). https://doi.org/10.17175/2023_010 

Dennerlein, K., Schmidt, T., & Wolff, C. (2024; In publication). Emotions in Stage Directions in German Drama of the Early Modern Period: Explorations via Computational Emotion Classification. In M. Andresen & N. Reiter (Eds.), Computational Drama Analysis. Reflecting Methods and Interpretation. (pp. 166–194). De Gruyter.

Schmidt, T., Dennerlein, K., & Wolff, C. (2021a). Emotion Classification in German Plays with Transformer-based Language Models Pretrained on Historical and Contemporary Language. In S. Degaetano-Ortlieb, A. Kazantseva, N. Reiter, & S. Szpakowicz (Eds.), Proceedings of the 5th Joint SIGHUM Workshop on Computational Linguistics for Cultural Heritage, Social Sciences, Humanities and Literature (pp. 67–79). Association for Computational Linguistics. https://doi.org/10.18653/v1/2021.latechclfl-1.8 

Schmidt, T., Dennerlein, K., & Wolff, C. (2021b). Towards a Corpus of Historical German Plays with Emotion Annotations. In D. Gromann, G. Sérasset, T. Declerck, J. P. McCrae, J. Gracia, J. Bosque-Gil, F. Bobillo, & B. Heinisch (Eds.), 3rd Conference on Language, Data and Knowledge (LDK 2021) (Vol. 93, p. 9:1-9:11). Schloss Dagstuhl – Leibniz-Zentrum für Informatik. https://doi.org/10.4230/OASIcs.LDK.2021.9 

Schmidt, T., Dennerlein, K., & Wolff, C. (2021c). Using Deep Learning for Emotion Analysis of 18th and 19th Century German Plays. In M. Burghardt, L. Dieckmann, T. Steyer, P. Trilcke, N.-O. Walkowski, J. Weis, & U. Wuttke (Eds.), Fabrikation von Erkenntnis: Experimente in den Digital Humanities. Teilband 1. Melusina Press. https://doi.org/10.26298/melusina.8f8w-y749-udlf 

Schmidt, T., Dennerlein, K., & Wolff, C. (2022). Evaluation computergestützter Verfahren der Emotionsklassifikation für deutschsprachige Dramen um 1800. In M. Geierhos, P. Trilcke, I. Börner, S. Seifert, A. Busch, & P. Helling (Eds.), DHd 2022 Kulturen des digitalen Gedächtnisses. 8. Tagung des Verbands “Digital Humanities im deutschsprachigen Raum” (DHd 2022) (pp. 107–113). Zenodo. https://doi.org/10.5281/zenodo.6328169 

Schmidt, T., Dennerlein, K., & Wolff, C. (2023). Results of Emotion Annotation in German Drama from 1650-1815. In A. Baillot, T. Tasovac, W. Scholger, & G. Vogeler (Eds.), Digital Humanities 2023. Collaboration as Opportunity (DH2023) (pp. 181–183). Alliance of Digital Humanities Organizations (ADHO). https://doi.org/10.5281/ZENODO.8107952

## Annotation Guidelines

Dennerlein, K., Schmidt, T., & Wolff, C. (2022c). Figurenemotionen in deutschsprachigen Dramen annotieren. Zenodo. https://doi.org/10.5281/zenodo.6228152

## Presentations

Dennerlein, K. (2021). Emotion und Gattung. Zur Analyse von Dramen um 1800. Göttingen, Germany. (Presentation at the University Göttingen).

Dennerlein, K. & Schmidt, T. (2021). Annotating and quantifying sentiment and emotions in German plays from around 1800. In Sentiment Analysis in Literary Studies (Workshop). Graz, Austria. (Keynote presentation). Video of the presentation: https://www.youtube.com/watch?v=WvJ8BvaSJCw 

Schmidt, T., Dennerlein, K. & Wolff, C. (2022). Insights and Perspectives of the Research project ‘Emotions in Drama’. In Computational Stylistics Workshop on Emotion and Sentiment Analysis in Literature. Paris, France. (Presentation at the University Paris)

Wolff, C., Dennerlein, K. & Schmidt, T. (2020). Emotions in Drama - Emotionen im Drama. Projektvorstellung. In Digital Humanities Day Leipzig 2020 (DHDL 2020). (Poster presentation). Link to poster: https://fdhl.info/wp-content/uploads/2020/12/Poster_DINA4.pdf  Link to video: https://youtube.com/watch?v=9DdybUzN92E

## Contact:

<ul>
  <li><a href="https://www.uni-regensburg.de/sprache-literatur-kultur/medieninformatik/sekretariat-team/thomas-schmidt/index.html">Thomas Schmidt</a></li>
  <li><a href="https://www.germanistik.uni-wuerzburg.de/lehrstuehle/computerphilologie/mitarbeiter/dennerlein/">Katrin Dennerlein</a></li>
  <li><a href="https://go.ur.de/christian-wolff">Christian Wolff</a></li>
</ul>

## Funding

This project is funded by the DFG (German Research Association) in the priority programme Computational Literary Studies (SPP 2207/1) with two grants (project number 424207618; grants DE 2188/3-1 and WO 835/4-1). https://dfg-spp-cls.github.io/projects_en/2020/01/24/TP-Emotions_in_Drama/

## License and Citation Information
All material on this repository is licensed under a <a href="https://creativecommons.org/licenses/by/4.0/deed.en">CC BY 4.0 Deed license</a>. 

<b>That means if you use any material of this repository, please cite one or more of the papers in the publications section depending on what material you use and what fits your usage best.</b>

If you use <b>the annotations in general</b> or the metadata without a focus on a specific publication, please cite the following publications:
<ul>
<li>Dennerlein, K., Schmidt, T., & Wolff, C. (2023b). EmoDrama. Ein Korpus mit Emotionsinformationen in Dramen von 1650-1815. Zeitschrift für digitale Geisteswissenschaften (ZfdG). https://doi.org/10.17175/2023_010</li>

<li>Schmidt, T., Dennerlein, K., & Wolff, C. (2023). Results of Emotion Annotation in German Drama from 1650-1815. In A. Baillot, T. Tasovac, W. Scholger, & G. Vogeler (Eds.), Digital Humanities 2023. Collaboration as Opportunity (DH2023) (pp. 181–183). Alliance of Digital Humanities Organizations (ADHO). https://doi.org/10.5281/ZENODO.8107952</li>
</ul>
If you use the <b>final classification model or classification results</b> from the main folder without a focus on a specific publication, please cite the following publications:
<ul>
<li>Schmidt, T., Dennerlein, K., & Wolff, C. (2021). Emotion Classification in German Plays with Transformer-based Language Models Pretrained on Historical and Contemporary Language. In S. Degaetano-Ortlieb, A. Kazantseva, N. Reiter, & S. Szpakowicz (Eds.), Proceedings of the 5th Joint SIGHUM Workshop on Computational Linguistics for Cultural Heritage, Social Sciences, Humanities and Literature (pp. 67–79). Association for Computational Linguistics. https://doi.org/10.18653/v1/2021.latechclfl-1.8</li>

<li>Dennerlein, K., Schmidt, T., & Wolff, C. (2023). Computational emotion classification for genre corpora of German tragedies and comedies from 17th to early 19th century. Digital Scholarship in the Humanities, 38(4), 1466–1481. https://doi.org/10.1093/llc/fqad046</li> 
</ul>
