---
title: Atributo de estilo da VML
description: Atributo de estilo da VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454087"
---
# <a name="vml-style-attribute"></a>Atributo de estilo da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o estilo do quadro. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *elemento* Style = " *expressão* " >

**Sintaxe do script**

*elemento* . Style = "*expressão*"

*expressão* = de *elemento*. Style

**Comentários**

Esse atributo usa os atributos normais de estilo CSS para posicionamento.

*Atributo padrão da VML*

**Exemplo**

O estilo define a posição real do quadro.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 