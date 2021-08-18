---
title: Atributo de marcador VML
description: Atributo de marcador VML
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f35fda917931567dcd2dc4cf823ed74e3b449e05fba6046f1390e3d6454fd45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755015"
---
# <a name="vml-bullet-attribute"></a>Atributo de marcador VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se uma forma é um marcador gráfico. Ler/gravar **VgTriState.**

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:bullet=" *expressão* ">

**Comentários**

O padrão é **False**. Se **True**, a forma será um marcador gráfico.

*Microsoft Office Atributo Extensions*

**Exemplo**

A forma é um marcador.


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 