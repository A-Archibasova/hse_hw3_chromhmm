# hse_hw3_chromhmm

[Collab](https://colab.research.google.com/drive/15pvGdmRgAwvVP6IPakkpnlMigqKMQG-9?usp=sharing)

# Main part

Клеточная линия, рассматриваемая в Дз2 (IMR-90), не содержит ChIP-seq эксперименты в рассматриваемых гистоновых метках, поэтоому для данного дз была выбрана GM12878

## Список гистоновых меток

| Гистоновая метка | Ссылка |
|------------------|--------|
|   H4K20me1          |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H4k20me1StdAlnRep1.bam    |
|   H3K79me2        |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k79me2StdAlnRep1.bam    |
|   H3K36me3        |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k36me3StdAlnRep1.bam    |
|   H3K27me3        |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k27me3StdAlnRep1.bam    |
|   H3K9me3         |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k9me3StdAlnRep1.bam    |
|   H3K4me2        |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k4me2StdAlnRep1.bam    |
|   H3K4me3       |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k4me3StdAlnRep1.bam    |
|   H3K4me1       |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k4me1StdAlnRep1.bam    |
|   H2AFZ       |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H2azStdAlnRep1.bam    |
|   H3K9ac       |    http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneGm12878H3k9acStdAlnRep1.bam    |

## cellmarkfiletable.txt

[Файл](./cellmarkfiletable.txt)

## ChromHMM
[Папка с выдачей](./ChromHMM/)

| |  |
|------------------|--------|
|   <img width="351" alt="Screenshot 2022-03-27 at 20 57 15" src="https://user-images.githubusercontent.com/71605966/160294261-f162da9e-d564-4154-bca4-4a3e15fff63e.png">   |  <img width="350" alt="Screenshot 2022-03-27 at 20 58 07" src="https://user-images.githubusercontent.com/71605966/160294294-0fce3c3f-b8c9-4425-babd-3a9d49029a64.png"> |
|    <img width="415" alt="Screenshot 2022-03-27 at 20 58 46" src="https://user-images.githubusercontent.com/71605966/160294315-df29650c-b53d-49af-98ac-a2da99730bec.png"> |  <img width="592" alt="Screenshot 2022-03-27 at 20 59 44" src="https://user-images.githubusercontent.com/71605966/160294354-fb6854d4-22d9-4953-9d86-3d411b132f5b.png"> |
|  <img width="596" alt="Screenshot 2022-03-27 at 21 00 10" src="https://user-images.githubusercontent.com/71605966/160294380-85d8fe29-f3cd-4f34-be36-f6b536fec844.png"> ||

## Эпигетические типы

| Состояние | Эпигенетический тип |Встречаемость в гистоновых модификациях| Описание | Изображение из USCC |
|-----------|----------|------|----------|---------------------|
|     1     |  Promoter  |  H3K4me1, в остальных значительно меньше   | Во всех, чаще RefSeqTES, LaminB1lads |
|     2     |  Enhancer |  Сильнее всего в H3K4me1 и H3K4me2, меньше в H3K4me3, H2AZ и H3K9ac |  Во всех, наиболее RefSeqTES | 
|     3     |  Enhancer |  H2AZ, меньше в H3K4me1 и H3K4me2  |  Во всех, кроме RefSeqGene  |
|     4     |  Repressed |  Чаще в H3K4me3, H3K4me2, H2AZ и H3K9ac |  CpGIsland, RefSeqExon, RefSeqTSS, RefSeqTSS2kb |
|     5     |  Enhancer |  Чаще в H3K4me3, H3K4me2, H3K79me2 и H3K9ac |  Во всех, кроме LaminB1lads |
|     6     |  Heterochromatin  |  Чаще в H3K79me2, меньше в H3K4me1, H3K4me2, H3K4me3  | RefSeqGene, меньше RefSeqTES, RefSeqTSS2kb |
|     7     |  Transcribed |  H3K79me2, в остальных значительно меньше | Только RefSeqGene |
|     8     |  Repressed |  Почти не встречается, кроме H3K36me3  | RefSeqGene, RefSeqTES, RefSeqExon |
|     9     |  Repressed |   Почти не встречается, кроме H3K27me3  |  Все  |   
|    10     |  Repressed  |  Не встречается |  Только  LaminB1lads | 

<img width="1427" alt="Screenshot 2022-03-27 at 21 46 39" src="https://user-images.githubusercontent.com/71605966/160296020-803cc018-d513-43f5-9f7c-af3bac0e25a0.png">
