# CDVS
## 1. CDVS Dataset paintings 
### KeyNet 
#### KeyNet 0. KeyNet Move File
-------------------------------------------------------------------------------------------------------------------
python __1__CDVS__paintings__Annotations__KeyNet__All.py __CDVS__paintings__500__KeyNet_1024_b4_1
python __1__CDVS__paintings__Annotations__KeyNet__All.py __CDVS__paintings__700__KeyNet_1024_b4_1
python __1__CDVS__paintings__Annotations__KeyNet__All.py __CDVS__paintings__900__KeyNet_1024_b4_1

-------------------------------------------------------------------------------------------------------------------
#### KeyNet 1. KeyNet Extract  
./extract__1101__All.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__paintings__500__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__paintings__500__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__paintings__Result__All/__CDVS__paintings__500__KeyNet_1024_b4_1__0.txt

-------------------------------------------------------------------------------------------------------------------
./extract__1101__All.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__paintings__700__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__paintings__700__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__paintings__Result__All/__CDVS__paintings__700__KeyNet_1024_b4_1__0.txt

-------------------------------------------------------------------------------------------------------------------
./extract__1101__All.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__paintings__900__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__paintings__900__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__paintings__Result__All/__CDVS__paintings__900__KeyNet_1024_b4_1__0.txt

-------------------------------------------------------------------------------------------------------------------
#### KeyNet 2. KeyNet  Move  
@~/f/CDVS/__TestEnv/__Extract__KeyNet

-------------------------------------------------------------------------------------------------------------------
python __3__cdvs__paintings__Trun_Move_KeyNet_DB_Extract.py __CDVS__paintings__900__KeyNet_1024_b4_1 0
python __3__cdvs__paintings__Trun_Move_KeyNet_DB_Extract.py __CDVS__paintings__700__KeyNet_1024_b4_1 0

-------------------------------------------------------------------------------------------------------------------

#### KeyNet 3. KeyNet Matching  
##### 700
./match_correct.exe __CDVS__paintings__matching_pairs.txt __CDVS__paintings__non_matching_pairs.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__700__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__700__KeyNet_1024_b4_1.txt
##### 900
./match_correct.exe __CDVS__paintings__matching_pairs.txt __CDVS__paintings__non_matching_pairs.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__900__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__900__KeyNet_1024_b4_1.txt
##### 500
./match_correct.exe __CDVS__paintings__matching_pairs.txt __CDVS__paintings__non_matching_pairs.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__500__KeyNet_1024_b4_1.txt
##### Class
./match_correct.exe __CDVS__paintings__matching_pairs__Canon.txt __CDVS__paintings__non_matching_pairs__Canon.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__500__KeyNet_1024_b4_1__Canon.txt
./match_correct.exe __CDVS__paintings__matching_pairs__Droid.txt __CDVS__paintings__non_matching_pairs__Droid.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__500__KeyNet_1024_b4_1__Droid.txt
./match_correct.exe __CDVS__paintings__matching_pairs__E63.txt __CDVS__paintings__non_matching_pairs__E63.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__500__KeyNet_1024_b4_1__E63.txt
./match_correct.exe __CDVS__paintings__matching_pairs__Palm.txt __CDVS__paintings__non_matching_pairs__Palm.txt 0 __KeyNet__CDVS__paintings__Data/__CDVS__paintings__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__paintings__Result/__CDVS__paintings__500__KeyNet_1024_b4_1__Palm.txt
##### Txt

sed -n '1,910 p' __CDVS__annotations/__CDVS__paintings__non_matching_pairs.txt  >  __CDVS__annotations/__CDVS__paintings__non_matching_pairs__Canon.txt
sed -n '911,1820 p' __CDVS__annotations/__CDVS__paintings__non_matching_pairs.txt  >  __CDVS__annotations/__CDVS__paintings__non_matching_pairs__E63.txt
sed -n '1821,2730 p' __CDVS__annotations/__CDVS__paintings__non_matching_pairs.txt  >  __CDVS__annotations/__CDVS__paintings__non_matching_pairs__Droid.txt
sed -n '2731,3640 p' __CDVS__annotations/__CDVS__paintings__non_matching_pairs.txt  >  __CDVS__annotations/__CDVS__paintings__non_matching_pairs__Palm.txt

