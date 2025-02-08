
#### **1. ما هو Flutter؟**  
**الإجابة:**  
Flutter هو إطار عمل مفتوح المصدر تم تطويره بواسطة Google لإنشاء تطبيقات للهواتف المحمولة (Android و iOS) وسطح المكتب والويب باستخدام قاعدة كود واحدة بلغة Dart.

---

#### **2. ما هي اللغة المستخدمة في Flutter؟**  
**الإجابة:**  
يستخدم Flutter لغة **Dart**، وهي لغة برمجة طورتها Google وتتميز بالأداء العالي والدعم القوي للبرمجة الشيئية.

---

#### **3. ما الفرق بين StatefulWidget و StatelessWidget؟**  
**الإجابة:**  
- **StatelessWidget**: هو عنصر واجهة مستخدم (widget) ثابت لا يتغير أثناء تشغيل التطبيق. يتم إعادة بنائه فقط عند إنشاءه أول مرة.  
- **StatefulWidget**: هو عنصر واجهة مستخدم يمكنه تغيير حالته أثناء تشغيل التطبيق وإعادة بناء نفسه عند حدوث تغييرات.

---

#### **4. ما هو الفرق بين Hot Reload و Hot Restart؟**  
**الإجابة:**  
- **Hot Reload**: يقوم بتحديث واجهة المستخدم بسرعة دون فقدان الحالة الحالية، مما يساعد في تطوير أسرع.  
- **Hot Restart**: يقوم بإعادة تشغيل التطبيق من البداية، مما يؤدي إلى فقدان الحالة ولكنه يحل بعض المشكلات التي قد لا يتم إصلاحها بواسطة Hot Reload.

---

#### **5. كيف يتم إدارة الحالة في Flutter؟**  
**الإجابة:**  
يمكن إدارة الحالة باستخدام عدة طرق مثل:  
- **setState** (لإدارة الحالة داخل StatefulWidget)  
- **Provider** (نهج حديث ومدعوم من Google)  
- **Bloc (Business Logic Component)**  
- **GetX** (يتميز بالبساطة والأداء العالي)  
- **Riverpod** (بديل محسّن لـ Provider)

---

#### **6. ما هو الفرق بين main.dart و pubspec.yaml؟**  
**الإجابة:**  
- **main.dart**: هو الملف الأساسي الذي يحتوي على نقطة البداية لتشغيل تطبيق Flutter.  
- **pubspec.yaml**: هو ملف تكوين يحتوي على معلومات عن التطبيق مثل الاسم، الإصدار، الحزم الخارجية (dependencies)، والخطوط (fonts) والصور (assets).

---

#### **7. كيف يمكن تشغيل التطبيق على جهاز فعلي أو محاكي؟**  
**الإجابة:**  
- لتشغيل التطبيق على جهاز فعلي، يجب توصيله عبر USB وتشغيل **USB Debugging** ثم تنفيذ الأمر:  
  ```bash
  flutter run
  ```
- لتشغيل التطبيق على المحاكي، يجب أولاً تشغيل المحاكي عبر Android Studio ثم تنفيذ نفس الأمر أعلاه.

---

#### **8. ما هي Widgets الأساسية في Flutter؟**  
**الإجابة:**  
بعض الـ **Widgets** الأساسية تشمل:  
- **Text** (لعرض النصوص)  
- **Container** (لإنشاء حاويات مع أنماط مختلفة)  
- **Row و Column** (لتنظيم العناصر أفقياً وعمودياً)  
- **Stack** (لوضع العناصر فوق بعضها)  
- **ListView** (لعرض قائمة من العناصر)  
- **GestureDetector** (لإضافة استجابات للنقرات)

---

#### **9. كيف يتم إضافة صورة داخل التطبيق؟**  
**الإجابة:**  
يتم إضافة الصورة داخل ملف `pubspec.yaml` كالتالي:  
```yaml
flutter:
  assets:
    - assets/images/logo.png
```
ثم يمكن عرض الصورة باستخدام:  
```dart
Image.asset('assets/images/logo.png')
```

