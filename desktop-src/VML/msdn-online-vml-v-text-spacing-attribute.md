---
title: Atributo de espaçamento da VML V-Text-
description: Atributo de espaçamento da VML V-Text-
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366364"
---
# <a name="vml-v-text-spacing-attribute"></a>Atributo de espaçamento da VML V-Text-

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a quantidade de espaçamento do texto. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "v-texto-Spacing: *expressão* " >

**Sintaxe do script**

*elemento* . Style. v-espaçamento de texto = "*expressão*"

*expressão* = de *elemento*. Style. v-espaçamento de texto

**Comentários**

O valor padrão é 100. Consulte o atributo [V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) para obter mais informações sobre o espaçamento de texto.

*Atributo padrão da VML*

**Exemplo**

O espaçamento entre cada letra é reforçado por 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 