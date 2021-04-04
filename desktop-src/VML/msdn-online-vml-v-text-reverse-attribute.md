---
title: Atributo de inversão de texto V de VML
description: Atributo de inversão de texto V de VML
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007853"
---
# <a name="vml-v-text-reverse-attribute"></a>Atributo de inversão de texto V de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se a ordem de layout das linhas é invertida. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "v-Text-Reverse: *expression* " >

**Sintaxe do script**

*elemento* . Style. v-Text-Reverse = "*expression*"

*expressão* = de *elemento*. Style. v-texto-reverso

**Comentários**

Se **for true**, a ordem de layout das linhas será invertida. Esse atributo é usado para layout de texto vertical. O valor padrão é **Falso**.

*Atributo padrão da VML*

**Exemplo**

A ordem de layout é invertida.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 