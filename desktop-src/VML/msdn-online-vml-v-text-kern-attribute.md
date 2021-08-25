---
title: Atributo VML V-Text-Kern
description: Atributo VML V-Text-Kern
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5ca41b66c05af673839ccbc8ba9eb95cf652eb223cd4dd3915799e91ff6c69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974626"
---
# <a name="vml-v-text-kern-attribute"></a>Atributo VML V-Text-Kern

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se o apuramento está ligado. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="v-text-ltd: *expression* ">

**Sintaxe do script**

*elemento* .style.v-text-kern="*expression*"

*expressão* = *elemento*.style.v-text-kern

**Comentários**

Se **True**, a a adoção será 100000001. O padrão é **False**. Oinging é a remoção de espaço entre determinados pares de letras para compensar as letras desiguais. Por exemplo, se o recurso for ligado, o espaço extra entre um "T" maiúsculo e um "i" minúsculo será removido.

*Atributo padrão VML*

**Exemplo**

O Kerning está ligado.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 