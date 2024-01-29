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




## Contact:

<ul>
  <li><a href="https://www.uni-regensburg.de/sprache-literatur-kultur/medieninformatik/sekretariat-team/thomas-schmidt/index.html">Thomas Schmidt</a></li>
  <li><a href="https://www.germanistik.uni-wuerzburg.de/lehrstuehle/computerphilologie/mitarbeiter/dennerlein/">Katrin Dennerlein</a></li>
  <li><a href="https://go.ur.de/christian-wolff">Christian Wolff</a></li>
</ul>