---

#### **10. ما هي الاختلافات بين Future و Stream؟**  
**الإجابة:**  
- **Future**: يُستخدم لإرجاع قيمة واحدة بعد اكتمال عملية غير متزامنة (مثل طلب HTTP).  
- **Stream**: يُستخدم للتعامل مع بيانات متعددة يتم استقبالها بمرور الوقت (مثل تحديثات الموقع أو تدفق البيانات المباشر).

---

#### **11. كيف يمكن تنفيذ طلب HTTP في Flutter؟**  
**الإجابة:**  
يمكن استخدام مكتبة `http` لإرسال طلبات HTTP:  
```dart
import 'package:http/http.dart' as http;

Future<void> fetchData() async {
  final response = await http.get(Uri.parse('https://api.example.com/data'));
  if (response.statusCode == 200) {
    print(response.body);
  } else {
    print('حدث خطأ: ${response.statusCode}');
  }
}
```

---

#### **12. كيف يمكن التنقل بين الشاشات في Flutter؟**  
**الإجابة:**  
يمكن استخدام `Navigator` للتنقل بين الشاشات:  
- للانتقال إلى صفحة جديدة:  
  ```dart
  Navigator.push(context, MaterialPageRoute(builder: (context) => SecondPage()));
  ```
- للعودة إلى الصفحة السابقة:  
  ```dart
  Navigator.pop(context);
  ```

---

#### **13. ما الفرق بين runApp و main في Flutter؟**  
**الإجابة:**  
- **main()** هي نقطة البداية للتطبيق وتقوم بتشغيل التطبيق.  
- **runApp()** هو الدالة التي تأخذ الـ **Widget** الرئيسي وتبدأ التطبيق.

---

#### **14. كيف يمكن استخدام Firebase في Flutter؟**  
**الإجابة:**  
1. أضف Firebase إلى التطبيق عبر `firebase_core`:  
   ```yaml
   dependencies:
     firebase_core: latest_version
   ```
2. قم بتثبيت الحزم باستخدام:  
   ```bash
   flutter pub get
   ```
3. قم بتكوين Firebase في المشروع من خلال `Firebase.initializeApp()`.

---

#### **15. كيف يمكن تخزين البيانات محلياً في Flutter؟**  
**الإجابة:**  
يمكن تخزين البيانات محلياً باستخدام:  
- **SharedPreferences** (لتخزين بيانات بسيطة مثل الإعدادات والمفاتيح)  
- **SQLite (sqflite package)** (لإدارة قواعد البيانات المحلية)  
- **Hive** (لحفظ البيانات بشكل أسرع بدون قاعدة بيانات SQL)

---

#### **16. كيف يتم التعامل مع الأخطاء في Flutter؟**  
**الإجابة:**  
يمكن التعامل مع الأخطاء باستخدام `try-catch`:  
```dart
try {
  int result = 10 ~/ 0; // يؤدي إلى خطأ
} catch (e) {
  print('حدث خطأ: $e');
}
```

---

#### **17. كيف يمكن تشغيل كود متزامن في Flutter؟**  
**الإجابة:**  
يمكن تشغيل كود غير متزامن باستخدام `async/await`:  
```dart
Future<void> fetchData() async {
  await Future.delayed(Duration(seconds: 2)); // محاكاة عملية غير متزامنة
  print('تم جلب البيانات');
}
```

---

#### **18. ما هو الفرق بين Expanded و Flexible؟**  
**الإجابة:**  
- **Expanded**: يملأ المساحة المتاحة بالكامل داخل `Row` أو `Column`.  
- **Flexible**: يمنح تحكمًا أكبر في كيفية تمدد العنصر داخل المساحة المتاحة.

---

#### **19. كيف يمكن تنفيذ Dark Mode في Flutter؟**  
**الإجابة:**  
يتم ذلك باستخدام `ThemeData` في `MaterialApp`:  
```dart
MaterialApp(
  theme: ThemeData.light(),
  darkTheme: ThemeData.dark(),
  themeMode: ThemeMode.system, // تغيير تلقائي حسب نظام الجهاز
)
```

