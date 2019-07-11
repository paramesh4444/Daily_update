# Daily_update


import 'package:flutter/material.dart';

void main()
{
  runApp(MyApp());
}

class MyApp extends StatefulWidget {
  @override
  State<StatefulWidget> createState() {
    // TODO: implement createState
    return MyAppState();
  }
}

class MyAppState extends State<MyApp> {
  int questionIndex = 0;

  void answerQuestion()
  {
    setState(() {
      questionIndex += 1;  
    });
    print(questionIndex);
  }

  @override
  Widget build(BuildContext context)
  {

    var questions = [
      'what\'s is your favorite color',
      'what\'s is your favorite animal',
    ];

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('MyApp'),
          backgroundColor: Colors.brown,
        ),
        body: Column(children: <Widget>[
          Text(questions[questionIndex]),
          RaisedButton(
            child: Text('Btn_1'),
            onPressed: answerQuestion,
          ),
          RaisedButton(
            child: Text('Btn_2'),
            onPressed: answerQuestion,
          ),
          RaisedButton(
            child: Text('Btn_3'),
            onPressed: answerQuestion,
          ),
        ],),
      ),
    );
  }
}
