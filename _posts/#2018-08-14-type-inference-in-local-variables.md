Java 10 မွာ ေျပာင္းလဲမႈအခ်ိဳ႕ထဲက Type-Inference in Local Variables ဆိုတဲ့အေၾကာင္းေလးကို မွ်ေဝေပးခ်င္ပါတယ္။

အထူးအဆန္းႀကီးရယ္ေတာ့မဟုတ္ပါဘူး။ Local variables ေတြကို <b><i>var</i></b> ဆိုတဲ့ keyword အသစ္နဲ႔ေရးလို႔ရလာတာပါ။

Kotlin မွာေတာ့ val နဲ႔ var ဆိုၿပီးသံုးလို႔ရပါတယ္။ Kotlin မွာ က var ကို Local variable အျဖစ္တင္မကဘဲ Class variable , Kotlin file variable အေနနဲ႔ပါ အသံုးျပဳလို႔ရတာပါ။

Java မွာ Kotlin ပံုစံအသံုးျပဳခ်င္ရင္ေတာ့ Lombok လို Third party library ရွိပါတယ္။

ကဲ လိုရင္းကိုဆက္သြားရေအာင္…

ယခင္က Local variables ေတြကို ဘယ္လို ေရးၾကရလဲ ျပန္ၾကည့္လိုက္ရေအာင္။

(၁) Local variales ေတြမွာ Access Modifiers ေတြျဖစ္တဲ့ public, private, protected စတဲ့ keywords ေတြ သံုးလို႔မရပါဘူး။

(၂) Java compiler က Local variables ေတြကို Default values ေတြ Assign လုပ္မေပးပါဘူး။ Default value ဆိုတာက ဥပမာ။ ။ String ထဲကို ဘာမွ initialize လုပ္မထားရင္ null, boolean ကိုဆိုရင္ false , integer ဆိုရင္ zero အစရွိသျဖင့္ ကိုေျပာတာပါ။

var အတြက္ ဥပမာေတြၾကည့္လိုက္ရေအာင္…

private void localVariableTypeInference() {
  //Java 10
  var str = "Hello Local Variable Type Inference";
  System.out.println(str);
}

private void localVariableTypeInference() {
  //Before Java 10
  var str = "Hello Local Variable Type Inference";
  System.out.println(str);
}

Array အတြက္ဆိုရင္

var arrayList = Arrays.asList("Dummy 1", "Dummy 2","Dummy 3");

Map အတြက္ဆိုရင္လည္း

var idToNameMap = new HashMap<Integer, String>();
idToNameMap.put(1, "One");
idToNameMap.put(2, "Two");
System.out.println(idToNameMap);

//For Loop
for (var i = 1; i <= 10; i++) {
 var dummy = 2 * i;
 System.out.println(dummy);
}

//For Each Loop
var list = Arrays.asList(1, 2, 3, 4, 5, 6);
for (var res : list) {
System.out.println(res);
}

//Java8 Stream
var stream = list.stream();
stream.filter(i -> i % 2 == 0).forEach(System.out::println);

//Ternary Operator
var d1 = 20;
var d2 = 50;
var max = d1 > d2 ? d1 : d2;
System.out.println(max);

//Anonymous Class
var message = “Running…”;
var runner = new Runnable() {
 @Override
 public void run() {
 System.out.println(message);
 }
};
runner.run();

//Passing value
private BigDecimal getSquareOf(BigDecimal n) {
var result = n.multiply(n);
 return result;
}

အေပၚ က ဥပမာေတြၾကည့္ၿပီး var ကိုသံုးတက္ေလာက္ပါၿပီ။

ဒါဆို ဘယ္လိုေနရာမ်ိဳးေတြမွာ သံုးမရလဲ ၾကည့္ရေအာင္…

အေပၚမွာ ေျပာခဲ့သလို Local variables ဆိုတဲ့အတိုင္း initialize မလုပ္ဘဲသံုးမရဘူး။
ဒီမွာက var num; ဆိုၿပီးကိုသံုးမရပါဘူး။ Assign တဲ့ Type ကို ၾကည့္ၿပီး Compile တဲ့အတြက္ပါ။

အရင္က Local variable က
String message; ဆိုၿပီး ေၾကျငာလို႔ရပါတယ္။သူ႔ကိုမသံုးခင္သာ Initialize လုပ္ရမွာပါ။

ေနာက္တစ္ခုက null assign မရပါဘူး။
var x = null; ဆိုရင္ မရပါဘူး။

ေနာက္ထပ္အသံုးျပဳလို႔မရတဲ့ ပံုစံေတြကေတာ့…

No lambda initializer
var runnable = ()->{};

No method reference initializer
var abc = BigDecimal::abc;

Not all array initializers
var number[] = new int{1,2,3};
ေရးခ်င္ရင္ var numbers = new int[]{1,2,3,4}; ဆိုၿပီးသံုးလို႔ရပါတယ္။

No compound declaration
var x= 10, y = 10, z = 10;

Method parameters as var not allowed
private void doSomething(var x){
}

Return types as var not allowed
private var doSomething(){
 return 10;
}

Catch Clause not allowed
catch (var e) {e.printStackTrace();}

ဒါေတြကေတာ့ local variables ေတြကို var အျဖစ္သံုးလို႔မရတာပါ။ အခုေလာက္ဆို နားလည္ၿပီလို႔ထင္ပါတယ္။

ဒါဆို Local variables ကို var နဲ႔ေရးတာနဲ႔ အရင္တုန္းကေရးတာနဲ႔ ဘာကြာလဲ ဆိုတာ ေမးစရာရွိမွာဘဲ။

“var is just a syntactic sugar” ပါ။ Syntactic အတြက္ပါဘဲ။
JVM မွာ လည္း no special instructions ပါဘဲ။

အမွားပါရင္လည္းေထာက္ျပေပးပါဦးဗ်။ ေက်းဇူးတင္ပါတယ္။