-------------------------------------------------------------------------------------------------------------------

### TestModel  
#### TestModel 1. TestModel Extract 
#### TestModel 2. TestModel  Move 
#### TestModel 3. TestModel Matching 

## 2. CDVS Dataset video 
--------------------------------------------------------------------------------------------------
### 1. Move File
python __1__CDVS__video__Annotations__KeyNet__All.py __CDVS__video__400__KeyNet_1024_b4_1

python __1__CDVS__video__Annotations__KeyNet__All.py __CDVS__video__400__KeyNet_1024_b4_1

### 2. Extract
#### 2-1. CDVS Standard TestModel Extract
./extract_TestModel.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel __KeyNet__Data__All/__CDVS__video__TestModel  >  __KeyNet__Data__All/__video__Result__All/__CDVS__Dataset__TestModel.txt

./extract_TestModel.exe annotations__All__S__640.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__S__640 __KeyNet__Data__All/__CDVS__video__TestModel__S__640 >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__S__640.txt
./extract_TestModel.exe annotations__All__S__2X.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__S__640 __KeyNet__Data__All/__CDVS__video__TestModel__S__2X >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__S__2X.txt
./extract_TestModel.exe annotations__All__S__4X.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__S__640 __KeyNet__Data__All/__CDVS__video__TestModel__S__4X >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__S__4X.txt
./extract_TestModel.exe annotations__All__All__2X.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__All__2X __KeyNet__Data__All/__CDVS__video__TestModel__All__2X >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__All__2X.txt
./extract_TestModel.exe annotations__All__All__4X.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__All__4X __KeyNet__Data__All/__CDVS__video__TestModel__All__4X >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__All__4X.txt
./extract_TestModel.exe annotations__All__All__640.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__All__640 __KeyNet__Data__All/__CDVS__video__TestModel__All__640 >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__All__640.txt
./extract_TestModel.exe annotations__Query.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__Query __KeyNet__Data__All/__CDVS__video__TestModel__Query >  __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__Query.txt
./extract_TestModel.exe annotations__All__All__O.txt 0 __KeyNet__Data__All/__CDVS__video__TestModel__All__O __KeyNet__Data__All/__CDVS__video__TestModel__All__O  >  __KeyNet__Data__All/__video__Result__All/__CDVS__Dataset__TestModel__All__O.txt


tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__All__640.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__All__640.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__All__4X.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__All__4X.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__All__2X.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__All__2X.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__S__640.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__S__640.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__S__2X.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__S__2X.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__S__4X.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__S__4X.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__TestModel__Query.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__TestModel__Query.txt

#### 2-2. CDVS Standard KeyNet Extract
./extract__1101__All.exe annotations__All__S__640.txt 0 __KeyNet__Data__All/__CDVS__video__300__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__video__300__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__video__Result__All/__CDVS__video__300__KeyNet_1024_b4_1_0.txt
./extract__1101__All.exe annotations__All__All__4X.txt 0 __KeyNet__Data__All/__CDVS__video__300__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__video__300__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__video__Result__All/__CDVS__video__300__KeyNet_1024_b4_1_0__All__4X.txt
tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__300__KeyNet_1024_b4_1_0__All__4X.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__300__KeyNet_1024_b4_1_0__All__4X.txt
./extract__1101__All.exe annotations__All__S__4X.txt 0 __KeyNet__Data__All/__CDVS__video__300__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__video__300__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__video__Result__All/__CDVS__video__300__KeyNet_1024_b4_1_0__S__4X.txt

