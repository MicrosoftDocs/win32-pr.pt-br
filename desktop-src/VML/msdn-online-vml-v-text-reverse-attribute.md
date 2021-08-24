---
title: Atributo de inversão de texto V de VML
description: Atributo de inversão de texto V de VML
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f1535620c1fefe98ac23e2f842ef9a97e13b9cb39c65ec6b97f6f7d12b1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654616"
---
# <a name="vml-v-text-reverse-attribute"></a>Atributo de inversão de texto V de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 