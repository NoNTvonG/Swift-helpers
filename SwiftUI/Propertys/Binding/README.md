# Приклад використання `@Binding`
Нижче наведений міні приклади як використати властивість в проекті.

---

 ```
struct ParentView: View {
    @State var text = "Hello, World!"

    var body: some View {
        ChildView(text: $text)
    }
}

struct ChildView: View {
    @Binding var text: String

    var body: some View {
        TextField("Enter text", text: $text)
    }
}
 ```

У цьому прикладі зміна тексту в `TextField` в дочірньому view `ChildView` буде автоматично відображатись в батьківському view `ParentView`, завдяки використанню `@Binding`.