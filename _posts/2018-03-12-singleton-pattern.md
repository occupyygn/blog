In OOP, a singleton class is a class that can have only one object (an instance of the class) at a time. Making the single object in JVM.

![SingletonDesignPattern]({{ "assets/images/java-post-img/singleton-design-pattern.png" | absolute_url }})


* 😘 I designed my love using singleton pattern.<br/>
  Via - Sir Aung Thaw Aye


* Design Pattern ထဲမွာ အလြယ္ဆံုးေျပာလို့ရတဲ့ Pattern ကေတာ့ singleton design pattern ပါပဲ. Creational Pattern စုဝင္ထဲကမွေပါ့ ကိုယ္ထုတ္လုပ္လိုက္တဲ့ obj က one single obj လုပ္ခ်င္ရင္ သည္ pattern ကိုသံုးရပါတယ္။ ေျပာရမယ္ဆိုရင္ user ကို contractor သံုးျပီး obj ကို ေဆာက္လို့ မရေအာင္ လုပ္ထားတယ္။ ေျပာမယ္ဆိုရင္ constructor ကို private ေပးျပီး static instance ကို instantiation လုပ္တာပါပဲ။<br/>
  Via - Ko Si Thu Hlaing


* Java class တစ္ခုကို instance တစ္ခုတည္း႐ွိေစခ်င္တဲ့ အခါမ်ိဳးမွာ ျဖစ္ေအာင္လုပ္ေပးႏိုင္ပါတယ္။ သူ႔မွာ private constructor တစ္ခု နဲ႔ instance တစ္ခုတည္းကိုသာ return ျပန္ေပးတဲ့ static method တစ္ခု ပါပါတယ္။ class တစ္ခုရွိတယ္ ဆိုပါစို႔။ အဲဒီ Class ကို "new" keyword နဲ႔ object ေတြ အမ်ားၾကီး ေဆာက္ၿပီးမသံုးေစခ်င္ဘူး။ Object တစ္ခုတည္းသာ သံုးေစတယ္။ အဲလို သံုးေစခ်င္တဲ့အခါမ်ိဳး နဲ႔ "new" keyword ျဖင့္ Object ေတြအမ်ားၾကီးေဆာက္ျခင္းမွ ကာကြယ္ခ်င္တဲ့ အခါမ်ိဳးမွာ Singleton Pattern သံုးပါတယ္။<br/>
  Via - Sir Kyaw Kyaw Lwin


* Class မွ ျဖစ္ေပၚလာသည့္ Object တစ္ခုတည္းသာ ရွိေအာင္ (တစ္နည္းအားျဖင့္၊ Object တစ္ခုထက္ ပိုတည္ေဆာက္လို႔ မရေအာင္) ေရးသားသည့္ ေရးဟန္ျဖစ္သည္။ Class မွ (new ျဖင့္) Object တိုက္႐ိုက္ တည္ေဆာက္ခြင့္မျပဳပဲ၊ Object တည္ေဆာက္၍ Return ျပန္ေပးႏိုင္ေအာင္ ႀကိဳတင္ေရးသားထားသည့္ Static Method တစ္ခုကို အသုံးျပဳ၍သာ Object တည္ေဆာက္ခြင့္ ျပဳျခင္းအားျဖင့္ Singleton လုပ္ေဆာင္ခ်က္ ရရွိႏိုင္သည္။<br/>
  Via - Sir Ei Maung


* Singleton design pattern ဆုိတာ GoF(Gang of Four) major design pattern ၂၃ မ်ိဳးထဲမွာ တစ္ခုအပါအ၀င္ပါပဲ။ သူ.ကုိ ဘာအတြက္သံုးလဲဆုိရင္ေတာ့ class တခုကုိ single instance ပဲလိုခ်င္ရင္ သံုးပါတယ္။ ဆုိခ်င္တာက class တခုအတြက္ object တစ္ခုပဲေဆာက္ခ်င္တာေပါ့။ ဘယ္လိုေနရာမ်ိဳးမွာ အသံုး၀င္လဲဆုိေတာ့ globally available ၿဖစ္တဲ့ တစ္ခုထက္ပုိေဆာက္ဖုိ.မလိုတဲ့ object မ်ိဳးလိုရင္ သူ.ကုိသံုးလို.ရပါတယ္။ ဥပမာ သာမာန္ small application ေတြမွာ DAO connector အတြက္ singleton ကုိသံုးလို.ရပါတယ္။ Application တခုလံုးမွာ single object ပဲရိွေနေစခ်င္ရင္ singleton ကုိသံုးပါတယ္။ Java မွာဆုိရင္ေတာ့ java.lang.Runtime class နဲ. java.awt.Desktop တုိ.ဟာ singleton class ေတြပါ။ Runtime class ဆုိတာ ခုလက္ရိွ run ေနတဲ့ OS နဲ.ပတ္သတ္ၿပီး process ေတြ execute လုပ္ခ်င္ရင္သံုးလုိ.ရတဲ့ method ေတြ ေတာ္ေတာ္မ်ားမ်ားပါ ပါတယ္။ Runtime object ကုိတစ္ခုထက္ပိုေဆာက္ဖုိ.မလိုပါဘူး ဘာလုိ.လဲဆုိေတာ့ OS runtime က တစ္ခုထဲရိွလို.ပါ။ အဲ့လိုေနရာေတြမွာ Singleton ကုိသံုးေပမဲ့လဲ အလြန္အကြ်ံသံုးမယ္ဆုိရင္ singleton ဟာ bad pattern ၿဖစ္လာပါတယ္။ Singleton pattern ရဲ.မေကာင္းတဲ့အခ်က္ေတြက ေအာက္ပါအတုိင္းၿဖစ္ပါတယ္။ Global vairable ပံုစံၿဖင့္ အသံုးၿပဳတဲ့အတြက္ singleton classes ဟာ application တခုလံုးမွာ ေနရာအႏွံ.ပါေနႏုိင္ပါတယ္။ ဒါက ဘာကိုၿဖစ္ေစလဲဆုိေတာ့ tight coupling between classes ကိုၿဖစ္ေစႏုိင္ပါတယ္။ Singleton object ေတြဟာ application အစကေန အဆံုးထိ lifetime ရိွႏုိင္ပါတယ္။ ဒါက performance ကုိက်ေစႏုိင္ပါတယ္။ ေနာက္တခုက singleton object ေတြဟာ သူတုိ.ရဲ. state (variable )ေတြကို persistence state (အေသထားထားတဲ့အတြက္) unit testing code ေတြေရးတဲ့အခါမွာ singleton object ေတြဟာ ဒုကၡေပးႏုိင္ပါတယ္။ ဒါဆုိ singleton မသံုးပဲဘယ္လိုလုပ္မလဲ ေပါ့။ ရွင္းပါတယ္ new နဲ. object တစ္ခုအၿပင္ကေနေဆာက္ၿပီးေတာ့ လုိတဲ့ module ဆီကုိ dependency injection သံုးၿပီး ပို.လိုက္ပါ။ Singleton ကုိအလြန္အကြ်ံမဟုတ္ပဲ ေတာ္သင့္ရံုပဲသံုးမယ္ဆုိလဲ ၿပ ႆနာကို အထုိက္အေလ်ာက္ေၿပလည္ႏုိင္ပါလိမ့္မယ္။ Principle ဆုိတာ အတိအက်လုိက္နာရမယ္ဆုိတာ မဟုတ္ပါဘူး။ Rule မဟုတ္ပါဘူး ။<br/>
  Via - Sir Thet Khine
