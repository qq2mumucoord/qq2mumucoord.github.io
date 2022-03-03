# O2 utils

**Simulation scripts**
- Load the environment on LXPLUS:
  ```ruby
  alienv enter VO_ALICE@O2sim::v20211203-1
  ```
- Run simulation workflow (kine only):
  ```ruby
  o2-sim -j 4 -n 1000 -g external -o sgn -m "PIPE ITS TPC" --configKeyValues "GeneratorExternal.fileName=$O2DPG_ROOT/MC/config/PWGDQ/external/generator/GeneratorCocktailPromptCharmoniaToMuonEvtGen_pp13TeV.C;GeneratorExternal.funcName=GeneratorCocktailPromptCharmoniaToMuonEvtGen_pp13TeV()"
  ```
  
  
  Run TableMaker and TableReader on MC sample
  
  ```ruby
  python runTableMaker2.py configTableMakerMCRun3.json runMC table-maker-m-c:processMuonOnlyWithCov:true
  ```
  
  ```ruby
  o2-analysis-dq-efficiency --configuration json://configAnalysisMC.json --aod-writer-json writerConfiguration_dileptons.json -b
  ```
