---
title: Atributo de modo de espaçamento da VML V-Text-mode
description: Atributo de modo de espaçamento da VML V-Text-mode
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454328"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Atributo de modo de espaçamento da VML V-Text-mode

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o modo para espaçamento. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "v-texto-Spacing-Mode: *expressão* " >

**Sintaxe do script**

*elemento* . Style. v-Text-Spacing-Mode = "*expressão*"

*expressão* = de *elemento*. Style. v-modo de espaçamento de texto

**Comentários**

Os valores incluem

-   **estreitamento** (padrão)
-   **controle alterações**

Esse atributo determina se o espaço será removido entre cada letra (apertar) ou adicionado entre cada letra (acompanhamento). A quantidade de alteração de espaçamento é definida pelo atributo [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) .

*Atributo padrão da VML*

**Exemplo**

O espaçamento entre cada letra é aumentado em 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 