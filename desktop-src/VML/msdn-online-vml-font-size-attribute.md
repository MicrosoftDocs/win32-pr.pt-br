---
title: Atributo Font-Size de VML
description: Atributo Font-Size de VML
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401d66668b0a86b92e453ac2e4a8a9adb96411131cc90f7bf14bd22be67e6775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346573"
---
# <a name="vml-font-size-attribute"></a>Atributo Font-Size de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 