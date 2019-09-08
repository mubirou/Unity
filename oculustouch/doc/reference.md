# Oculus Touch コントローラ･マニュアル
Version Alpha1（2019年09月06日リリース） 対応  
© 2019 夢寐郎

# ◆入門
1. GameManager オブジェクトの作成  
	1. [GameObject]-[Create Empty] を選択（空の GameObject の作成）
	1. 名前を "GameObject"→"GameManager" に変更  

1. GameManager クラスの作成
	1. [Assets]-[Create]-[C# Script] を選択（ C# スクリプトを作成）
	1. 名前を "NewBehaviourScript"→"GameManager" に変更

1. GameManager クラスのアタッチ
	1. [Hierarchy]-[GameManager]（GameObject）-[Inspector] を開く
	1. [Project]-[Assets]-[GameManager]（C# スクリプト）を上記の [Inspector] エリアにドラッグ＆ドロップ  

1. OculusTouch クラスのアタッチ
	1. [OculusTouch.cs](https://raw.githubusercontent.com/mubirou/Unity3D/master/oculustouch/OculusTouch.cs) ファイルをプロジェクト内の Assets フォルダ内に保存
	1. [Project]-[Assets]-[OculusTouch]（C# スクリプト）を上記の [Inspector] エリアにドラッグ＆ドロップ  

1. GameManager クラスの変更
	1. GameManager（C# スクリプト）は初期設定は次の通り  
		```
		using System.Collections;
		using System.Collections.Generic;
		using UnityEngine;

		public class GameManager : MonoBehaviour
		{
			// Start is called before the first frame update
			void Start()
			{
				
			}

			// Update is called once per frame
			void Update()
			{
				
			}
		}
		```
	1. 上記に [new OculusTouch()](#OculusTouch) 記述する

# ◆コンストラクタ
* [new OculusTouch()](#OculusTouch) : 


# ◆メソッド一覧
* [AddTargetObjects()](#AddTargetObjects) : 
* [RemoveTargetObjects()](#RemoveTargetObjects) : 


# ◆プロパティ
* [IsLHandTriggerDown](#IsLHandTriggerDown) : 
* [IsLIndexTriggerDown](#IsLIndexTriggerDown) : 
* [IsRHandTriggerDown](#IsRHandTriggerDown) : 
* [IsRIndexTriggerDown](#IsRIndexTriggerDown) : 
* [L](#L) : 
* [LHandTrigger](#LHandTrigger) : 
* [LIndexTrigger](#LIndexTrigger) : 
* [LThumbstickRotate](#LThumbstickRotate) : 
* [R](#R) : 
* [RHandTrigger](#RHandTrigger) : 
* [RIndexTrigger](#RIndexTrigger) : 
* [RThumbstickRotate](#RThumbstickRotate) : 
* [TargetObjects](#TargetObjects) : 


# ◆イベント
* [ADown](#) : 
* [ARawTouch](#) : 
* [AUp](#) : 
* [BDown](#) : 
* [BRawTouch](#) : 
* [BUp](#) : 
* [LHandTriggerDown](#) : 
* [LHandTriggerUp](#) : 
* [LIndexTriggerDown](#) : 
* [LIndexTriggerRawNearTouch](#) : 
* [LIndexTriggerRawTouch](#) : 
* [LIndexTriggerUp](#) : 
* [LLaserDown](#) : 
* [LLaserOut](#) : 
* [LLaserOver](#) : 
* [LLaserUp](#) : 
* [LLsserUpOutside](#) : 
* [LThumbstickDown](#) : 
* [LThumbstickDownDown](#) : 
* [LThumbstickDownUp](#) : 
* [LThumbstickLeftDown](#) : 
* [LThumbstickLeftUp](#) : 
* [LThumbstickRawTouch](#) : 
* [LThumbstickRightDown](#) : 
* [LThumbstickRightUp](#) : 
* [LThumbstickUp](#) : 
* [LThumbstickUpUp](#) : 
* [LThumbstickUpDown](#) : 
* [RHandTriggerDown](#) : 
* [RHandTriggerUp](#) : 
* [RIndexTriggerDown](#) : 
* [RIndexTriggerRawNearTouch](#) : 
* [RIndexTriggerRawTouch](#) : 
* [RIndexTriggerUp](#) : 
* [RLaserDown](#) : 
* [RLaserOut](#) : 
* [RLaserOver](#) : 
* [RLaserUp](#) : 
* [RLsserUpOutside](#) : 
* [RThumbstickDown](#) : 
* [RThumbstickDownDown](#) : 
* [RThumbstickDownUp](#) : 
* [RThumbstickLeftDown](#) : 
* [RThumbstickLeftUp](#) : 
* [RThumbstickRawTouch](#) : 
* [RThumbstickRightDown](#) : 
* [RThumbstickRightUp](#) : 
* [RThumbstickUp](#) : 
* [RThumbstickUpUp](#) : 
* [RThumbstickUpDown](#) : 
* [StartDown](#) : 
* [StartUp](#) : 
* [XDown](#) : 
* [XRawTouch](#) : 
* [XUp](#) : 
* [YDown](#) : 
* [YRawTouch](#) : 
* [YUp](#) : 

***

<a name="OculusTouch"></a>

# new OculusTouch()

### ◆構文
new OculusTouch()

### ◆引数
なし  

### ◆説明
コンストラクタ。Oculus Touchを制御するためのクラス。

### ◆例文
```
//GameManager.cs
using UnityEngine;

public class GameManager : MonoBehaviour {
    void Start() {
        OculusTouch _oculusTouch = GetComponent<OculusTouch>();
        _oculusTouch.L = GameObject.Find("OculusTouchL");
        _oculusTouch.R = GameObject.Find("OculusTouchR");
    }
}
```

### ◆参照
[GetComponent](https://docs.unity3d.com/ja/current/ScriptReference/GameObject.GetComponent.html)