---
title: Atributo da VML V-Text-Align
description: Atributo da VML V-Text-Align
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917423"
---
# <a name="vml-v-text-align-attribute"></a>Atributo da VML V-Text-Align

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o alinhamento do texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "v-text-align: *expression* " >

**Sintaxe do script**

*elemento* . Style. v-texto-align = "*expressão*"

*expressão* = de *elemento*. Style. v-alinhamento de texto

**Comentários**

Os valores são:

-   **esquerda** (padrão)
-   **direita**
-   **centraliza**
-   **Justify**
-   **justificar à carta**
-   **alongar/justificar**

*Atributo padrão da VML*

**Exemplo**

O texto será ampliado para se ajustar ao caminho, mas o espaço extra será colocado entre cada letra.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 