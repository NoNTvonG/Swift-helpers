# Приклад використання `@StateObject`
Нижче наведений міні приклади як використати властивість в проекті.

---

 ```
class MyViewModel: ObservableObject {
    @Published var count: Int = 0
}

struct MyView: View {
    @StateObject var viewModel = MyViewModel()

    var body: some View {
        VStack {
            Text("Count: \(viewModel.count)")
            Button("Increment") {
                viewModel.count += 1
            }
        }
    }
}
 ```

У цьому прикладі ми створили екземпляр `MyViewModel` з `@StateObject`. Коли користувач натискає на кнопку "Increment", значення лічильника `count` в `MyViewModel` збільшується на 1, і нове значення відображається в `Text` віджеті. Оскільки `viewModel` є збереженим за допомогою `@StateObject`, його значення зберігається між перезавантаженнями віджета.