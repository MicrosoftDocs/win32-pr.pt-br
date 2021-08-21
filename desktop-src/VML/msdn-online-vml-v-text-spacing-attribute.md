---
title: Atributo de espaçamento da VML V-Text-
description: Atributo de espaçamento da VML V-Text-
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0b699e70cd235bf7d0f7530f75a8fc5eaef52974180cc8d36a10a69c9197f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057674"
---
# <a name="vml-v-text-spacing-attribute"></a>Atributo de espaçamento da VML V-Text-

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 