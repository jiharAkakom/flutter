# Basic - flutter
## STEP 1
~~~dart
import 'package:flutter/material.dart';
void main(){
runApp(
  new Container(
    decoration: new BoxDecoration(color: Colors.blueAccent),
    child: new Center(
      child: new Text("Hello jihar")
    )
  )
);
}
~~~
![Gambar 1](Image/1.png)

## STEP 2
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()                           //new
    )
  );
}
// all of code bellow is new
class MyStatelessWidget extends StatelessWidget{               
    @override                                                  
    Widget build(BuildContext context){                        
      return new Scaffold(                                     
        appBar: new AppBar(title: new Text("Kancio"))        
      );        
    }           
}               
~~~
![Gambar 1](Image/2.png)

## Step 3
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()
    )
  );
}

class MyStatelessWidget extends StatelessWidget{
    @override
    Widget build(BuildContext context){
      return new Scaffold(
        appBar: new AppBar(title: new Text("Kancio")),
        body: new Container(                              //new
          child:new Column(                               //new
            children: <Widget>[                           //new
              new Text("Hello"),                          //new
              new Text("My name is Jihar Al Gifari"),     //new
              new Text("I am a man"),                     //new
            ],  //new
          ),  //new
        )  //new
      );
    }
}
~~~

![Gambar 1](Image/3.png)

## Step 4 add card
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()
    )
  );
}

class MyStatelessWidget extends StatelessWidget{
    @override
    Widget build(BuildContext context){
      return new Scaffold(
        appBar: new AppBar(title: new Text("Kancio")),
        body: new Container(
          child:new Column(
            children: <Widget>[
              new MyLove(),                             //new
              new MyLove(),                             //new
              new MyLove(),                             //new
            ],
          ),
        )
      );
    }
}

// all of code bellow is new
class MyLove extends StatelessWidget {
  MyLove({this.title, this.icon});
  final Widget title;
  final Widget icon;

  @override
  Widget build(BuildContext context){
    return new Container(
      child: new Card(
        child: new Column(
          children: <Widget>[
            new Text("I like learn go and flutter"),
            new Icon(Icons.favorite)
          ],
        ),
      ),
    );
  }
}
~~~
![Gambar 1](Image/4.png)

## Step 5
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()
    )
  );
}

class MyStatelessWidget extends StatelessWidget{
    @override
    Widget build(BuildContext context){
      return new Scaffold(
        appBar: new AppBar(title: new Text("Kancio")),
        body: new Container(
          child:new Column(
            crossAxisAlignment: CrossAxisAlignment. stretch,       // new
            children: <Widget>[
              new MyLove(),
              new MyLove(),                                        // new
              new MyLove(),                                        // new
            ],
          ),
        )
      );
    }
}

class MyLove extends StatelessWidget {
  MyLove({this.title, this.icon});
  final Widget title;
  final Widget icon;

  @override
  Widget build(BuildContext context){
    return new Container(
      child: new Card(
        child: new Column(
          children: <Widget>[
            new Text("I like learn go and flutter"),
            new Icon(Icons.favorite)
          ],
        ),
      ),
    );
  }
}
~~~
![Gambar 1](Image/5.png)

## Step 6
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()
    )
  );
}

class MyStatelessWidget extends StatelessWidget{
    @override
    Widget build(BuildContext context){
      return new Scaffold(
        appBar: new AppBar(title: new Text("Kancio")),
        body: new Container(
          child:new Column(
            crossAxisAlignment: CrossAxisAlignment. stretch,
            children: <Widget>[
              new MyLove(
                title: new Text("I love golang"),
                icon: new Icon(Icons.favorite),
              ),                                              //changed
              new MyLove(
                title: new Text("I love Islam"),
                icon: new Icon(Icons.favorite_border),
              ),                                              //changed
              new MyLove(
                title: new Text("I love Muhammad SAW"),
                icon: new Icon(Icons.link),
              ),                                              //changed
            ],
          ),
        )
      );
    }
}

class MyLove extends StatelessWidget {
  MyLove({this.title, this.icon});
  final Widget title;
  final Widget icon;

  @override
  Widget build(BuildContext context){
    return new Container(
      child: new Card(
        child: new Column(
          children: <Widget>[
            this.title,             // edit
            this.icon,              // edit
          ],
        ),
      ),
    );
  }
}
~~~
![Gambar 1](Image/6.png)

## Step 7 Add Padding
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()
    )
  );
}

class MyStatelessWidget extends StatelessWidget{
    @override
    Widget build(BuildContext context){
      return new Scaffold(
        appBar: new AppBar(title: new Text("Kancio")),
        body: new Container(
          padding:new EdgeInsets.all(10.0) , // new
          child:new Column(
            crossAxisAlignment: CrossAxisAlignment. stretch,
            children: <Widget>[
              new MyLove(
                title: new Text("I love golang"),
                icon: new Icon(Icons.favorite),
              ),
              new MyLove(
                title: new Text("I love Islam"),
                icon: new Icon(Icons.favorite_border),
              ),
              new MyLove(
                title: new Text("I love Muhammad SAW"),
                icon: new Icon(Icons.link),
              ),
            ],
          ),
        )
      );
    }
}

class MyLove extends StatelessWidget {
  MyLove({this.title, this.icon});
  final Widget title;
  final Widget icon;

  @override
  Widget build(BuildContext context){
    return new Container(
      padding: new EdgeInsets.only(bottom: 20.0),  // new
      child: new Card(
        child: new Column(
          children: <Widget>[
            this.title,
            this.icon,
          ],
        ),
      ),
    );
  }
}
~~~
![Gambar 1](Image/7.png)

## Step 8 Add padding in the padding, and Size for icons
~~~dart
import 'package:flutter/material.dart';

void main(){
  runApp(
    new MaterialApp(
      home: new MyStatelessWidget()
    )
  );
}

class MyStatelessWidget extends StatelessWidget{
    @override
    Widget build(BuildContext context){
      return new Scaffold(
        appBar: new AppBar(title: new Text("Kancio")),
        body: new Container(
          padding:new EdgeInsets.all(10.0) ,
          child:new Column(
            crossAxisAlignment: CrossAxisAlignment. stretch,
            children: <Widget>[
              new MyLove(
                title: new Text("I love golang"),
                icon: new Icon(Icons.favorite, size:60.0),        //edit size
              ),
              new MyLove(
                title: new Text("I love Islam"),
                icon: new Icon(Icons.favorite_border, size:60.0),   //edit size
              ),
              new MyLove(
                title: new Text("I love Muhammad SAW"),
                icon: new Icon(Icons.link, size:60.0),          //edit size
              ),
            ],
          ),
        )
      );
    }
}

class MyLove extends StatelessWidget {
  MyLove({this.title, this.icon});
  final Widget title;
  final Widget icon;

  @override
  Widget build(BuildContext context){
    return new Container(
      padding: new EdgeInsets.only(bottom: 20.0),
      child: new Card(
        child: new Container(                     //new
          padding: new EdgeInsets.all(15.0),      //new
          child: new Column(
            children: <Widget>[
              this.title,
              this.icon,
            ],
          ),
        )
      ),
    );
  }
}
~~~
![Gambar 1](Image/8.png)

## Step 9 add color icon
~~~dart
  new MyLove(
    title: new Text("I love golang"),
    icon: new Icon(Icons.favorite, size:60.0, color: Colors.redAccent),
),
~~~
![Gambar 1](Image/9.png)

## Step 10 Font Size
~~~dart
title: new Text("I love Muhammad SAW",
    style: new TextStyle(
    fontSize: 20.0
    ),
),
~~~
![Gambar 1](Image/10.png)
