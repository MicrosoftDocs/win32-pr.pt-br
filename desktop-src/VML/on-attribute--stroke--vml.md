---
title: Atributo On (Traço)(VML)
description: Atributo On (Traço)(VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5682200a44a98d2b4c074b11db172e2b94b812a196a404927a33b4d142289e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007566"
---
# <a name="on-attribute-strokevml"></a>Atributo On (Traço)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se o traço será exibido. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* on=" *expressão* ">

**Sintaxe do script**

*elemento* .on="*expression*"

*expressão* = *elemento*.on

**Comentários**

Se **False**, o traço não será exibido. O padrão é **True**.

*Atributo padrão VML*

**Exemplo**

O traço não será exibido.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 