./extract__1101__All.exe annotations__Query.txt 0 __KeyNet__Data__All/__CDVS__video__500__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__video__500__KeyNet_1024_b4_1 keynet_label.txt > __KeyNet__Data__All/__video__Result__All/__CDVS__video__500__KeyNet_1024_b4_1_0__Query.txt

tail -n 50 __KeyNet__Data__All/__video__Result__All/__CDVS__video__500__KeyNet_1024_b4_1_0__Query.txt > __KeyNet__Data__All/__video__Result__50/__50__CDVS__video__500__KeyNet_1024_b4_1_0__Query.txt

### 3. Move File
~/f/CDVS/__TestEnv/__Extract__KeyNet
##### 3-1. KeyNet  Move
python __3__cdvs__video__Trun_Move_KeyNet_DB_Extract.py __CDVS__video__600__KeyNet_1024_b4_1 0

##### 3-2. TestModel  Move
python __3__cdvs__video__Trun_Move_KeyNet_DB_Extract.py __CDVS__video__TestModel 0

### 4. Matching
~/f/CDVS/__TestEnv/__Match
##### 4-1. KeyNet Matching
./match_correct.exe __CDVS__video__matching_pairs__All__2X.txt __CDVS__video__non_matching_pairs__All__2X.txt 0 __KeyNet__CDVS__video__Data/__CDVS__video__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__video__Result/__CDVS__video__500__KeyNet_1024_b4_1__All__2X.txt
./match_correct.exe __CDVS__video__matching_pairs__All__O.txt __CDVS__video__non_matching_pairs__All__O.txt 0 __KeyNet__CDVS__video__Data/__CDVS__video__TestModel __CDVS__annotations > __KeyNet__CDVS__video__Result/__CDVS__video__TestModel__All__O.txt
./match_correct.exe __CDVS__video__matching_pairs__All__2X__5800.txt __CDVS__video__non_matching_pairs__All__2X__5800.txt 0 __KeyNet__CDVS__video__Data/__CDVS__video__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__video__Result/__CDVS__video__500__KeyNet_1024_b4_1__All__2X__5800.txt
./match_correct.exe __CDVS__video__matching_pairs__All__2X__N97.txt __CDVS__video__non_matching_pairs__All__2X__N97.txt 0 __KeyNet__CDVS__video__Data/__CDVS__video__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__video__Result/__CDVS__video__500__KeyNet_1024_b4_1__All__2X__N97.txt
./match_correct.exe __CDVS__video__matching_pairs__All__2X__N900.txt __CDVS__video__non_matching_pairs__All__2X__N900.txt 0 __KeyNet__CDVS__video__Data/__CDVS__video__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__video__Result/__CDVS__video__500__KeyNet_1024_b4_1__All__2X__N900.txt
./match_correct.exe __CDVS__video__matching_pairs__All__2X__iPhone.txt __CDVS__video__non_matching_pairs__All__2X__iPhone.txt 0 __KeyNet__CDVS__video__Data/__CDVS__video__500__KeyNet_1024_b4_1 __CDVS__annotations > __KeyNet__CDVS__video__Result/__CDVS__video__500__KeyNet_1024_b4_1__All__2X__iPhone.txt

-------------------------------------------------------------------------------------------------------------------
sed -n '1,100 p'   __CDVS__annotations/__CDVS__video__matching_pairs__All__2X.txt  >  __CDVS__annotations/__CDVS__video__matching_pairs__All__2X__5800.txt
sed -n '101,200 p' __CDVS__annotations/__CDVS__video__matching_pairs__All__2X.txt  >  __CDVS__annotations/__CDVS__video__matching_pairs__All__2X__N97.txt
sed -n '201,300 p' __CDVS__annotations/__CDVS__video__matching_pairs__All__2X.txt  >  __CDVS__annotations/__CDVS__video__matching_pairs__All__2X__N900.txt
sed -n '301,400 p' __CDVS__annotations/__CDVS__video__matching_pairs__All__2X.txt  >  __CDVS__annotations/__CDVS__video__matching_pairs__All__2X__iPhone.txt
sed -n '1,100 p'   __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X.txt    >  __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X__5800.txt
sed -n '101,200 p' __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X.txt    >  __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X__N97.txt
sed -n '201,300 p' __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X.txt    >  __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X__N900.txt
sed -n '301,400 p' __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X.txt    >  __CDVS__annotations/__CDVS__video__non_matching_pairs__All__2X__iPhone.txt

