# UCA_dataset

This is the official project page of the paper "Towards Surveillance Video-and-Language Understanding: New Dataset, Baselines, and Challenges"

## Project Overview

We are excited to introduce the **UCA** (UCF-Crime Annotation) dataset, meticulously crafted based on the UCF-Crime dataset.

The UCA dataset is extensive, featuring **1,854** videos and **23,542** sentences that span 110.7 hours, each averaging **20 words** in length. Each video in the dataset has been meticulously annotated with event descriptions, providing precise start and end times down to **0.1 seconds**. This level of detail and annotation density makes UCA a valuable resource for exploring and advancing multi-modal learning techniques, especially in the field of intelligent security.

In addition to constructing this comprehensive dataset, we benchmark SOTA models for four multimodal tasks on UCA. These tasks serve as new baselines for the understanding of surveillance video in conjunction with language. Our experiments reveal that mainstream models, which performed well on publicly available datasets, face new challenges in the surveillance video context. This underscores the unique complexities of surveillance video-and-language understanding.

## Dataset Description

### Format Explanation

The UCA dataset is available in two formats: `txt` and `json`.

- **txt format**:

  ```
  VideoName StartTime EndTime ##Video event description
  ```

- **json format**:

  ```
  "VideoName": {
      "duration": xx.xx,
      "timestamps": [
          [StartTime 1, EndTime 1],
          [StartTime 2, EndTime 2]
      ],
      "sentences": ["Video event description 1", "Video event description 2"]
  }
  ```

### Data Folders

- `txt`: Contains annotation data in txt format.
- `json`: Contains annotation data in json format.
- `txt_mask`: Contains gender-neutral annotation data.

### License

The dataset is available under the Apache-2.0 license.

## Experiment Tasks

We conducted four types of experiments on our dataset:

1. **Temporal Sentence Grounding in Videos (TSGV)**: This task focuses on temporal activity localization in a video based on a language query.
2. **Video Captioning (VC)**: Understanding a video clip and describing it with language.
3. **Dense Video Captioning (DVC)**: Involves generating the temporal localization and captioning of dense events in an untrimmed video.
4. **Multimodal Anomaly Detection (MAD)**: Utilizes captions as a text feature source to enhance traditional anomaly detection in complex surveillance videos.

## Experiment Results

For each task, multiple models were evaluated. Here, we present some experiment results as examples.
1. **Result of TSGV**:
   
   [![ex-tsgv.png](https://i.postimg.cc/2yfjT2YP/ex-tsgv.png)](https://postimg.cc/WFXP1mhn)
   
2. **Result of VC**: 
  
   [![ex-vc.png](https://i.postimg.cc/br2bS6TW/ex-vc.png)](https://postimg.cc/RJ4qjL2L)
   
3. **Result of DVC**:
   

  [![ex-dvc.png](https://i.postimg.cc/MTfb1KZ9/ex-dvc.png)](https://postimg.cc/5Y1CVJCz)


4. **Result of MAD**: 
   
   [![ex-mad.png](https://i.postimg.cc/pL0D7np0/ex-mad.png)](https://postimg.cc/G4y8TtPY)
   

## Visualizations

To better understand the dataset and the experimental outcomes, the following visualizations are included:

1. **Annotation Examples**: Fine-grained sentence queries and corresponding timing in our UCA dataset.
   [![fig-visual.jpg](https://i.postimg.cc/ZqyVxR0W/fig-visual.jpg)](https://postimg.cc/R347Mv7m)

2. **TSGV Visualization**: Example by MMN.
   [![fig-tsgv-2.jpg](https://i.postimg.cc/mhfbhhc7/fig-tsgv-2.jpg)](https://postimg.cc/Mf5kF6mG)

3. **VC Visualization**: Example by SwinBert.
    [![fig-vc.jpg](https://i.postimg.cc/pVqj6Hwk/fig-vc.jpg)](https://postimg.cc/K4341dvg)

4. **DVC Visualization**: Example by PDVC.
   [![fig-dvc.jpg](https://i.postimg.cc/wjd95twr/fig-dvc.jpg)](https://postimg.cc/QH0LhMGg)

5. **MAD Captioning Results**: Examples of different video captioning results.
    [![fig-mad.jpg](https://i.postimg.cc/V5PPFTWt/fig-mad.jpg)](https://postimg.cc/kRsHJTZM)

## Usage and Contact

Our dataset is exclusively available for academic and research purposes. Please feel free to contact the original authors for inquiries, suggestions, or collaboration proposals.
