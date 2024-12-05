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

  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Color Swapper'),
        ),
        body: Center(
          child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              Row(
                mainAxisAlignment: MainAxisAlignment.center, 
                children: <Widget>[
                  SizedBox(
                    width: 100,
                    height: 100,
                    child: ColoredBox(color: _color1),
                  ),
                  const SizedBox(width: 20), 
                  SizedBox(
                    width: 100,
                    height: 100,
                    child: ColoredBox(color: _color2),
                  ),
                ],
              ),
              const SizedBox(height: 20),
              ElevatedButton(
                onPressed: _swapColors,
                child: const Text('Swap Colors')
                
![image](https://github.com/user-attachments/assets/fdf7b8a5-3a7d-4d75-b1a8-af3ad076698d)

primarySwatch: Colors.deepPurple, // Set a primary color for the app
      ),
      home: Scaffold(
        appBar: AppBar(title: const Text('Colorful Widget Showcase')),
        body: SingleChildScrollView(
          padding: const EdgeInsets.all(16.0),
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.stretch,
            children: [
              // Row with Expanded widgets and text
              Row(
                children: [
                  Expanded(
                    child: Container(
                      color: Colors.tealAccent,
                      padding: const EdgeInsets.all(16.0),
                      child: const Center(
                          child: Text('Expanded Widget 1',
                              style: TextStyle(
                                  fontSize: 18, fontWeight: FontWeight.bold))),
                    ),
                  ),
                  Expanded(
                    child: Container(
                      color: Colors.lightBlueAccent,
                      padding: const EdgeInsets.all(16.0),
                      child: const Center(
                          child: Text('Expanded Widget 2',
                              style: TextStyle(
                                  fontSize: 18, fontWeight: FontWeight.bold))),
                    ),
                  ),
                ],
              ),
              const SizedBox(height: 20),
              
 Container(
                color: Colors.amberAccent,
                padding: const EdgeInsets.all(10.0),
                child: Align(
                  alignment: Alignment.centerRight,
                  child: const Text('Aligned Text',
                      style:
                          TextStyle(fontSize: 20, fontWeight: FontWeight.w500)),
                ),
              ),
              const SizedBox(height: 20),

   Center(
                child: Container(
                  width: 150,
                  height: 100,
                  decoration: const BoxDecoration(
                    gradient: LinearGradient(
                      colors: [Colors.pink, Colors.purple],
                    ),
                  ),
                  child: const Center(
                      child: Text('Centered Container',
                          style: TextStyle(fontSize: 16, color: Colors.white))),
                ),
              ),
              const SizedBox(height: 20),

Stack(
                alignment: Alignment.center,
                children: [
                  Container(
                    width: 120,
                    height: 120,
                    decoration: BoxDecoration(
                      color: Colors.deepOrange,
                      borderRadius: BorderRadius.circular(10),
                      boxShadow: [
                        BoxShadow(
                          color: Colors.grey.withOpacity(0.5),
                          spreadRadius: 2,
                          blurRadius: 5,
                          offset:
                              const Offset(0, 3), // changes position of shadow
                        ),
                      ],
                    ),
                  ),
                  const Text('Stacked Text',
                      style: TextStyle(fontSize: 20, color: Colors.white)),
                ],
              ),
              const SizedBox(height: 20),

 Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  const Padding(
                    padding: EdgeInsets.all(8.0),
                    child: Text('List of Items',
                        style: TextStyle(
                            fontSize: 18, fontWeight: FontWeight.bold)),
                  ),
                  SizedBox(
                    height: 200,
                    child: ListView.builder(
                      itemCount: 5,
                      itemBuilder: (context, index) {
                        return ListTile(
                          leading: CircleAvatar(
                              backgroundColor: Colors
                                  .primaries[index % Colors.primaries.length]),
                          title: Text('Item ${index + 1}')

![image](https://github.com/user-attachments/assets/d5a08f6e-f659-4525-a86a-68643759b5eb)

Передача данных с onGenerateRoute.

![image](https://github.com/user-attachments/assets/c77a74b7-ab70-4f12-a01c-b7790c292e77)

![image](https://github.com/user-attachments/assets/511930f8-f7e8-4d41-85e7-beebed02e58b)

 TextField(
              decoration: InputDecoration(
                labelText: 'TextField',
                hintText: 'Enter text here',
                border: OutlineInputBorder(),
              ),
            ),
            SizedBox(height: 16.0),
            TextFormField(
              decoration: InputDecoration(
                labelText: 'TextForm',
                hintText: 'Enter text ',
                border: OutlineInputBorder(),
              )

![image](https://github.com/user-attachments/assets/65bdee15-f6ab-464e-81b8-647fad13b3dd)

 @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text("setState Example")),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text('Counter:', style: TextStyle(fontSize: 20)),
            Text('$_counter', style: TextStyle(fontSize: 40)),
            ElevatedButton(
              onPressed: _incrementCounter,
              child: Text("+1"),
            ),


![image](https://github.com/user-attachments/assets/8346f657-dfbb-47d7-9def-49438fe464a4)

![image](https://github.com/user-attachments/assets/4326dbb5-6b03-4e50-9973-7fd4ba4bab6a)


  @override
  Stream<CounterState> mapEventToState(CounterEvent event) async* {
    if (event is IncrementCounter) {
      yield CounterChanged(counterValue: state.counterValue + 1);
    } else if (event is DecrementCounter) {
    yield CounterChanged(counterValue: state.counterValue - 1);
    }

    
class IncrementCounter extends CounterEvent {} 

class DecrementCounter extends CounterEvent {}  
abstract class CounterState {
  final int counterValue;
  CounterState({required this.counterValue});
}

class CounterInitial extends CounterState {
  CounterInitial({required int counterValue})
      : super(counterValue: counterValue);
}

class CounterChanged extends CounterState {
  CounterChanged({required int counterValue})
      : super(counterValue: counterValue);
}

  ![image](https://github.com/user-attachments/assets/4268117b-d741-4026-b83b-5c71a9a8bcee)

    @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Shared Preferences Demo'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            Text(
              'Counter value: ${_counter ?? 'No data'}',
              style: Theme.of(context).textTheme.headlineSmall,
            ),
            Text(
              'Last action: $_action',
              style: Theme.of(context).textTheme.bodyLarge,
            ),
            SizedBox(height: 20),
            ElevatedButton(
              onPressed: _saveData,
              child: Text('Increment Counter'),
            ),
            ElevatedButton(
              onPressed: _clearData,
              child: Text('Clear Data'),
              style: ElevatedButton.styleFrom(backgroundColor: Colors.red),
            ),

   ![image](https://github.com/user-attachments/assets/92005394-7f98-4dde-ba7b-c89374759aa1)

![image](https://github.com/user-attachments/assets/ef6be8f1-483c-45ff-9c5f-40fab36c8d37)

   class CounterRepository {
  static const _counterKey = 'counter';

  Future<int> getCounter() async {
    final prefs = await SharedPreferences.getInstance();
    return prefs.getInt(_counterKey) ?? 0;
  }

  Future<void> setCounter(int value) async {
    final prefs = await SharedPreferences.getInstance();
    prefs.setInt(_counterKey, value);

    class CounterUseCase {
 final CounterRepository repository;

 CounterUseCase(this.repository);

 Future<int> getCounter() {
   return repository.getCounter();
 }

 Future<void> incrementCounter() async {
   final currentValue = await repository.getCounter();
   await repository.setCounter(currentValue + 1);
 }

 Future<void> decrementCounter() async {
   final currentValue = await repository.getCounter();
   await repository.setCounter(currentValue - 1);

   Future<void> _loadCounter() async {
    final counterValue = await _counterUseCase.getCounter();
    setState(() {
      _counter = counterValue;
    });
  }

  // Увеличение счетчика
  Future<void> _increment() async {
    await _counterUseCase.incrementCounter();
    _loadCounter(); // Обновление UI
  }

![image](https://github.com/user-attachments/assets/c8b40080-e952-4da2-b02b-0ab9dcb5c9f6)

 



        
