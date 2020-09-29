Grave seu primeiro texto em Braille
=======================================



BrailleRapSP é uma máquina acionada por G-CODE, para estampar braille é necessário antes de tudo traduzir o texto em Braille.
Existem 2 soluções para traduzir Braille:
O aplicativo BrailleRap online https://crocsg.github.io/BrailleRap/
O aplicativo NatBraille  http://natbraille.free.fr 


Utilização do aplicativo BrailleRap
---------------------------------------

vá para https://crocsg.github.io/BrailleRap/

.. image :: ./IMG/braillerapapp.png
       :align: center
Digite seu texto e baixe o arquivo GCODE para a impressora

.. image :: ./IMG/braillerapapp_download.png
       :align: center

Para enviar o arquivo GCODE para a impressora, você pode usar um software como **cura** ou **pronterface** 



Configuração NatBraille
------------------------

Crie software no diretório do projeto NatBrailleTools

Nas opções gerais do NatBraille, use TbFr2007 para tabela Braille, codificação de documento em preto automatizado , codificação de documento em Braille Windows1252

.. image :: ./IMG/natbraille.png
       :align: center

Nas opções de relevo, use TbFr2007 para tabela braille para relevo
Habilitar opção usar um comando do sistema para estampagem
use o parâmetro java -jar d: \ usr \ home \ logger \ BrailleLogger.jar $ f | java -jar d: \ usr \ home \ logger \ gcodestreamer.jar COM4 250000 para comando de impressora.
Você precisa modificar o diretório executável e a referência da porta COM

.. image :: ./IMG/natbrailleembossig.png
       :align: center


Nas configurações da página, insira 31 e 26 como caractere por linha e linha por página

.. image :: ./IMG/natbraille_page.png
       :align: center

