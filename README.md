# Emotions in Drama

This is a GitHub-repository for the research project <a href="https://dfg-spp-cls.github.io/projects_en/2020/01/24/TP-Emotions_in_Drama/">Emotions in Drama</a>.

The repository is used to store data and other material that is created during the project and meant to be published or serves as additional material for papers.

Please refer to the reference section for informations about all publications and scientific contributions. The main components of this repository are described as follows:

## Annotations

The annotation folder contains the final annotations of 18 plays according to our guidelines (Dennerlein, Schmidt & Wolff, 2022c) and has the following structure:
<ul>
  <li>Emotions: Emotion annotations for 18 plays including implicit source/target annotations.</li>
  <ul>
    <li>Raw_Emotion_Annotations: Unfiltered (raw) emotion annotations by two annotators each.</li>
    <li>Filtered_Emotion_Annotations_withNoAnnotation: Emotion annotations filterd by disagreements and including the no annotation class (non-annotated material).
    These are the annotations used to train the final classification model.</li>
   </ul>
    <li>Source_Target: Implicit and explicit source/target annotations for 18 plays and overall.</li>
  </ul>
  Some information regarding the annotations:
    <ul>
      <li>Please refer to Dennerlein, Schmidt and Wolff (2022c) for explanations of annotation data, processes and German/English translations.</li>
      <li>Main annotation attributes are: tag_type (sub-emotions), main_emotion_class, base_polarity (positive, negative, being moved, eventually no annotation)</li>
      <li>Annotations of different annotators are seperable via the annotator attribute and consist of 2-letter-abbreviations (e.g. VH, LS)</li>
    </ul>

## Classification_Model
This folder contains a link to the model used in Dennerlein, Schmidt and Wolff (2023; 2024) and evaluation information. The model achieves an average F1-score for sub-emotion classification of 72% and was fine-tuned for four epochs with a batch size of 32, a learning rate of 4e-5, and the Adam optimizer, utilizing a Tesla P100 GPU with the filtered annotations. 

Please refer to the <a href="https://huggingface.co/">hugging face library</a> on how to use the unzipped model. We also included a link to a google colab for a basic usage example.

## Classification_Results

The results of the application of the classification model on the sentences of 313 plays. Subsets of these results are used in Dennerlein, Schmidt and Wolff (2023; 2024). The original plays are from GerDracor, TextGrid or based on our own preparations.

Some information regarding the classification results:
<ul>
  <li>To get the concrete corpora used in papers please refer to the <b>Additional_Data_Per_Paper</b> section.</li>
  <li>Main annotation attributes are: pre1_tag_type (sub-emotions), pre1_main_emotion_class (main emotion class), pre1_base_polarity (positive, negative, being moved, eventually no annotation).</li>
  <li>The type attribute differs between character speeches (spoken text) and stage directions (Dennerlein, Schmidt & Wolff, 2024)</li>
  <li>Additional metadata is derived from the data in the <b>Metadata</b> folder.</li>
  <li>Only plays of the GerDracor corpus contain consistent gender information and character ids.</li>
</ul>

## Metadata

Metadata about the plays used for the classification process.

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
