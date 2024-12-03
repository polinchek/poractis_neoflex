Установка Flutter

Установка  VS Code

Установка  androidstudio

Установка расширения
![image](https://github.com/user-attachments/assets/175cf672-e1e0-4c30-80d1-d68db33f15de)

Проверка flutter doctor
![image](https://github.com/user-attachments/assets/3580008d-ce0f-41eb-801f-f411834e7574)

Итог:

Запуск в браузере:

![image](https://github.com/user-attachments/assets/389ef555-e50c-466c-83cf-c9fdda82437e)

Запуск на эмуляторе:

![image](https://github.com/user-attachments/assets/47ca3c97-5a6f-4a44-aa77-d4141becfbca)

      body: MyStatelessWidget(color: const Color.fromARGB(255, 211, 158, 235)),
      floatingActionButton:
          IconButton(onPressed: () {}, icon: const Icon(Icons.add)),
    ),
  ));
}

class MyStatelessWidget extends StatefulWidget {
  const MyStatelessWidget({super.key, required this.color});

  final Color color;

  @override
  State<MyStatelessWidget> createState() => _MyStatelessWidgetState();
}

class _MyStatelessWidgetState extends State<MyStatelessWidget> {
  late Color color;

  @override
  void initState() {
    super.initState();
    color = widget.color;
  }

  @override
  Widget build(BuildContext context) {
    return GestureDetector(
      onTap: () {
        setState(() {
          color = const Color.fromARGB(
              255, 123, 182, 221); 
        });

Приложение до смены цвета

  ![image](https://github.com/user-attachments/assets/bcb53563-72fb-46bc-8397-4552b99b1f1a)
        
  После смены цвета
  
![image](https://github.com/user-attachments/assets/1453756e-867e-4c53-bd66-aa4e6dba8fcb)

 child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Text(
                'Текст',
                style: TextStyle(fontSize: _fontSize),
              ),
              const SizedBox(height: 20),
              Column(
                // Изменили Row на Column
                children: [
                  ElevatedButton(
                    onPressed: _increaseFontSize,
                    child: const Text('Увеличить'),
                  ),
                  const SizedBox(height: 10), // Добавили отступ между кнопками
                  ElevatedButton(
                    onPressed: _decreaseFontSize,
                    child: const Text('Уменьшить'),
                  ),

  Уменьшаем текст

  ![image](https://github.com/user-attachments/assets/0f4f15f3-42a9-4dd3-9424-d66f3d2bf085)

Увеличиваем текст

![image](https://github.com/user-attachments/assets/24ef2679-8232-4f87-acec-65db83f8e617)

class ScreenA extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('Screen A')),
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            Navigator.pushNamed(context, '/screenB');
          },
          child: Text('Go to Screen B'),
        ),
      ),
    );
  }
}

class ScreenB extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('Screen B')),
      body: Center(
        child: ElevatedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child: Text('Back to Screen A'),
        ),

Экран А

![image](https://github.com/user-attachments/assets/10048c63-4303-486b-b3be-0dc33c9b2f4b)

Переход на экран В

![image](https://github.com/user-attachments/assets/a0596f5c-3b70-4304-a5a7-0f659b1488d3)

  

        
