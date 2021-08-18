---
title: Atributo OnEd do VML
description: Atributo OnEd do VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ef444037a0cd05a7cfbed5a97bb93ed7e8236a9d9f66bf1f7bd77b92b82e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999146"
---
# <a name="vml-oned-attribute"></a>Atributo OnEd do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se os alças extras de uma forma estão ocultos. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:oned=" *expressão* ">

**Comentários**

Oculta todos os alças de forma, exceto a parte superior esquerda e inferior direita; ou seja, os mesmos alças usados para um segmento de linha reta. O padrão é **False**.

*Microsoft Office Atributo Extensions*

**Exemplo**

Todos, menos os alças superior esquerdo e inferior direito da forma, estão ocultos.


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 