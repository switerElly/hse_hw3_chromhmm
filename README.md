# hse_hw3_chromhmm
### Варфоломеева Анастасия БПМ213
[Ссылка на гугл колаб](https://colab.research.google.com/drive/1LFJBLx1PIFKdFM80cOPHlQq8WqnC6zLk?usp=sharing)

## cellmarkfiletable.txt
Клеточная линия: NHEK (для PC-9 из ДЗ2 нет данных)
Клеточная линия | Гистоновая метка | Имя файла | Файл с контролем 
| --- | --- | --- | ---
NHEK|H3k79me2|H3k79me2AlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H2az|H2azAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k4me3|H3k4me3StdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k36me3|H3k36me3StdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k27me3|H3k27me3StdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k27ac|H3k27acStdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k4me2|H3k4me2StdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k4me1|H3k4me1StdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H3k9ac|H3k9acStdAlnRep1.bam|ControlStdAlnRep1.bam
NHEK|H4k20me1|H4k20me1StdAlnRep1.bam|ControlStdAlnRep1.bam

## Выдача после ChromHMM
| ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/ChromHMM/transitions_10.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/ChromHMM/emissions_10.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/ChromHMM/NHEK_10_overlap.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/ChromHMM/NHEK_10_RefSeqTSS_neighborhood.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/ChromHMM/NHEK_10_RefSeqTES_neighborhood.png) |
| ------------- | ------------- |--------------------| -- | -- |

## Данные из геномного браузера
| ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2013-35-10.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2013-34-06.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2013-31-19.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2013-30-03.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2013-32-51.png) |
| ------------- | ------------- |--------------------| -- | -- |

## Названия эпигенетических типов(на основе выдачи ChromHMM, геномного браузера и литературы):
|Состояние|1|2|3|4|5|6|7|8|9|10|
|--|--|--|--|--|--|--|--|--|--|--|
|Метки|немного H3k36me3|H3k79me2, немного H3k36me3|H3k79me2, H3k4me1, немного H3k4me2, H3k27ac|H3k79me2, H3k4me1, H3k4me2, H3k4me3, H3k9ac, H3k27ac|H3k4me2, H3k4me3, H3k9ac, H3k27ac, H2az, немного H3k79me2|H3k4me2, H3k4me3, H2az|H3k4me1, H3k4me2, H3k27ac, немного H2az|немного H3k4me1, H2az|-|немного H3k27me3| 
|Часть генома|экзоны, гены, конец транскрипции|гены, конец транскрипции, экзон|гены, конец транскрипции, экзон|гены, конец транскрипции, экзон|CpG island, экзоны, гены, старт транскрипции|CpG island, экзоны, гены, старт транскрипции|конец транскрипции, ядерная ламина, гены|ядерная ламина, конец транскрипции|большой процент в геноме, ядерная ламина|конец транскрипции, ядерная ламина|
|Расположение относительно TSS(старт транскрипции)|-|-|немного до и после TSS|после TSS и несного до|на TSS(максимум находится на старте и спад в обе стороны)|на TSS(максимум находится на старте и спад в обе стороны)|немного до TSS|немного до TSS|-|немного на TSS и с обеих сторон от него|
|Расположение относительно TES(конец транскрипции)|на TES и с обеих сторон от него|несного до TES|немного на TES и с обеих сторон от него|на TES и с обеих сторон от него|на TES и с обеих сторон от него|на TES и с обеих сторон от него|немного на TES и с обеих сторон от него|немного на TES и с обеих сторон от него|-|на TES и с обеих сторон от него|
|Итог|Transcribed region|Transcribed region|Strong enhancer|Strong enhancer|Active promoter|Active promoter|Strong enhancer|Weak enhancer|Heterochromatin|Polycomb-repressed|

## Данные из геномного браузера для бонуса
Итоговый файл для бонуса можно найти [тут](https://drive.google.com/file/d/1GbQx8Ve1GD7BpZrDjuHgi3zrFkcHGNEY/view?usp=sharing).
| ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2019-48-32.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2019-49-06.png) | ![image](https://github.com/switerElly/hse_hw3_chromhmm/blob/main/img/Screenshot%20from%202024-03-24%2019-49-49.png) |
| ------------- | ------------- |--------------------|
