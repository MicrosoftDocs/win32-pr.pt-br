---
title: Atributo de kerning da VML V-Text-
description: Atributo de kerning da VML V-Text-
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917513"
---
# <a name="vml-v-text-kern-attribute"></a>Atributo de kerning da VML V-Text-

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se o kerning está ativado. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "v-Text-kerning: *expression* " >

**Sintaxe do script**

*elemento* . Style. v-Text-kerning = "*expression*"

*expressão* = de *elemento*. Style. v-ajuste de texto

**Comentários**

Se for **true**, o kerning será ativado. O padrão é **False**. O kerning é a remoção de espaço entre determinados pares de letras para compensar letterformss desiguais. Por exemplo, se o kerning for ativado, o espaço extra entre um "T" maiúsculo e um "i" minúsculo seriam removidos.

*Atributo padrão da VML*

**Exemplo**

O kerning está ativado.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 