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
 
![Снимок экрана 2021-10-30 в 20 15 54](https://user-images.githubusercontent.com/88490455/139542742-bab99e11-a380-4ce7-adbf-8b502389870d.png) ![Снимок экрана 2021-10-30 в 20 16 36](https://user-images.githubusercontent.com/88490455/139542797-955c5d7f-0a43-440c-8989-e9705a7887d1.png)


( метод чтобы квадрат седалать кругом redLight.layer.cornerRadius = redLight.frame.width/2 )
