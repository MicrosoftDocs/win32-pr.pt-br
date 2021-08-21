---
title: Usando o elemento Shapetype
description: Usando o elemento Shapetype
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Workshop da Web, elemento shapetype
- projetando páginas da Web, elemento shapetype
- linguagem VML (VML), elemento shapetype
- Elemento VML (linguagem VML),shapetype
- gráficos vetoriais, elemento shapetype
- Elemento shapetype
- Elementos VML, shapetype
- Formas VML, elemento shapetype
- linguagem VML (VML), definindo formas usadas com frequência
- VML (linguagem VML), definindo formas usadas com frequência
- gráficos vetoriais, definindo formas usadas com frequência
- definindo formas usadas com frequência
- Formas VML, definindo as usadas com frequência
- linguagem VML (VML), instando cópias de formas
- VML (linguagem VML), instando cópias de formas
- gráficos vetoriais, instando cópias de formas
- instando cópias de formas
- Formas VML, instando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d815d9f5f911e1a34d558496881ae606819d328a501c635ff463a84f2926ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512637"
---
# <a name="using-the-shapetype-element"></a>Usando o elemento Shapetype

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Neste tópico, ilustramos como usar o elemento para definir suas próprias formas usadas com frequência e, em seguida, criar ou criar formas do `<shapetype>` tipo de forma.

Se você quisesse desenhar muitas formas que têm as mesmas propriedades ou propriedades semelhantes, seria entediante se você tivesse que digitar repetidamente os mesmos atributos de propriedade para cada forma. O VML fornece `<shapetype>` o elemento para que você possa definir um protótipo de uma forma. Em seguida, você pode usar `<shape>` o elemento para insinuar muitas cópias de formas do mesmo tipo de forma.

Você pode seguir as três etapas para definir um tipo de forma e, em seguida, insinuar uma forma do tipo de forma:

1.  Digite um `<shapetype>` elemento e dê a ele um nome especificando o atributo id.
2.  Descreva o tipo de forma usando seus atributos de propriedade ou subconjunto.
3.  Insinue uma forma digitando um elemento e consulte o atributo de tipo da forma para o atributo `<shape>` id do tipo de forma.

Por exemplo, digite as seguintes linhas para criar um tipo de forma chamado "MyShape":


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



Em seguida, altere o tipo de forma definindo alguns atributos de propriedade, como `fillcolor="red" strokecolor="blue"` . Ou você pode usar subconjunto dentro do tipo de forma, como , , (vamos falar sobre esses `<path>` `<fill>` `<stroke>` subconjunto em tópicos posteriores).


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



Em seguida, você insinuou uma forma do tipo de forma "MyShape" especificando , conforme mostrado na representação VML a `type="#MyShape"` seguir. Essa forma herda todas as propriedades do tipo de forma "MyShape" e é exibida dentro de sua caixa de contenção com um tamanho de 100 por 80.


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



Você pode insinuar outra forma do tipo de forma "MyShape" especificando e substituindo algumas propriedades, como , conforme mostrado na representação VML a `type="#MyShape"` `fillcolor="maroon"` seguir. Essa forma herda todas as propriedades do tipo de forma "MyShape", exceto a propriedade fillcolor, e é exibida dentro de sua caixa de contenção com um tamanho de 70 por 90.


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



Aqui está a representação de VML completa para o exemplo anterior:

![type1 \-1.gif (477 bytes)](images/type1-1.gif)![type1 \-2.gif (471 bytes)](images/type1-2.gif)


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





Como você aprendeu, quando uma forma é instautada de um tipo de forma, ela herda todos os atributos de propriedade do tipo de forma. Você pode substituir alguns ou todos os atributos herdados redefinindo atributos dentro do `<shape>` elemento . Esteja ciente de que a herança é apenas um nível. Isso porque apenas um `<shape>` elemento pode referenciar um `<shapetype>` elemento. Um `<shapetype>` elemento não pode referenciar outro `<shapetype>` elemento.

Além disso, um tipo de forma não pertence a nenhum grupo. Portanto, o `<shapetype>` elemento pode aparecer sozinho ou dentro de um elemento `<group>` . Você pode ter muitas formas dentro de grupos diferentes que referenciam o mesmo tipo de forma. Se um tipo de forma aparecer dentro de um grupo, uma forma que resida em outro grupo ainda poderá referenciar esse tipo de forma.

Por exemplo, na representação VML a seguir, Rect1 e Rect2 estão em GroupA e Rect3 está em GroupB. Todos os três retângulos são instautados do tipo de forma MyShape.


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



Para obter mais informações sobre esse elemento, consulte a [especificação de VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .

 

 