---

#### **20. كيف يمكن تحسين أداء تطبيق Flutter؟**  
**الإجابة:**  
- استخدام **const** للـ widgets الثابتة  
- تقليل عمليات إعادة البناء باستخدام **Provider** أو **Bloc**  
- تجنب الاستخدام غير الضروري لـ `setState`  
- استخدام **Flutter DevTools** لمراقبة الأداء  

---

### **أسئلة وأجوبة مقابلات Flutter عن Dart و State Management ونشر التطبيقات**  

---

### **📌 أولًا: إتقان Dart**  

#### **1. ما هي الميزات الأساسية في لغة Dart؟**  
**الإجابة:**  
Dart هي لغة برمجة حديثة طورتها Google وتتميز بالآتي:  
- **Strongly Typed** (لغة ذات أنواع بيانات قوية)  
- **Garbage Collection** (إدارة تلقائية للذاكرة)  
- **Asynchronous Programming** (دعم البرمجة غير المتزامنة باستخدام Future و Stream)  
- **OOP (البرمجة الكائنية)** (تدعم الكلاسات والتوريث والـ mixins)  
- **JIT & AOT Compilation** (تحسين الأداء أثناء التطوير والتشغيل)  

---

#### **2. ما الفرق بين var, final, const في Dart؟**  
**الإجابة:**  
- **var**: يمكن تغيير القيمة بعد التعيين، ويتم تحديد نوع المتغير تلقائيًا.  
  ```dart
  var name = "Ahmed";
  name = "Ali"; // ✅ مسموح
  ```
- **final**: لا يمكن تغيير القيمة بعد التعيين، ولكن يتم تعيينها وقت التشغيل.  
  ```dart
  final age = 25;
  age = 30; // ❌ خطأ
  ```
- **const**: لا يمكن تغيير القيمة بعد التعيين، ويتم تعيينها وقت **الترجمة (compile-time)**.  
  ```dart
  const pi = 3.14;
  ```

---

#### **3. ما الفرق بين Future و Stream؟**  
**الإجابة:**  
- **Future**: يستخدم لتنفيذ عملية غير متزامنة تعيد **قيمة واحدة فقط**.  
  ```dart
  Future<String> fetchData() async {
    return "Hello World";
  }
  ```
- **Stream**: يستخدم لاستقبال **عدة قيم** بشكل متدفق (مثل استقبال البيانات من API أو حساسات).  
  ```dart
  Stream<int> counterStream() async* {
    for (int i = 0; i < 5; i++) {
      yield i; // يرسل القيم واحدة تلو الأخرى
      await Future.delayed(Duration(seconds: 1));
    }
  }
  ```

---

#### **4. كيف يمكن استخدام Mixins في Dart؟**  
**الإجابة:**  
Mixins تسمح بإضافة وظائف للكلاسات بدون التوريث المباشر.  
```dart
mixin Logger {
  void log(String message) {
    print("LOG: $message");
  }
}

class MyClass with Logger {}

void main() {
  MyClass obj = MyClass();
  obj.log("Hello from mixin!"); // ✅
}
```

---

#### **5. كيف يتم التعامل مع Null Safety في Dart؟**  
**الإجابة:**  
Dart تستخدم **null safety** لمنع الأخطاء الناتجة عن القيم الفارغة.  
- **?** تعني أن المتغير يمكن أن يكون **null**.  
  ```dart
  String? name; // يمكن أن يكون null
  ```
- **!** تُستخدم لتأكيد أن القيمة **ليست null**.  
  ```dart
  print(name!); // ❌ قد يسبب خطأ إذا كانت null
  ```
- **??** تُستخدم لإعطاء قيمة افتراضية إذا كانت null.  
  ```dart
  String username = name ?? "Guest";
  ```

---

### **📌 ثانيًا: إدارة الحالة في Flutter (State Management)**  

