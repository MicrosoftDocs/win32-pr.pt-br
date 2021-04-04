---
title: Atributo size (VMLFrame)
description: Atributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007612"
---
# <a name="size-attribute-vmlframe"></a>Atributo size (VMLFrame)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o tamanho da região de recorte do quadro. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *Element* tamanho = " *expression* " >

**Sintaxe do script**

*elemento* . Size = "*expressão*"

*expressão* = de *elemento*. Size

**Comentários**

O valor padrão é 0,0. Observe que o **tamanho** funciona apenas se o [clipe](msdn-online-vml-clip-attribute.md) for **verdadeiro**. Nesse atributo, o tamanho é definido como a largura e a altura do quadro.

*Atributo padrão da VML*

**Exemplo**

O tamanho da região de recorte será 50pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 