---
title: Atributo VML V
description: Atributo VML V
ms.assetid: be55704f-71f3-4c0b-8a1b-d7de5efa85dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbf2f8654d32714d20e9b0c5a36fb939173698749569692120c04b89e84b6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768326"
---
# <a name="vml-v-attribute"></a>Atributo VML V

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define os comandos que comem um caminho. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* v=" *expressão* ">

**Sintaxe do script**

*element* .v="*expression*"

*expressão* = *elemento*.v

**Comentários**

Substitui o **atributo Path** de uma forma. As coordenadas podem ser números fixos, números relativos ou referências a fórmulas (usando o formato " em que n é um número de fórmula; por exemplo, " " refere-se à segunda fórmula na matriz de @n @2 fórmulas).

*Atributo padrão VML*

**Exemplo**

Um retângulo é criado usando o **atributo V.** Observe que uma letra minúscula L (**comando lineto)** é usada após o primeiro conjunto de coordenadas delimitadas por vírgulas.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```





 

 