-------------------------------------------------------------------------------------------------------------------
##### 4-2. TestModel Matching
./match_correct.exe __CDVS__objects__matching_pairs.txt __CDVS__objects__non_matching_pairs.txt 6 __KeyNet__Standard__Data/__CDVS__Dataset__TestModel __CDVS__annotations/

--Srcipt
~/f/CDVS/__TestEnv/__Extract__KeyNet
sh __sh__1__CDVS__Trun__KeyNet__Txt__All.sh

--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------
-CDVS Standard TestModel
--Move File
python __1__CDVS__Trun__KeyNet__Txt__All.py __CDVS__video__400__KeyNet_1024_b4_1

-- Extract
./extract_TestModel.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__Dataset__TestModel __KeyNet__Data__All/__CDVS__Dataset__TestModel

--Move File
~/f/CDVS/__TestEnv/__Extract__KeyNet
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__TestModel 0
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__TestModel 6

-- Matching
~/f/CDVS/__TestEnv/__Match
./match_correct.exe __CDVS__objects__matching_pairs.txt __CDVS__objects__non_matching_pairs.txt 0 __KeyNet__Standard__Data/__CDVS__Dataset__TestModel __CDVS__annotations/
./match_correct.exe __CDVS__objects__matching_pairs.txt __CDVS__objects__non_matching_pairs.txt 6 __KeyNet__Standard__Data/__CDVS__Dataset__TestModel __CDVS__annotations/

--Srcipt
~/f/CDVS/__TestEnv/__Extract__KeyNet
sh __sh__1__CDVS__Trun__KeyNet__Txt__All.sh

--------------------------------------------------------------------------------------------------

## 3. CDVS__Dataset Object ============================================
--------------------------------------------------------------------------------------------------
-CDVS Standard TestModel
--Move File
python __1__CDVS__Trun__KeyNet__Txt__All.py __CDVS__Dataset__850__KeyNet_1024_b4_1

-- Extract
./extract_TestModel.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__Dataset__TestModel __KeyNet__Data__All/__CDVS__Dataset__TestModel

--Move File
~/f/CDVS/__TestEnv/__Extract__KeyNet
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__TestModel 0
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__TestModel 6

-- Matching
~/f/CDVS/__TestEnv/__Match
./match_correct.exe __CDVS__objects__matching_pairs.txt __CDVS__objects__non_matching_pairs.txt 0 __KeyNet__Standard__Data/__CDVS__Dataset__TestModel __CDVS__annotations/
./match_correct.exe __CDVS__objects__matching_pairs.txt __CDVS__objects__non_matching_pairs.txt 6 __KeyNet__Standard__Data/__CDVS__Dataset__TestModel __CDVS__annotations/

--Srcipt
~/f/CDVS/__TestEnv/__Extract__KeyNet
sh __sh__1__CDVS__Trun__KeyNet__Txt__All.sh

--------------------------------------------------------------------------------------------------
-KeyNet
-- Extract
./extract__1101__All.exe annotations__All.txt 6 __KeyNet__Data__All/__CDVS__Dataset__300__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__Dataset__300__KeyNet_1024_b4_1 keynet_label.txt
./extract__1101__All.exe annotations__All.txt 1 __KeyNet__Data__All/__CDVS__Dataset__500__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__Dataset__500__KeyNet_1024_b4_1 keynet_label.txt
./extract__1101__All.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__Dataset__1500__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__Dataset__1500__KeyNet_1024_b4_1 keynet_label.txt
./extract__1101__All.exe annotations__All.txt 6 __KeyNet__Data__All/__CDVS__Dataset__300__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__Dataset__300__KeyNet_1024_b4_1 keynet_label.txt

