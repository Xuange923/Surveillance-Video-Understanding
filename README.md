# UCA_dataset

This is the official project page of the paper "Towards Surveillance Video-and-Language Understanding: New Dataset, Baselines, and Challenges"

## Project Overview

We are excited to introduce the **UCA** (UCF-Crime Annotation) dataset, meticulously crafted based on the UCF-Crime dataset.

The UCA dataset is extensive, featuring **1,854** videos and **23,542** sentences that span 110.7 hours, each averaging **20 words** in length. Each video in the dataset has been meticulously annotated with event descriptions, providing precise start and end times down to **0.1 seconds**. This level of detail and annotation density makes UCA a valuable resource for exploring and advancing multi-modal learning techniques, especially in the field of intelligent security.

In addition to constructing this comprehensive dataset, we benchmark SOTA models for four multimodal tasks on UCA. These tasks serve as new baselines for the understanding of surveillance video in conjunction with language. Our experiments reveal that mainstream models, which performed well on publicly available datasets, face new challenges in the surveillance video context. This underscores the unique complexities of surveillance video-and-language understanding.

## Dataset Description

### Comparative Analysis with Other Video Datasets
The following table provides a statistical comparison between the UCA dataset and other traditional video datasets in multimodal learning tasks. Our dataset is specifically designed for the surveillance domain, featuring the longest average word count per sentence.

![tab-1.png](https://s2.loli.net/2023/12/04/pu2UQBCXsPYxikF.png)

### Quality and Fairness Assurance
During the video collection process for UCA, we conducted a meticulous screening of the original UCF-Crime dataset to filter out videos of lower quality. This ensures the quality and fairness of our UCA dataset. The low-quality videos identified had issues like repetitions, severe obstructions, or excessively fast playback speeds, which impeded the clarity of manual annotations and the precision of event time localization.

Consequently, we removed 46 videos from the original UCF-Crime dataset, resulting in a total of 1,854 videos for UCA. The data split in UCA is outlined in the table below.

![tab-2.png](https://s2.loli.net/2023/12/04/TwCVjQvGf5PmU6H.png)

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

**Annotation Examples**: The following image shows fine-grained sentence queries and their corresponding timing in our UCA dataset.
   [![fig-visual.jpg](https://i.postimg.cc/ZqyVxR0W/fig-visual.jpg)](https://postimg.cc/R347Mv7m)

### Data Folders

- `txt`: Contains annotation data in txt format.
- `json`: Contains annotation data in json format.
- `txt_mask`: Contains gender-neutral annotation data.

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

  ![tab-2.png](https://s2.loli.net/2023/12/04/TwCVjQvGf5PmU6H.png)

4. **Result of MAD**: 
   
   [![ex-mad.png](https://i.postimg.cc/pL0D7np0/ex-mad.png)](https://postimg.cc/G4y8TtPY)
   

## Visualizations

To better understand the dataset and the experimental outcomes, the following visualizations are included:


1. **TSGV Visualization**: Example by MMN.
   [![fig-tsgv-2.jpg](https://i.postimg.cc/mhfbhhc7/fig-tsgv-2.jpg)](https://postimg.cc/Mf5kF6mG)

2. **VC Visualization**: Example by SwinBert.
    [![fig-vc.jpg](https://i.postimg.cc/pVqj6Hwk/fig-vc.jpg)](https://postimg.cc/K4341dvg)

3. **DVC Visualization**: Example by PDVC.
   [![fig-dvc.jpg](https://i.postimg.cc/wjd95twr/fig-dvc.jpg)](https://postimg.cc/QH0LhMGg)

4. **MAD Captioning Results**: Examples of different video captioning results.
    [![fig-mad.jpg](https://i.postimg.cc/V5PPFTWt/fig-mad.jpg)](https://postimg.cc/kRsHJTZM)

## Original UCF-Crime Dataset Reference

Our UCA dataset is built upon the foundational UCF-Crime dataset. For those interested in exploring the original data, the UCF-Crime dataset can be downloaded directly from this link: [Download zip](http://www.crcv.ucf.edu/data1/chenchen/UCF_Crimes.zip).

Additionally, further details about the UCF-Crime project are available on their official website: [Visit here](https://www.crcv.ucf.edu/research/real-world-anomaly-detection-in-surveillance-videos/).

If you wish to reference the UCF-Crime dataset in your work, please cite the following paper:
```
@inproceedings{sultani2018real,
  title={Real-world anomaly detection in surveillance videos},
  author={Sultani, Waqas and Chen, Chen and Shah, Mubarak},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={6479--6488},
  year={2018}
}
```
Each annotation in our UCA dataset is associated with a corresponding video in the original UCF-Crime dataset. Users interested in this dataset can easily match the videos to the annotation information after downloading.

## Usage and Contact

Our dataset is exclusively available for academic and research purposes. Please feel free to contact the original authors for inquiries, suggestions, or collaboration proposals.

### License
The dataset is available under the Apache-2.0 license.

### Cite Our Work

```
@inproceedings{
}
```
