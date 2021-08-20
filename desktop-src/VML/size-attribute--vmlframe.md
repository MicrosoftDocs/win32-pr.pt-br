---
title: Atributo size (VMLFrame)
description: Atributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32d496bc40b5b84b7a8a16bf6b84a2926010d56dcc311659dd63300363a7067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754121"
---
# <a name="size-attribute-vmlframe"></a>Atributo size (VMLFrame)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 