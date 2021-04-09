---
title: Atributo TextBoxRect de VML
description: Atributo TextBoxRect de VML
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007616"
---
# <a name="vml-textboxrect-attribute"></a>Atributo TextBoxRect de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma ou mais caixas de texto dentro de uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* textboxrect = " *expressão* " >

**Sintaxe do script**

*Element* . textboxrect = "*expressão*"

*expressão* = de *elemento*. textboxrect

**Comentários**

Uma caixa de texto é definida por um ou mais conjuntos de números que especificam (na ordem) os pontos esquerdo, superior, direito e inferior do retângulo. Vários conjuntos são delimitados por ponto e vírgula. O valor padrão é o mesmo valor de dimensão que o retângulo que o contém. Se mais de uma caixa de texto for definida, os conjuntos de quádruplo delimitados por vírgula que definem cada caixa de texto serão separados por ponto e vírgula. Normalmente, as caixas de Textsão fornecidas em conjuntos de 1, 2, 3 ou 6 retângulos em uma forma.

*Atributo padrão da VML*

**Exemplo**

Uma caixa de texto de 95 unidades por 95 unidades é definida e colocou 5 unidades dentro do canto superior esquerdo da forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 