-- Move File
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__300__KeyNet_1024_b4_1 6
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__128__KeyNet_1024_b4_1 0
python __3__CDVS__Trun_Move_KeyNet_DB_Extract.py __CDVS__Dataset__1500__KeyNet_1024_b4_1 0

-- Matching
./match_correct.exe __CDVS__objects__matching_pairs.txt __CDVS__objects__non_matching_pairs.txt 0 __KeyNet__Standard__Data/__CDVS__Dataset__128__KeyNet_1024_b4_1 __CDVS__annotations/













Get-ChildItem -Path .\ -Recurse -Include *.DB.cdvs | Copy-Item -Path {$.Name} -Destination {“…\CDVS_DB_Match_Keynet\Dataset_KeyNet_0930_extract_750” +"keynet"+ $.Directory.Name +""+ $_.Name}

Get-ChildItem -Path .\ -Recurse -Include *.DB.cdvs | Copy-Item -Path {$_.Name}  -Destination {"..\..\..\CDVS_DB_Match_Keynet\Dataset_KeyNet_0930_extract_750\" +"keynet_"+ $_.Directory.Name +"_"+ $_.Name}

Get-ChildItem -Path .\ -Recurse -Include *.DB.cdvs | Copy-Item -Path {$.Name} -Destination {“…\CDVS_DB_Match_Keynet\Dataset_Ours_0920_VS12_Release_Source_1004_Release” +"keynet"+ $.Directory.Name +""+ $_.Name}


python train_network.py --data-dir ~/d/imagenet-object-localization-challenge/ILSVRC/Data --network-version KeyNet_1019_e100_b95_lr1e-4 --num-epochs 100 --batch-size 95 --write-summary True --init-initial-learning-rate 1e-4


annotations.txt 0 Test_Release_extract_KeyNet_0930_extract_750/v_artisans Test_Release_extract_KeyNet_0930_extract_750/v_artisans keynet_label.txt


python extract_multiscale_features.py --list-images HSequences_bench/HPatches_images.txt --results-dir Extract_KeyNet_1018_e500_b90/ --network-version KeyNet_1018_e500_b90 --num-points 300


./extract_KeyNet_0930_extract_750        annotations.txt 0 KeyNet_1018_e500_b95_p750/i_ajuntament       KeyNet_1018_e500_b95_p750/i_ajuntament keynet_label.txt./
./extract_KeyNet_0930_extract_750.exe annotations.txt 0 750/KeyNet_1024_b4/keypoint/i_ajuntament     750/KeyNet_1024_b4/keypoint/i_ajuntament    keynet_label.txt
./extract_Ours_0920_VS12_Release_Source_1004_Release.exe annotations.txt 0 750/KeyNet_1024_b4/keypoint/i_ajuntament 750/KeyNet_1024_b4/keypoint/i_ajuntament keynet_label.txt

./match_correct.exe  matching_Ours_0920_VS12_Release_Source_1004_Release.txt nonmatching_Ours_0920_VS12_Release_Source_1004_Release.txt 0 KeyNet_1018_e500_b95_p750 annotations


./extract__1101__All.exe annotations__All.txt 1 __KeyNet__Data__All/__CDVS__Dataset__500__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__Dataset__500__KeyNet_1024_b4_1 keynet_label.txt


./extract__1101__All.exe annotations__All.txt 0 __KeyNet__Data__All/__CDVS__Dataset__128__KeyNet_1024_b4_1 __KeyNet__Data__All/__CDVS__Dataset__128__KeyNet_1024_b4_1 keynet_label.txt