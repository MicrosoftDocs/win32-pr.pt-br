---
title: Atributo de ID (VMLFrame) (VML)
description: Atributo de ID (VMLFrame) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007762"
---
# <a name="id-attribute-vmlframevml"></a>Atributo de ID (VMLFrame) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um identificador exclusivo para o quadro. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *Element* ID = " *expression* " >

**Sintaxe do script**

*Element* . ID = "*expressão*"

*expressão* = de *elemento*. ID

**Comentários**

Use **ID** para fazer referência a um quadro. Por exemplo, você pode mover o quadro na página alterando a posição do quadro referenciado pela **ID**.

*Atributo padrão da VML*

**Exemplo**

A **ID** do quadro é "frame01".


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 