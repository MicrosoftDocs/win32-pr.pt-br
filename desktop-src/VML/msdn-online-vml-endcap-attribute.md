---
title: Atributo EndCap de VML
description: Atributo EndCap de VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b2d36eb76b840ca8f89aebf3dadefaa68093394a07bd78db0e8fa0b18ed555
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346711"
---
# <a name="vml-endcap-attribute"></a>Atributo EndCap de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o estilo de extremidade para o final de um traço. Leitura/gravação. **VgLineEndCapStyle**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* EndCap = " *expressão* " >

**Sintaxe do script**

*Element* . EndCap = "*expressão*"

*expressão* = de *elemento*. EndCap

**Comentários**

Os valores são:

-   Simples (padrão)
-   Square
-   Round

*Atributo padrão da VML*

**Exemplo**

Uma linha é desenhada com uma extremidade plana no final do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 