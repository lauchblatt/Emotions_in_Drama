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

## Contact:

<ul>
  <li><a href="https://www.uni-regensburg.de/sprache-literatur-kultur/medieninformatik/sekretariat-team/thomas-schmidt/index.html">Thomas Schmidt</a></li>
  <li><a href="https://www.germanistik.uni-wuerzburg.de/lehrstuehle/computerphilologie/mitarbeiter/dennerlein/">Katrin Dennerlein</a></li>
  <li><a href="https://go.ur.de/christian-wolff">Christian Wolff</a></li>
</ul>