#### **6. ما الفرق بين setState و Provider؟**  
**الإجابة:**  
- **setState**: يتم استخدامه داخل `StatefulWidget` لتحديث واجهة المستخدم يدويًا.  
  ```dart
  setState(() {
    counter++;
  });
  ```
- **Provider**: هو نهج لإدارة الحالة على مستوى التطبيق بالكامل، مما يسمح بإعادة بناء جزء معين فقط من الـ UI بدلاً من إعادة بناء الصفحة كاملة.  
  ```dart
  final counter = Provider<int>((ref) => 0);
  ```

---

#### **7. ما الفرق بين Provider و Bloc؟**  
**الإجابة:**  
| **المعيار**  | **Provider** | **Bloc** |
|-------------|-------------|---------|
| **التعقيد** | بسيط وسهل الاستخدام | أكثر تعقيدًا لكنه أكثر تنظيمًا |
| **الأداء** | جيد مع المشاريع الصغيرة | ممتاز للمشاريع الكبيرة |
| **طريقة العمل** | يستخدم `ChangeNotifier` للإشعارات | يعتمد على **Events & States** |
| **مثال** | `context.read<Counter>().increment()` | `bloc.add(IncrementEvent())` |

---

#### **8. ما هو Riverpod ولماذا يُفضل على Provider؟**  
**الإجابة:**  
- **Riverpod** هو نظام إدارة حالة مشابه لـ Provider ولكنه يحل بعض مشاكله، مثل **الأمان من التكرار (safe from context issues)**.  
- يدعم **Lazy Loading** (تحميل البيانات فقط عند الحاجة).  
- مثال على استخدام Riverpod:  
  ```dart
  final counterProvider = StateProvider<int>((ref) => 0);
  ```

---

### **📌 ثالثًا: نشر التطبيقات على Google Play و App Store**  

#### **9. ما الخطوات المطلوبة لنشر تطبيق Flutter على Google Play؟**  
**الإجابة:**  
1. **إنشاء حساب مطور على Google Play**.  
2. **إعداد التوقيع الرقمي (App Signing)**:  
   ```bash
   keytool -genkey -v -keystore my-release-key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias my-key-alias
   ```
3. **إضافة معلومات التوقيع إلى android/app/build.gradle**.  
4. **بناء التطبيق بصيغة APK أو AAB**:  
   ```bash
   flutter build apk --release
   flutter build appbundle
   ```
5. **رفع التطبيق على Google Play Console**.  

---

#### **10. ما الخطوات المطلوبة لنشر تطبيق Flutter على App Store؟**  
**الإجابة:**  
1. **إنشاء حساب Apple Developer** (مطلوب اشتراك سنوي).  
2. **إعداد Xcode وتكوين `Runner.xcworkspace`**.  
3. **توليد ملف `.ipa`** عبر الأمر:  
   ```bash
   flutter build ios --release
   ```
4. **رفع التطبيق عبر Transporter** أو `Xcode Organizer`.  
5. **إرسال التطبيق إلى المراجعة** في App Store Connect.  

---

#### **11. ما الفرق بين APK و AAB؟**  
**الإجابة:**  
- **APK (Android Package Kit)**: ملف تثبيت التطبيق التقليدي لنظام Android.  
- **AAB (Android App Bundle)**: صيغة جديدة تتيح لـ Google Play تقسيم التطبيق وتحسين حجمه بناءً على الجهاز. **(موصى به للنشر على Google Play)**.  

---

#### **12. ما هو TestFlight وكيف يمكن استخدامه لاختبار تطبيق iOS؟**  
**الإجابة:**  
TestFlight هو أداة من Apple لاختبار التطبيقات قبل نشرها في App Store.  
- يتم تحميل التطبيق على **App Store Connect** ثم إضافته إلى TestFlight لتوزيعه على المختبرين.  
- يمكن للمستخدمين تحميل التطبيق عبر **رابط الدعوة** دون الحاجة لنشره رسميًا.  

---
 
### **أسئلة وأجوبة مقابلات Flutter عن تحسين الأداء، التكامل مع APIs، وحل المشكلات التقنية**  

