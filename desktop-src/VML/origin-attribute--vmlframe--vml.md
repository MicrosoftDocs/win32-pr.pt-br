---
title: Atributo Origin (VMLFrame) (VML)
description: Atributo Origin (VMLFrame) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874b857a2408927e296f82f0f9aa0a5e15f6da69b1e2af6eaf6ebe2c5df746d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768256"
---
# <a name="origin-attribute-vmlframevml"></a>Atributo Origin (VMLFrame) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a origem da região de recorte do quadro. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *elemento* Origin = " *expressão* " >

**Sintaxe do script**

*elemento* . Origin = "*expressão*"

*expressão* = de *elemento*. Origin

**Comentários**

O valor padrão é 0,0. Observe que a **origem** só funciona se o [clipe](msdn-online-vml-clip-attribute.md) for **verdadeiro**. Nesse atributo, a origem é definida como o canto superior esquerdo do quadro.

*Atributo padrão da VML*

**Exemplo**

A origem da região de recorte é 100pt, 100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 