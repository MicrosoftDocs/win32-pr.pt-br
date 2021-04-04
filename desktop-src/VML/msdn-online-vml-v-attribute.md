---
title: Atributo da VML V
description: Atributo da VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690518e998163f7e47fb326b3037e6a4ec397e8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084639"
---
# <a name="vml-v-attribute"></a>Atributo da VML V

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define os comandos que compõem um caminho. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* v = " *expressão* " >

**Sintaxe do script**

*elemento* . v = "*expressão*"

*expressão* = de *elemento*. v

**Comentários**

Substitui o atributo **path** de uma forma. As coordenadas podem ser números fixos, números relativos ou referências a fórmulas (usando o formato " @n ", em que n é um número de fórmula; por exemplo, " @2 " refere-se à segunda fórmula na matriz de fórmulas).

*Atributo padrão da VML*

**Exemplo**

Um retângulo é criado usando o atributo **V** . Observe que uma letra minúscula L (comando **LineTo** ) é usada após o primeiro conjunto de coordenadas delimitadas por vírgulas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 