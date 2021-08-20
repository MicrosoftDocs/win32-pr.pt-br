---
title: Atributo mestre da VML
description: Atributo mestre da VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d126b9d02144bbc8831d7be9e73a3e5896c2ceccca71cfcbc8161d5ccc8112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999106"
---
# <a name="vml-master-attribute"></a>Atributo mestre da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Determina se um elemento **ShapeType** é um elemento mestre. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Formatype](msdn-online-vml-shapetype-element.md)

**Sintaxe de marca**

<v: *Element* o:Master = " *expressão* " >

**Comentários**

Se **for true**, a forma **ShapeType** será renderizada pelo mecanismo de renderização. O valor padrão é **Falso**.

*Microsoft Office Atributo de extensões*

**Exemplo**

O elemento **formatype** é uma forma mestra.


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 