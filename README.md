# 🎧 CodecFake+: Codec-Based Resynthesized Data as a Proxy for Detecting CodecFake Speech

> A benchmark for studying **neural codec–based deepfake speech detection**.
>
> Published in *IEEE Transactions on Audio, Speech and Language Processing*, vol. 34, pp. 2929–2944, 2026.

🔗 [Audio demo](https://responsiblegenai.github.io/CodecFake-Plus-Dataset/) · [Paper (IEEE)](https://doi.org/10.1109/TASLPRO.2026.3692291) · [arXiv](https://arxiv.org/abs/2501.08238) · [Dataset (Hugging Face)](https://huggingface.co/datasets/CodecFake/CodecFake_Plus_Dataset)

---

## 🧩 Overview
**CodecFake+** is a large-scale benchmark designed to evaluate the detection and generalization capabilities of models across diverse neural audio codec–generated deepfakes.
It enables controlled, taxonomy-aware analysis for codec-based deepfake research.

| Subset | Role | Bona fide | Spoof | Models | Paper | Status |
|---|---|---:|---:|---|---|---|
| **CoRS** | Train / Val / Eval | 44,455 | 1,378,105 | 31 codecs | [CodecFake+ (TASLP 2026)](https://doi.org/10.1109/TASLPRO.2026.3692291) | [Available](https://huggingface.co/datasets/CodecFake/CodecFake_Plus_Dataset) |
| **CoSG Eval** | Eval | 866 | 931 | 17 CoSG systems | [CodecFake+ (TASLP 2026)](https://doi.org/10.1109/TASLPRO.2026.3692291) | [Available](https://huggingface.co/datasets/CodecFake/CodecFake_Plus_Dataset) |
| **CoSG ExtEval** | Ext. Eval | — | — | 40 CoSG systems | [Proxy-to-Wild (ISCSLP 2026)](https://arxiv.org/abs/2606.07494) | Coming soon |

---

## 📰 News
- **[2026.11]** 🏆 Our follow-up paper, [Mitigating Proxy-to-Wild Domain Gap in Deepfake Speech](https://arxiv.org/abs/2606.07494), received an **Outstanding Paper** award at ISCSLP 2026. It introduces the **CoSG ExtEval** evaluation set.
- **[2026.05]** CodecFake+ was published in [*IEEE Transactions on Audio, Speech and Language Processing*](https://doi.org/10.1109/TASLPRO.2026.3692291). The earlier preprint title was "CodecFake+: A Large-Scale Neural Audio Codec-Based Deepfake Speech Dataset."
- **[2025.12]** 🏆 Our source tracing paper, [Towards Generalized Source Tracing for Codec-Based Deepfake Speech](https://arxiv.org/abs/2506.07294), received a **Best Student Paper Nomination (Top 2.5%)** at IEEE ASRU 2025. [[Award]](https://xjchen.tech/docs/ASRU2025_BestStudentNom.pdf)
- **[2025.10]** The CoRS and CoSG sets and their label files were released on [Hugging Face](https://huggingface.co/datasets/CodecFake/CodecFake_Plus_Dataset).

## How the Papers Relate

CodecFake+ is one part of our research line on codec-based deepfake speech. This table shows where it fits: the Dataset & Detection papers cover how CodecFake speech is detected and how well detectors generalize, and the Source Tracing papers use CodecFake+ to trace how a fake was generated, from defining the tasks to advancing the methods.

**Dataset & Detection**

| Paper | Position | Contribution | Builds on |
|---|---|---|---|
| [Proxy-to-Wild](https://arxiv.org/abs/2606.07494) (ISCSLP 2026)<br>🏆 Outstanding Paper | In-the-wild generalization | Domain-Shift Feature Augmentation; CoSG ExtEval | Extends CoSG Eval: 40 unseen models, long-form audio |
| **[CodecFake+](https://doi.org/10.1109/TASLPRO.2026.3692291) (TASLP 2026)**<br>[[arXiv]](https://arxiv.org/abs/2501.08238) | Large-scale benchmark | **This dataset:** CoRS, CoSG Eval, and the codec taxonomy | Extends CodecFake: 6 → 21 codec types, 3 → 17 CoSG systems, adds taxonomy |
| [CodecFake](https://doi.org/10.21437/Interspeech.2024-2093) (INTERSPEECH 2024) | Proof of concept | 6 codec types (15 codec models), 3 CoSG systems | — |

**Source Tracing**

| Paper | Position | Contribution | Builds on |
|---|---|---|---|
| [SASTNet](https://arxiv.org/abs/2506.07294) (ASRU 2025)<br>🏆 Best Student Paper Nomination (Top 2.5%)<br>[[Code]](https://github.com/ResponsibleGenAI/CodecFake-Source-Tracing) [[Award]](https://xjchen.tech/docs/ASRU2025_BestStudentNom.pdf) | Advanced method | Semantic-Acoustic Source Tracing Network | Taxonomy-based source tracing tasks on CodecFake+ |
| [Taxonomy-based source tracing](https://arxiv.org/abs/2505.12994) (INTERSPEECH 2025)<br>[[ISCA]](https://www.isca-archive.org/interspeech_2025/chen25j_interspeech.html) [[Code]](https://github.com/ResponsibleGenAI/CodecFake-Source-Tracing) | Task definition | Source tracing tasks via the codec taxonomy | CodecFake+ dataset and taxonomy |

Source tracing [code](https://github.com/ResponsibleGenAI/CodecFake-Source-Tracing) and [model checkpoints](https://huggingface.co/CodecFake/CodecFake_Source_Tracing) are available separately.

## Citations

### Dataset
If you use CodecFake+ or CoSG ExtEval, please cite:
```bibtex
@article{chen2026codecfake+,
  title   = {{CodecFake+}: Codec-Based Resynthesized Data as a Proxy for Detecting {CodecFake} Speech},
  author  = {Chen, Xuanjun and Du, Jiawei and Wu, Haibin and Zhang, Lin and Lin, I-Ming and Chiu, I-Hsiang and Ren, Wenze and Tseng, Yuan and Tsao, Yu and Jang, Jyh-Shing Roger and Lee, Hung-yi},
  journal = {IEEE Transactions on Audio, Speech and Language Processing},
  volume  = {34},
  pages   = {2929--2944},
  year    = {2026},
  doi     = {10.1109/TASLPRO.2026.3692291}
}

@inproceedings{chen2026mitigating,
  title     = {Mitigating Proxy-to-Wild Domain Gap in Deepfake Speech},
  author    = {Chen, Xuanjun and Wu, Yun-Shing and Lu, Wei-Chung and Lin, Claire and Wu, Haibin and Lee, Hung-yi and Jang, Jyh-Shing Roger},
  booktitle = {Proceedings of the International Symposium on Chinese Spoken Language Processing (ISCSLP)},
  year      = {2026}
}

@inproceedings{wu24p_interspeech,
  title     = {{CodecFake: Enhancing Anti-Spoofing Models Against Deepfake Audios from Codec-Based Speech Synthesis Systems}},
  author    = {Haibin Wu and Yuan Tseng and Hung-yi Lee},
  year      = {2024},
  booktitle = {{INTERSPEECH 2024}},
  pages     = {1770--1774},
  doi       = {10.21437/Interspeech.2024-2093},
  issn      = {2958-1796},
}
```

### Source Tracing
If you build on our source tracing work, please cite:
```bibtex
@inproceedings{chen2025towards,
  title     = {Towards Generalized Source Tracing for Codec-Based Deepfake Speech},
  author    = {Chen, Xuanjun and Lin, I-Ming and Zhang, Lin and Wu, Haibin and Lee, Hung-yi and Jang, Jyh-Shing Roger},
  booktitle = {2025 IEEE Automatic Speech Recognition and Understanding Workshop (ASRU)},
  pages     = {1--8},
  year      = {2025},
  doi       = {10.1109/ASRU65441.2025.11434771}
}

@inproceedings{chen2025codec,
  title     = {Codec-Based Deepfake Source Tracing via Neural Audio Codec Taxonomy},
  author    = {Chen, Xuanjun and Lin, I-Ming and Zhang, Lin and Du, Jiawei and Wu, Haibin and Lee, Hung-yi and Jang, Jyh-Shing Roger},
  booktitle = {{INTERSPEECH 2025}},
  pages     = {1538--1542},
  year      = {2025},
  doi       = {10.21437/Interspeech.2025-1297}
}
```
