# memoIT
<p>
<img src="https://img.shields.io/badge/Swift-5.2-orange?logo=swift">
<img src="https://img.shields.io/badge/Xcode-13.2.1-blue?logo=xcode">
<img src="https://img.shields.io/badge/iOS-15.2-black?logo=apple">
</p>

### π κ·Έλκ·Έλ κΈ°λ‘ν΄μ

> μλλ‘μ΄λμμ μμ΄ν°μΌλ‘ λμ΄μ€λ©΄μ μλ μ¬μ©νλλλ‘ κ°λ¨νκ² λ©λͺ¨ μ±μ μ¬μ©νλ € 
νμκ³ , μ΄μ λμ μ±μ λνΌμμ μ€μ€λ‘ κ°λ¨νκ² λ§λ€μ΄ μ¬μ©ν  μ μμΌλ¦¬λΌ μκ°νλ€. κ·Έλμ
λ°μ΄ν°λ₯Ό νμ΄μ΄λ² μ΄μ€λ₯Ό ν΅ν΄μ λ°μμ€λ μ νλ¦¬μΌμ΄μ λ§κ³ λ, Core Dataλ₯Ό νμ©ν΄ λ‘μ»¬μμ λ°μ΄ν°λ₯Ό
λΆλ¬μ λ§λ€μ΄λ³΄κΈ°λ μ’μ κ²μ΄λΌ μκ°νμλ€.

memoITμ postITμμ κ·Έ μ΄λ¦μ λ°μμ΅λλ€. ν¬μ€νΈμμ΄ μκ°λ  λλ§λ€
λ°λ‘ κΈ°λ‘ν  μ μλ κ²μ²λΌ λ©λͺ¨μμ μμ΄ν°μμ μκ°λ μ , νΉμ κΈ°μ΅ν΄λμ΄μΌ ν 
κ²λ€μ μ±μ ν΅ν΄μ λ°λ‘ κΈ°λ‘ν΄ λ μ μλ μ νλ¦¬μΌμ΄μ μλλ€.

### κ΅¬ν κΈ°λ₯
* μμ±ν λ©λͺ¨ λͺ©λ‘μ λ³Ό μ μκ² νλ€.
* λ©λͺ¨ λͺ©λ‘ μΌμͺ½ μλ¨μ λ²νΌμ ν΅ν΄ **λ©λͺ¨λ₯Ό μΆκ°**ν  μ μλ€.
* λ©λͺ¨μ λͺ©λ‘μ λλ¬ **λ©λͺ¨λ₯Ό μ­μ νκ±°λ μμ **ν  μ μλ€.

|β λ©λͺ¨ μμ±|β λ©λͺ¨ μ­μ |β λ©λͺ¨ μμ |
|:---:|:---:|:---:|
|<img src="https://user-images.githubusercontent.com/76734067/162631647-24e4cec7-ed36-404b-ba35-777ff3004fd7.gif">|<img src="https://user-images.githubusercontent.com/76734067/162631654-5ee4b11c-9b9b-4ffc-b9f9-3f082ffe2b58.gif">|<img src="https://user-images.githubusercontent.com/76734067/162631656-1e201097-cc14-49eb-a3be-11c3dd2ab3cb.gif">|

## λ¦¬ν©ν λ§
μλ¦Όμ΄ λ°μν λλ§λ€ μλ‘μ΄ μλ¦Όμ λ§λ€κ³ , μλ¦Όμ μ‘μμ μΆκ°νλ λ°λ³΅μ μΈ μ½λκ° λ°μνμ¬ μλ¦Όμ μμ±νκ³  μ€νμμΌμ£Όλ
ν¨μλ₯Ό μΆκ°νμμ΅λλ€.
```swift
func activateDefaultAlert(title: String, message: String, alertAction: UIAlertAction? = nil) {
    let alert = UIAlertController(title: title, message: message, preferredStyle: .alert)
    if let action = alertAction {
        alert.addAction(action)
    }
    self.present(alert, animated: true, completion: nil)
}
```

μ¬μ©μμ
```swift
activateDefaultAlert(title: "μ λͺ©μ΄ μλ ₯λμ§ μμμ΅λλ€",
                     message: "μ λͺ©μ μλ ₯ν΄μ£ΌμΈμ",
                     alertAction: okButton)
```

## π¨λ²κ·Έ μμ 
μλ¬΄ λ©λͺ¨λ μλ ₯νμ§ μκ³  `Save`λ²νΌμ λλ μ λ, λ©λͺ¨ λͺ©λ‘μΌλ‘ λμκ°λ©΄ λ©λͺ¨κ° μ‘΄μ¬νλ λ²κ·Έλ₯Ό ν΄κ²°νμμ΅λλ€.<br>
λ©λͺ¨μ νμ΄νμ΄λ λ΄μ©μ΄ λΉμ΄μλμ§ νμΈνκΈ° μ΄μ μ `Memo(context: self.context)`λ₯Ό ν΅ν΄μ `Memo`λ°μ΄ν°λ₯Ό λ§λ€μκ³ 
λ°μ΄ν°κ° μ€μ λ‘ λ‘μ»¬μ μ μ₯λμ§ μμλλΌλ, μμ±λ λ°μ΄ν°μ΄κΈ° λλ¬Έμ fetchνλκ³Όμ μμ ν΄λΉλ°μ΄ν°λ₯Ό ν¬ν¨μν¨κ²μΌλ‘ λ³΄μλλ€.
**μμ ν μ λͺ©μ΄λ λ΄μ©μ΄ λΉμ΄μλ κ²μ νμΈλ νμ κ°μ²΄λ₯Ό μμ±ν΄μ λ²κ·Έλ₯Ό μμ νμμ΅λλ€.**
```swift
@IBAction func saveButtonPressed(_ sender: UIBarButtonItem) {
    //μλλ μ΄κ³³μ μμλ newMemoκ°μ²΄ μμ±μ
    let okButton = UIAlertAction(title: "OK", style: .default)
    
    if memoTitleTextField.text == "" {
        activateDefaultAlert(title: "μ λͺ©μ΄ μλ ₯λμ§ μμμ΅λλ€",
                                message: "μ λͺ©μ μλ ₯ν΄μ£ΌμΈμ",
                                alertAction: okButton)
    } else if memoBodyTextView.text == "" {
        activateDefaultAlert(title: "λ΄μ©μ΄ μλ ₯λμ§ μμμ΅λλ€",
                                message: "λ΄μ©μ μλ ₯ν΄μ£ΌμΈμ",
                                alertAction: okButton)
    } else {
        //μ΄κ³³μΌλ‘ μ?κ²Όμ΅λλ€.
        let newMemo = Memo(context: self.context)
        newMemo.title = memoTitleTextField.text
        newMemo.body = memoBodyTextView.text
        newMemo.date = Date()
        do {
            try! self.context.save()
            print("μ μ₯λμμ΅λλ€~")
        } catch {
            print(error)
        }
        self.fetchMemo()
        navigationController?.popViewController(animated: true)
    }
}
```
|β λ²κ·Έ μμ  μ |β­οΈ λ²κ·Έ μμ  ν|
|:---:|:---:|
|<img src="https://user-images.githubusercontent.com/76734067/162803538-866522d8-a77e-4107-bdb9-afe4f16366e8.gif" width="50%">|<img src="https://user-images.githubusercontent.com/76734067/162804329-ddcb14c1-53e6-4dbe-8763-1db9225448ae.gif" width="50%">|