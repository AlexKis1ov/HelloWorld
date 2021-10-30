# HelloWorld
#### При нажатии на кнопку текст "Hello World" скрывается, а при повторном нажатии появляется.


@IBOutlet var helloWorldLabel: UILabel!       -   свойства(Outlet)
    @IBOutlet var showTextButton: UIButton!   - свойства
    
    override func viewDidLoad() {              - шаблоны
        super.viewDidLoad()                      
        helloWorldLabel.isHidden = true           - этот метод делает так чтобы текст скрылся (чтобы надпись скрылась)  
        showTextButton.layer.cornerRadius = 10      - этот метод скругляет края кнопки
    }


    @IBAction func ShowTextPressed() {       -  методы (action)
        helloWorldLabel.isHidden.toggle()    - этот метод меняет значение логической переменной на противопложенное (т.e делает чтобы надпись появилась)
        
        if helloWorldLabel.isHidden {                                - сдесь созается условие которое будет действовать при нажатии на кнопку
            showTextButton.setTitle("Show text", for: .normal)
        } else {
            showTextButton.setTitle("Hide text", for: .normal)
        }
            
    }
}
 
![Снимок экрана 2021-10-30 в 20 15 54](https://user-images.githubusercontent.com/88490455/139542742-bab99e11-a380-4ce7-adbf-8b502389870d.png)
