---
title: Atributo de fonte VML
description: Atributo de fonte VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074aa0672002dcbbac55d21ed27383d5a3fd6e3b9ccfe9125ad89c2c43ac71ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986656"
---
# <a name="vml-font-attribute"></a>Atributo de fonte VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica um valor composto de atributos de fonte. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="font: *expression* ">

**Sintaxe do script**

*expressão element* .style.font=""

*expressão* = *elemento*.style.font

**Comentários**

Define os atributos de uma fonte, incluindo família, estilo, peso, tamanho e variante. A ordem das definições na cadeia de caracteres é: **font-style**, **font-variant**, **font-weight**, **font-size**, **line-height** e **font-family**. Os valores são os mesmos que os atributos de estilo HTML padrão.

*Atributo padrão VML*

**Exemplo**

A fonte do texto textpath é itálico, small-caps, negrito, 36 pontos Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 