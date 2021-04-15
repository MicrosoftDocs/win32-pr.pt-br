---
title: Atributo Font-Size de VML
description: Atributo Font-Size de VML
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c02b2df8fb0076ed6df6342e40b980ed8aa248e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454330"
---
# <a name="vml-font-size-attribute"></a>Atributo Font-Size de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o tamanho da fonte. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "fonte-tamanho: *expressão* " >

**Sintaxe do script**

*elemento* . Style. FontSize = "*expressão*"

*expressão* = de *elemento*. Style. FontSize

**Comentários**

O tamanho da fonte é definido em pontos. Os valores são os mesmos que os atributos de estilo HTML padrão.

*Atributo padrão da VML*

**Exemplo**

O tamanho da fonte é de 36 pontos.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 