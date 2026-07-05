---
layout: distill
permalink: /dress/
title: DREsS
description: Dataset for Rubric-based Essay Scoring
nav: false
nav_order: 0
---

> 🎉 DREsS is accepted to ACL 2025!

<div class="row">
    <div class="col-sm mt-3 mt-md-0 d-none d-md-block">
        {% include figure.liquid loading="eager" path="assets/img/haneul_yoo.jpg" title="Haneul Yoo" class="img-fluid rounded-circle z-depth-1" %}
        <h5 style="text-align: center;"><a href="https://haneul-yoo.github.io/">Haneul Yoo</a></h5>
    </div>
    <div class="col-sm mt-3 mt-md-0 d-none d-md-block">
        {% include figure.liquid loading="eager" path="assets/img/jieun_han.jpeg" title="Jieun Han" class="img-fluid rounded-circle z-depth-1" %}
        <h5 style="text-align: center;"><a href="https://zeunie.github.io/">Jieun Han</a></h5>
    </div>
    <div class="col-sm mt-3 mt-md-0 d-none d-md-block">
        {% include figure.liquid loading="eager" path="assets/img/soyeon_ahn.png" title="So-Yeon Ahn" class="img-fluid rounded-circle z-depth-1" %}
        <h5 style="text-align: center;"><a href="https://sites.google.com/view/soyeonahn">So-Yeon Ahn</a></h5>
    </div>
      <div class="col-sm mt-3 mt-md-0 d-none d-md-block">
        {% include figure.liquid loading="eager" path="assets/img/alice_oh.jpg" title="Alice Oh" class="img-fluid rounded-circle z-depth-1"  %}
        <h5 style="text-align: center;"><a href="https://aliceoh9.github.io/">Alice Oh</a></h5>
    </div>
</div>
<br/>

This is an official website of [DREsS: Dataset for Rubric-based Essay Scoring on EFL Writing (Yoo et al., 2025)](https://aclanthology.org/2025.acl-long.659/).

DREsS is a **large-scale**, **standard** dataset for **rubric-based automated essay scoring**. DREsS comprises three sub-datasets: 

- **DREsS_New** with 2,279 essays from English as a foreign language (EFL) learners and their scores assessed by experts
- **DREsS_Std.** with 6,515 essays and scores from existing datasets
- **DREsS_CASE** with 40,185 synthetic essay samples.

## Dataset

The essays in DREsS are scored on a range of 1 to 5, with increments of 0.5, based on the three rubrics: `content`, `organization`, and `language`.

| Criteria     | Description                                                                                                                                                                                                                                             |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Content      | Paragraph is well-developed and relevant to the argument, supported with strong reasons and examples.                                                                                                                                                   |
| Organization | The argument is very effectively structured and developed, making it easy for the reader to follow the ideas and understand how the writer is building the argument. Paragraphs use coherence devices effectively while focusing on a single main idea. |
| Language     | The writing displays sophisticated control of a wide range of vocabulary and collocations. The essay follows grammar and usage rules throughout the paper. Spelling and punctuation are correct throughout the paper.                                   |


{% details Data attributes %}
| Column | Type    | Description                                                                |
| ------ | ------- | -------------------------------------------------------------------------- |
| id     | Integer | A unique identifier of each essay sample                                   |
| source | String  | *[Optional]* An original source of the essay sample (only for DREsS_std)     |
| prompt | String  | An essay prompt                                                            |
| essay  | String  | A student-written essay                                                    |
| score  | Float   | A rubric-based score of the essay (content, organization, language, total) |
{% enddetails %}

{% details Data statistics %}
| Subdata    | Source    | Content | Organization | Language |
|------------|-----------|---------|--------------|----------|
| DREsS_New  | -         | 2,279   | 2,279        | 2,279    |
| DREsS_Std. | ASAP P7   | 1,569   | 1,569        | 1,569    |
|            | ASAP P8   | 723     | 723          | 723      |
|            | ASAP++ P1 | 1,785   | 1,785        | 1,785    |
|            | ASAP++ P2 | 1,799   | 1,799        | 1,799    |
|            | ICNALE EE | 639     | 639          | 693      |
| DREsS_CASE | -         | 8,307   | 31,086       | 792      |
| Total      |           | 17,101  | 39,880       | 9,586    |
{% enddetails %}


## Download

Please submit the [consent form](https://forms.gle/WCSzhyRkr4jgeeYS7). You will be redirected to the accessible link to DREsS.

## Citation

{% raw %}

```html
@inproceedings{yoo-etal-2025-dress,
    title = "{DRE}s{S}: Dataset for Rubric-based Essay Scoring on {EFL} Writing",
    author = "Yoo, Haneul  and
      Han, Jieun  and
      Ahn, So-Yeon  and
      Oh, Alice",
    editor = "Che, Wanxiang  and
      Nabende, Joyce  and
      Shutova, Ekaterina  and
      Pilehvar, Mohammad Taher",
    booktitle = "Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2025",
    address = "Vienna, Austria",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.acl-long.659/",
    doi = "10.18653/v1/2025.acl-long.659",
    pages = "13439--13454",
    ISBN = "979-8-89176-251-0",
}
```

{% endraw %}