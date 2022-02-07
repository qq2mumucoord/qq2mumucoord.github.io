# O2 utils

**Simulation scripts**
- Load the environment on LXPLUS:
  ```ruby
  alienv enter VO_ALICE@O2sim::v20211203-1
  ```
- Run simulation workflow (kine only):
  ```ruby
  o2-sim -j 4 -n 1000 -g external -o sgn -m "PIPE ITS TPC" --configKeyValues "GeneratorExternal.fileName=$O2DPG_ROOT/MC/config/PWGDQ/external/generator/GeneratorCocktailPromptCharmoniaToElectronEvtGen_pp13TeV.C;GeneratorExternal.funcName=GeneratorCocktailPromptCharmoniaToElectronEvtGen_pp13TeV()"
  ```
