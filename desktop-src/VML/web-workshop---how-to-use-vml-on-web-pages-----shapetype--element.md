---
title: Usando o elemento ShapeType
description: Usando o elemento ShapeType
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web Workshop, elemento ShapeType
- Criando páginas da Web, elemento ShapeType
- Linguagem VML (VML), elemento ShapeType
- VML (linguagem VML), elemento ShapeType
- gráficos vetoriais, elemento ShapeType
- elemento ShapeType
- Elementos de VML, formatype
- Formas de VML, elemento ShapeType
- Linguagem VML (VML), definindo formas usadas com frequência
- VML (linguagem VML), definindo formas usadas com frequência
- gráficos vetoriais, definição de formas usadas com frequência
- definindo formas usadas com frequência
- Formas de VML, definindo frequentemente usadas
- Linguagem VML (VML), instanciando cópias de formas
- VML (linguagem VML), instanciando cópias de formas
- gráficos vetoriais, instanciando cópias de formas
- Criando uma instância de cópias de formas
- Formas de VML, instanciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454289"
---
# <a name="using-the-shapetype-element"></a>Usando o elemento ShapeType

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Neste tópico, Ilustraremos como usar o `<shapetype>` elemento para definir suas próprias formas usadas com frequência e, em seguida, instanciar ou criar formas a partir de ShapeType.

Se você quisesse desenhar muitas formas que tenham Propriedades iguais ou semelhantes, seria entediante se você tivesse que digitar repetidamente os mesmos atributos de propriedade para cada forma. A VML fornece o `<shapetype>` elemento para que você possa definir um protótipo de uma forma. Em seguida, você pode usar o `<shape>` elemento para instanciar muitas cópias de formas do mesmo ShapeType.

Você pode seguir as três etapas para definir um ShapeType e, em seguida, instanciar uma forma a partir de ShapeType:

1.  Digite um `<shapetype>` elemento e dê a ele um nome especificando o atributo de ID.
2.  Descreva o tipo de forma usando seus atributos de propriedade ou subelementos.
3.  Crie uma instância de uma forma digitando um `<shape>` elemento e consulte o atributo Type da forma para o atributo ID de ShapeType.

Por exemplo, você digita as linhas a seguir para criar um tipo de forma chamado "myShape":


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Em seguida, você altera o tipo de forma definindo alguns atributos de propriedade, como `fillcolor="red" strokecolor="blue"` . Ou, você pode usar subelementos dentro de ShapeType, como `<path>` , `<fill>` (Falaremos `<stroke>` sobre esses subelementos nos tópicos posteriores).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Em seguida, você cria uma instância de uma forma de forma "myforma" especificando `type="#MyShape"` , conforme mostrado na representação de VML a seguir. Essa forma herda todas as propriedades da forma "myFormat" e é exibida dentro de sua caixa de conteúdo em um tamanho de 100 por 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Você pode criar uma instância de outra forma com base no tipo de forma "myFormat" especificando `type="#MyShape"` e substitui algumas propriedades, como `fillcolor="maroon"` , conforme mostrado na representação de VML a seguir. Essa forma herda todas as propriedades da forma "myShape", exceto da propriedade FillColor, e é exibida dentro de sua caixa que contém um tamanho de 70 por 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Aqui está a representação de VML completa para o exemplo anterior:

![\-1.gif type1 (477 bytes)](images/type1-1.gif)![\-2.gif type1 (471 bytes)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





Como você aprendeu, quando uma forma é instanciada de um ShapeType, ela herda todos os atributos de Propriedade do ShapeType. Você pode substituir alguns ou todos os atributos herdados redefinindo atributos dentro do `<shape>` elemento. Lembre-se de que a herança é apenas um nível. Isso ocorre porque apenas um `<shape>` elemento pode referenciar um `<shapetype>` elemento. Um `<shapetype>` elemento não pode fazer referência A outro `<shapetype>` elemento.

Além disso, um ShapeType não pertence a nenhum grupo. Portanto, o `<shapetype>` elemento pode aparecer sozinha ou dentro de um `<group>` elemento. Você pode ter muitas formas dentro de grupos diferentes que referenciam o mesmo ShapeType. Se um ShapeType aparecer dentro de um grupo, uma forma que mora em outro grupo ainda poderá fazer referência a esse ShapeType.

Por exemplo, na seguinte representação de VML, Rect1 e Rect2 estão em GroupA e Rect3 está em GroupB. Todos os três retângulos são instanciados a partir de ShapeType de myFormat.


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



Para obter mais informações sobre esse elemento, consulte a [especificação da VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 