---

## **📌 أولًا: تحسين الأداء وضمان استجابة التطبيقات لمختلف الأجهزة**  

#### **1. ما هي أفضل الممارسات لتحسين أداء تطبيق Flutter؟**  
**الإجابة:**  
1. **استخدام `const` عند الإمكان** لتجنب إعادة إنشاء الـ widgets الثابتة.  
   ```dart
   const Text("Hello, Flutter!");
   ```
2. **تقليل استخدام `setState`** بحيث لا يتم إعادة بناء كل الصفحة عند كل تغيير.  
3. **استخدام `ListView.builder` بدلاً من `ListView`** لتجنب تحميل جميع العناصر دفعة واحدة.  
   ```dart
   ListView.builder(
     itemCount: items.length,
     itemBuilder: (context, index) {
       return ListTile(title: Text(items[index]));
     },
   );
   ```
4. **تقليل عدد الطبقات في الـ widget tree**.  
5. **استخدام `Image.network` مع `cacheWidth` و `cacheHeight`** لتوفير استهلاك الذاكرة.  
6. **استخدام `Isolates` لتنفيذ العمليات الثقيلة مثل فك تشفير البيانات**.  
7. **تقليل استخدام `Opacity` و `ClipRect`** حيث يؤثران على الأداء عند الاستخدام المكثف.  

---

#### **2. كيف يمكن ضبط التطبيق ليدعم مختلف الأجهزة وأحجام الشاشات؟**  
**الإجابة:**  
1. **استخدام `MediaQuery` للحصول على أبعاد الشاشة:**  
   ```dart
   double screenWidth = MediaQuery.of(context).size.width;
   ```
2. **استخدام `LayoutBuilder` لإنشاء تخطيطات ديناميكية:**  
   ```dart
   LayoutBuilder(
     builder: (context, constraints) {
       if (constraints.maxWidth > 600) {
         return TabletLayout();
       } else {
         return MobileLayout();
       }
     },
   );
   ```
3. **استخدام `FittedBox` و `Expanded` لتجنب مشاكل Overflow.**  
4. **استخدام `flutter_screenutil` لضبط الأحجام تلقائيًا بناءً على الجهاز.**  
   ```dart
   ScreenUtil().setWidth(100);
   ```

---

#### **3. كيف يمكن تحسين تجربة المستخدم لتجنب التقطيع (Jank) في التطبيق؟**  
**الإجابة:**  
- **استخدام `RepaintBoundary`** لمنع إعادة رسم الأجزاء غير المتغيرة في الواجهة.  
- **تجنب العمليات الثقيلة في `build()` واستبدالها بـ `FutureBuilder` أو `StreamBuilder`**.  
- **استخدام `CachedNetworkImage` للصور** بدلاً من تحميلها في كل مرة.  
- **تقليل استخدام الرسوم المتحركة المكثفة أو تعويضها بـ `Lottie` للرسوم الخفيفة**.  

---

## **📌 ثانيًا: التكامل مع APIs وقواعد البيانات Firebase / MySQL**  

#### **4. كيف يمكن استهلاك API في Flutter؟**  
**الإجابة:**  
1. أضف مكتبة `http` إلى `pubspec.yaml`:  
   ```yaml
   dependencies:
     http: latest_version
   ```
2. إرسال طلب HTTP باستخدام `http.get`:  
   ```dart
   import 'package:http/http.dart' as http;
   import 'dart:convert';

   Future<void> fetchData() async {
     final response = await http.get(Uri.parse('https://api.example.com/data'));
     if (response.statusCode == 200) {
       final data = jsonDecode(response.body);
       print(data);
     } else {
       print('Error: ${response.statusCode}');
     }
   }
   ```

---

#### **5. كيف يمكن التكامل مع Firebase في Flutter؟**  
**الإجابة:**  
1. أضف `firebase_core` و `cloud_firestore` إلى `pubspec.yaml`:  
   ```yaml
   dependencies:
     firebase_core: latest_version
     cloud_firestore: latest_version
   ```
