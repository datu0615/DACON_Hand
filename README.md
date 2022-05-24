# DACON_Hand
![20220524_125804](https://user-images.githubusercontent.com/84311270/169948591-b6d94521-355d-4a05-8913-76056b73e883.png)
Ego-Vision 관점의 영상에서 추출한 이미지 학습데이터를 활용한 인공지능 모델 기반의 손동작 인식 및 분류 모델 개발

## Dataset
open  
	|	--	train  
	|			|	--	0  
	|			|			|	--		0.png : 연속된 Image 중 첫 번째 이미지 (가장 낮은 숫자)   
	|			|			|	--		1.png : 연속된 Image 중 두 번째 이미지 (두 번째로 낮은 숫자)  
	|			|			|	--		2.png : 연속된 Image 중 세 번째 이미지 (세 번째로 낮은 숫자)  
	|			|			|					...					: 숫자의 크기 순으로 연속된 이미지들이 저장됨  
	|			|			`	--		0.json : 폴더명과 동일한 이름의 json 파일  
	|			|													연속된 Iamge에 대한 포괄 정보  
	|			|													actor : 배우에 대한 정보  
	|			|													image : 이미지에 대한 정보  
	|			|													annotations : 이미지의 id, label, key_point 정보  
	|			`	--	648  
	|	--	test  
	|			|	--	649  
	|			|			|	--		0.png  
	|			|			|	--		1.png  
	|			|			|	--		2.png  
	|			|			|					...  
	|			|			`	--		649.json  
	|			`	--	865  
	|  
	|	--	hand_gesture_pose.csv 	:	손동작에 대한 정보	  
	`	--	sample_submission.csv	:	제출 파일 Sample_submission  
  
  ## Model
  다양한 Data Augmentation 기법을 사용하여 데이터를 증강시키고 EfficientNetB5 모델을 사용하여 학습.
  
  ## Results
  Public Score : 0.91064, Private Score : 1.00549로 최종 45등으로 마무리.
