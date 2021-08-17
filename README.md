import 'package:flutter/material.dart';

void main() {
  {
    runApp(MaterialApp(
      home: Home(),
      debugShowCheckedModeBanner: false,
    ));
  }
}
class Home extends StatefulWidget {
  const Home({Key? key}) : super(key: key);

  @override
  _HomeState createState() => _HomeState();
}

class _HomeState extends State<Home> {
  bool _selecionarvalor = false;
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        centerTitle: true,
        title: Text(
          'Forms',


        ),
      ),
      body: SafeArea(
        child: Padding(
          padding: EdgeInsets.fromLTRB(5, 5, 5, 0),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.start,
            crossAxisAlignment: CrossAxisAlignment.center,
            children: [
              Row(
                children: [
                  Icon(
                    Icons.account_box_sharp

                  ),
                  Expanded(
                    child: TextFormField(
                      obscureText: false,
                      decoration: InputDecoration(
                        hintText: 'nome no cartão',

                      ),
                    ),
                  )
                ],
              ),
              Row(
                mainAxisAlignment: MainAxisAlignment.center,

                crossAxisAlignment: CrossAxisAlignment.center,

                children: [
                  Icon(
                    Icons.credit_card_outlined,
                    color: Colors.blueGrey,
                    size: 24,
                  ),
                  Expanded(
                    child: TextFormField(
                      obscureText: false,
                      decoration: InputDecoration(

                        hintText: 'número do cartão',

                      ),
                    ),
                  ),
                  Expanded(
                    child: TextFormField(
                      obscureText: false,
                      decoration: InputDecoration(
                        hintText: 'Cvv',
                      ),
                    ),
                  )
                ],
              ),
              Row(
                mainAxisAlignment: MainAxisAlignment.start,
                children: [
                  Icon(
                    Icons.settings_outlined,
                  ),
                ],
              ),
              Column(
                children: [
                  Row(
                    children: [
                      Icon(
                        Icons.location_pin,
                      ),
                      Expanded(
                        child: TextFormField(
                          obscureText: false,
                          decoration: InputDecoration(
                            hintText: 'CEP',
                          ),
                        ),
                      )
                    ],
                  ),
                  Row(
                    children: [
                      Icon(
                        Icons.business,
                        size: 24,
                      ),
                      Expanded(
                        child: TextFormField(
                          obscureText: false,
                          decoration: InputDecoration
                            (hintText: 'addres line'),
                        ),
                      )
                    ],
                  ),
                ],
              ),
              Row(
                children: [
                  Text(
                    'salvar informações para compras futuras',
                  ),
                  Checkbox(value: _selecionarvalor, onChanged: (_valorcheck){
                    setState(() {
                      if(_selecionarvalor)
                      {
                        _selecionarvalor = false;
                      }else{
                        _selecionarvalor = true;
                      }
                    });
                  }
                  ),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }
}
