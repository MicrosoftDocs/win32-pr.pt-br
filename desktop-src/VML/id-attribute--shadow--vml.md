---
title: Atributo de ID (sombra) (VML)
description: Atributo de ID (sombra) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44cc307bcdd381247a105cc447e920819d3e8877bf66a81088bc8eabc8fa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057914"
---
# <a name="id-attribute-shadowvml"></a>Atributo de ID (sombra) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Especifica um nome que fornece um identificador exclusivo para uma sombra. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *Element* ID = " *expression* " >

**Sintaxe do script**

*Element* . ID = "*expressão*"

*expressão* = de *elemento*. ID

**Comentários**

Use **ID** para fazer referência a uma sombra específica. Depois de criar uma sombra e dada a ela uma ID, você pode usar o nome da ID quando desejar manipular a sombra.

*Atributo padrão da VML*

**Exemplo**

A forma tem uma ID de sombra chamada "MyShadow".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 