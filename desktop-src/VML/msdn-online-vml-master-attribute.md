---
title: Atributo mestre da VML
description: Atributo mestre da VML
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084881"
---
# <a name="vml-master-attribute"></a>Atributo mestre da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se um elemento **ShapeType** é um elemento mestre. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Formatype](msdn-online-vml-shapetype-element.md)

**Sintaxe de marca**

<v: *Element* o:Master = " *expressão* " >

**Comentários**

Se **for true**, a forma **ShapeType** será renderizada pelo mecanismo de renderização. O valor padrão é **Falso**.

*Atributo de extensões de Microsoft Office*

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



 

 