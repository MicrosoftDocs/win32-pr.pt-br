---
title: Elemento de sombra VML
description: Elemento de sombra VML
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917343"
---
# <a name="vml-shadow-element"></a>Elemento de sombra VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma sombra para uma forma.

Os atributos a seguir modificam uma sombra.



| Atributo                                          | Descrição                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Cor](color-attribute--shadow--vml.md)          | Define a cor de uma sombra.                     |
| [Color2](color2-attribute--shadow--vml.md)        | Define a segunda cor de uma sombra.              |
| [ID](id-attribute--shadow--vml.md)                | Especifica o identificador exclusivo de uma sombra.       |
| [Matriz](matrix-attribute--shadow--vml.md)        | Define a transformação de perspectiva de uma sombra.     |
| [Obscurecida](msdn-online-vml-obscured-attribute.md) | Determina se a sombra é transparente.      |
| [Deslocamento](offset-attribute--shadow--vml.md)        | Define até que distância a sombra ultrapassa a forma. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Define um segundo deslocamento.                           |
| [Ativado](on-attribute--shadow--vml.md)                | Determina se uma sombra é exibida.          |
| [Opacidade](opacity-attribute--shadow--vml.md)      | Determina a transparência de uma sombra.           |
| [Ter](origin-attribute--shadow--vml.md)        | Define o centro da sombra.                  |
| [Tipo](type-attribute--shadow--vml.md)            | Especifica o tipo de sombra.                      |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

Além disso, o atributo [on](on-attribute--shadow--vml.md) deve ser definido como **true**.

Veja a seguir o código mínimo necessário para produzir uma sombra.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



Você não pode notar a sombra a menos que aumente os valores de [deslocamento](offset-attribute--shadow--vml.md) , já que o deslocamento padrão é 2PT, 2PT.

**Exemplos**

-   [Exemplo de sombra simples](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Exemplo de sombra dinâmica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 