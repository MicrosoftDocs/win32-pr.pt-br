---
title: Atributo VML V-Text-Spacing-Mode
description: Atributo VML V-Text-Spacing-Mode
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42137e8c8ec401548c4e0b027a50f34813fc7b45b04c4568011617906ac8e1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057654"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Atributo VML V-Text-Spacing-Mode

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o modo para espaçamento de letras. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="v-text-spacing-mode: *expression* ">

**Sintaxe do script**

*elemento* .style.v-text-spacing-mode="*expression*"

*expressão* = *elemento*.style.v-text-spacing-mode

**Comentários**

Os valores incluem

-   **reforçando** (padrão)
-   **Rastreamento**

Esse atributo determina se o espaço será removido entre cada letra (reforçando) ou adicionado entre cada letra (acompanhamento). A quantidade de alteração de espaçamento de letras é definida pelo [atributo espaçamento de](msdn-online-vml-v-text-spacing-attribute.md) texto de V.

*Atributo padrão VML*

**Exemplo**

O espaçamento de letras entre cada letra é aumentado em 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 