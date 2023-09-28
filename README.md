# rna-seq_analysis

## 全体の流れ

### 1. 品質管理（Quality Control (QC)）<br>
シーケンシングリードの品質をチェック

低品質のリードを除去、リードをトリミング

FastQCダウンロード先
https://www.bioinformatics.babraham.ac.uk/projects/fastqc/



参照ゲノムへのマッピング(Reference genome mapping)：

遺伝子発現の定量化(Quantification)：

発現変動遺伝子解析(Differential expression analysis)：

機能アノテーション(Functional annotation)：

GO解析
Gene Ontology Consortium (http://www.geneontology.org/) は、標準化された用語によって生物学的現象を記述することを目的とした機能情報に関するデータベース
GO Termは大きく３つのサブカテゴリ（Biological Process , Cellular Component , Molecular Function）で表現
エンリッチメント解析を行うとき、発現変動遺伝子のみに着目した一般的なエンリッチメント解析と、発現変動遺伝子だけでなく遺伝子全体に着目した Gene Set Enrichment Analysis (GSEA) とよばれる解析方法

### RNA extraction
Total RNA was extracted from articular cartilage using a Qiagen RNeasy Mini Kit according to the manufacturer's protocols.




# FastQC
Basic Statistics: シーケンスデータの基本的な情報を示します。これには、シーケンスの数、シーケンスの長さ、GCコンテンツの平均などの情報が含まれます。
Per base sequence quality: 各塩基位置での品質スコアの分布を示すプロットです。Y軸には品質スコア、X軸には塩基の位置が示されています。品質が低下する位置を特定するのに役立ちます。
Per sequence quality scores: 各シーケンスの平均品質スコアの分布を示すプロット。品質スコアが低いシーケンスが多いかどうかを確認するのに役立ちます。
Per base sequence content: シーケンス中の各塩基の割合を示すプロット。期待されるAT/GC比率から大きく外れる場所があるかを確認できます。
Per sequence GC content: シーケンス毎のGCコンテンツの分布を示すプロット。通常、ベル形の分布が期待されます。
Per base N content: 各位置での不明な塩基（N）の発生頻度を示すプロット。
Sequence Length Distribution: シーケンスの長さの分布を示すプロット。
Duplicate Sequences: 重複するシーケンスの数とその発生頻度を示すプロット。
Overrepresented sequences: データセット内で過剰に繰り返されるシーケンスと、それが関連する可能性のある既知の配列を示します。
Kmer Content: シーケンス内の特定のKmerの出現を示すプロット。これは、特定の配列が過剰に表現されているか、または一部の位置で変動しているかを特定するのに役立つ場合があります。

RNA-seq and data analysis
Total RNA from each cartilage specimen was extracted using RNeasy Mini Kit (Qiagen) according to the manufacturer's protocols.
RNA integrity was assessed using an Agilent Technologies 2100 Bioanalyzer system (Agilent Technologies, Santa Clara, CA, USA) and samples with an RNA Integrity Number (RIN) value > 5.0 were used for subsequent analysis. 
Total RNA-seq libraries were generated using a TruSeq Stranded Total RNA Sample Prep Kit (Illumina, San Diego, CA, USA) following the manufacturer’s protocol. 
Library pools and clusters were generated on cBot and sequenced using a Novaseq 6000 Sequencing System (Illumina), yielding 2,500 reads with 2 × 100 base pair (bp) read lengths.



# Bulk RNA isolation
For bulk RNA isolation, segments were transferred to RNAlater (Qiagen) for 1 h at 4°C before removing the RNAlater and freezing samples at −80°C. Segment samples were cryo-pulverized (59012 N, Biospec) and gently resuspended in TriFast™ (VWR), mixed with 1-bromo-3-chloropropane (Sigma Aldrich) and incubated for 10 min. Centrifugation was performed for 10 min at 10.000×g and the top aqueous phase was further collected for RNA isolation using the RNeasy Mini Kit (Qiagen) according to the manufactures’ instructions. Purity of the RNA was analyzed via Nanodrop; RNA integrity and quality were verified via Agilent 2,100 Bioanalyzer or Fragment Analyzer (RNA-sequencing).

