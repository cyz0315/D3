# D3: Compute DNA Density and Distance to periphery.
D3 is a fast and accurate tool for computing **D**NA **D**ensity and **D**istance to periphrery (DisTP). In our paper, we show that the DNA density and DisTP are highly correlated with nuclear activities. 

paper.

![D3-logo](https://user-images.githubusercontent.com/37327473/133361303-b0526de0-b8d8-429a-a61d-260cd74e2111.png)

# Requirements
D3 was tested on Python v3.9.1 (macOS and DeepinOS), with the following basic requirements:

 * NumPy (tested on v1.20.2)
 * SciPy (tested on v1.6.2)
 * Pandas (tested on v1.2.4)
 * Seaborn (tested on v0.11.1)
 * Matplotlib (tested on v3.3.4)
 
#  Tipycal Workflow
Below is a typical workflow using the test data.
  ```
  cd PATH/WHERE/D3/AT
  mkdir -p test_result/den_dtp
  
  # Compute Density and DisTP
  python D3.py D3s test_data/dg_files test_data/hg19_diplo_20k.window.bed test_result/den_dtp
  
  # Construct Density-DisTP matrix
  python D3.py sta test_result/den_dtp/den_dtp test_data/hg19_diplo_20k.window.bed test_result/test_map_sta
  python D3.py map test_result/den_dtp/den_dtp test_data/hg19_diplo_20k.window.bed test_result/test_map
  python D3.py ave 
  
  ```
  
# License
D3 is free for non-commercial use by academic, government, and non-profit/not-for-profit institutions. A commercial version of the software is available and licensed through Xi’an Jiaotong University. For more information, please contact with Yizhuo che (cyz0315@stu.xjtu.edu.cn) or Kai Ye (kaiye@xjtu.edu.cn).
