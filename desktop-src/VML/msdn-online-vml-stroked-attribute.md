---
title: Atributo de traço de VML
description: Atributo de traço de VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9398452365ee6076309cafa40c0373dcaa12d52a868e71eb77e4b42780badb0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754441"
---
# <a name="vml-stroked-attribute"></a>Atributo de traço de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define se o caminho será traçado. Leitura/gravação. [VgTriState](msdn-online-vml-vgtristate.md) .

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* strokeed = " *expression* " >

**Sintaxe do script**

*elemento* . stroked = "*expressão*"

*expressão* = de *elemento*. strokeed

**Comentários**

O valor é duplicado a partir do atributo **on** do elemento [Stroke](msdn-online-vml-stroke-element.md) .

*Atributo padrão da VML*

**Exemplo**

O caminho da forma é traçado.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo de atributo strokeed](/previous-versions/bb264094(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 