# Приклад використання `@ObservedObject`
Нижче наведений міні приклади як використати властивість в проекті.

---

 ```
 class MyModel: ObservableObject {
     @Published var name: String = ""
 }

 struct MyView: View {
     @ObservedObject var myModel = MyModel()

     var body: some View {
         TextField("Enter name", text: $myModel.name)
     }
 }
 ```
Тепер, коли ми вводимо текст у поле введення, значення властивості name в нашому екземплярі MyModel змінюється, а SwiftUI автоматично оновлює відображення, що використовують цей об'єкт.