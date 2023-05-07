# Приклад використання `@Environment`
Нижче наведений міні приклади як використати властивість в проекті.

---

 ```
struct ContentView: View {
    @Environment(\.colorScheme) var colorScheme

    var body: some View {
        SubView(colorScheme: colorScheme)
    }
}

struct SubView: View {
    var colorScheme: ColorScheme

    var body: some View {
        // використовуємо colorScheme
    }
}
 ```

В цьому коді ми використовуємо `@Environment(\.colorScheme)`, щоб отримати значення теми додатку, яке потім передається в підвид `SubView`.

Існує багато вбудованих значень `@Environment`, таких як `colorScheme`, `layoutDirection`, `presentationMode`, `locale`, `calendar`, `timeZone` та інші. Ви також можете створювати свої власні значення `@Environment`, щоб передавати додаткові параметри в різні вю.