2. قم بتهيئة Firebase في `main.dart`:  
   ```dart
   import 'package:firebase_core/firebase_core.dart';

   void main() async {
     WidgetsFlutterBinding.ensureInitialized();
     await Firebase.initializeApp();
     runApp(MyApp());
   }
   ```
3. إضافة أو قراءة بيانات من Firestore:  
   ```dart
   FirebaseFirestore.instance.collection('users').add({
     'name': 'Ahmed',
     'age': 25,
   });

   FirebaseFirestore.instance.collection('users').get().then((snapshot) {
     for (var doc in snapshot.docs) {
       print(doc.data());
     }
   });
   ```

---

#### **6. كيف يمكن الاتصال بـ MySQL في Flutter؟**  
**الإجابة:**  
- **استخدام PHP كوسيط بين Flutter و MySQL.**  
1. أنشئ سكربت `get_data.php` لاسترجاع البيانات:  
   ```php
   <?php
   $conn = new mysqli("localhost", "username", "password", "database");
   $result = $conn->query("SELECT * FROM users");
   $data = array();
   while ($row = $result->fetch_assoc()) {
       $data[] = $row;
   }
   echo json_encode($data);
   ?>
   ```
2. استدعاء الـ API في Flutter:  
   ```dart
   Future<void> fetchUsers() async {
     final response = await http.get(Uri.parse('https://example.com/get_data.php'));
     if (response.statusCode == 200) {
       List users = jsonDecode(response.body);
       print(users);
     }
   }
   ```

---

## **📌 ثالثًا: حل المشكلات التقنية وتحسين التطبيقات**  

#### **7. كيف يتم التعامل مع الأخطاء في Flutter؟**  
**الإجابة:**  
- **استخدام `try-catch` لمنع تعطل التطبيق عند حدوث خطأ:**  
  ```dart
  try {
    int result = 10 ~/ 0; // خطأ القسمة على صفر
  } catch (e, stackTrace) {
    print('حدث خطأ: $e');
  }
  ```
- **استخدام `FlutterError.onError` لتسجيل الأخطاء العامة:**  
  ```dart
  FlutterError.onError = (FlutterErrorDetails details) {
    print("Flutter Error: ${details.exception}");
  };
  ```

---

#### **8. كيف يمكن تتبع مشاكل الأداء وإصلاحها في Flutter؟**  
**الإجابة:**  
1. **استخدام Flutter DevTools** لمراقبة الأداء والذاكرة.  
2. **تفعيل `debugProfileBuildsEnabled` لمعرفة الـ widgets التي يتم إعادة بنائها كثيرًا:**  
   ```dart
   debugProfileBuildsEnabled = true;
   ```
3. **تحليل الأداء باستخدام `Timeline` في Dart Observatory.**  
4. **تقليل وقت تحميل الشاشة باستخدام `precacheImage`:**  
   ```dart
   precacheImage(AssetImage('assets/logo.png'), context);
   ```

---

#### **9. كيف يتم تحديث وتحسين التطبيقات بعد النشر؟**  
**الإجابة:**  
1. **استخدام Firebase Remote Config** لإجراء تحديثات بدون إعادة رفع التطبيق.  
2. **إصدار تحديثات منتظمة وتحليل البيانات باستخدام Firebase Analytics.**  
3. **إضافة إشعارات تحديث باستخدام `in_app_update`** لعرض تحديثات التطبيق.  
4. **استخدام `flutter_downloader` لتنزيل التحديثات الجديدة من السيرفر.**  

---

#### **10. كيف يمكن التعامل مع مشكلات التوافق بين الحزم المختلفة؟**  
**الإجابة:**  
1. **التأكد من استخدام إصدارات متوافقة في `pubspec.yaml`.**  
2. **استخدام `flutter pub upgrade` و `flutter pub outdated` لمعرفة التحديثات المتاحة.**  
3. **إذا كان هناك تضارب بين الحزم، يتم تجربة إصدار أقدم أو استخدام `dependency_overrides`.**  

---
 

