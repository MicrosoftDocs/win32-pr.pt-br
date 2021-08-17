---
title: Atributo de estilo da VML
description: Atributo de estilo da VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0b7ce7985687d560fc46ebb98d41b51e7a461e811deb228b0a5709a35c5d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475186"
---
# <a name="vml-style-attribute"></a>Atributo de estilo da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 