# covid19tw-data 

## 專案任務：
- 蒐集 covid19 相關的數據
- 整理 covid19 相關的數據

## 資料夾說明：
- RawData：原始數據
- ETL：整理數據使用的源碼
    - etl-dev-ipynb：ETL 開發實用的 jupyter notebook
    - etl-dev-py：ETL 開發實用的 python 源碼或套件
    - etl-dev-r：ETL 開發實用的 R 源碼或套件
- ReleasedData：完成整理後的數據

## 專案的 git flow：

- branch naming： 
    - 分支合併方向：feature -> dev -> preview -> production
    - feature-?-v?-?：某功能的某版本的某開發項目分支 
    - dev-v?：某預定釋出版本的總開發分支（將展開與合併所有下轄功能分支） 
    - preview-v?： 某預定釋出版本的預覽分支 
    - production-v?：某預定釋出版本的釋出分支
    - hotfix-?：針對 preview 或 production 分支進行修復的分支

- git flow：採用 fork PR 的作法
    - Step1：fork 整個 Repo
    - Step2：從 dev-v? 分支出要開發的 feature-?-v?，或是從 feature-?-v? 中 分支出要開發的 feature-?-v?-?
    - Step3：開發完畢
    - Step4：合併前更新主線，並 rebase 準備 PR 的分支
    - Step5：對 dev-v? 分支或  feature-?-v? 分支發出 PR
    - Step6：審核完成後 merged

