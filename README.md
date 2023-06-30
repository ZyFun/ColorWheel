# ColorWheel

Цветовой круг, с помощью которого можно выбрать нужный цвет жестом, и присвоить его любому элементу.

Как использовать
```Swift
import ColorWheel

let colorWheel = ColorWheel() // Это обычная view, поэтому можно задать размеры любым способом
var panGestureRecognizer = UIPanGestureRecognizer(target: self, action: #selector(selectColor)

@objc private func selectColor(_ gestureRecognizer: UIPanGestureRecognizer) {
    let location = gestureRecognizer.location(in: colorView)
    let color = colorView.colorAtPoint(point: location)
    view.backgroundColor = color
}
```
