---
title: Atributo To (Line)(VML)
description: Atributo To (Line)(VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d1e47261daf76103717476a84eea3bed99ddb0b514192df8a74cd0b69572a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654446"
---
# <a name="to-attribute-linevml"></a>Atributo To (Line)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o ponto final de uma linha. Leitura/gravação. **VgVector2D.**

**Aplica-se a**

[Linha](msdn-online-vml-line-element.md)

**Sintaxe de marca**

<v: *elemento* to=" *expressão* ">

**Sintaxe do script**

*element* .to="*expression*"

*expressão* = *elemento*.to

**Comentários**

Define o ponto final da linha no espaço de coordenadas do elemento pai. Se o pai não for um [](msdn-online-vml-units.md) elemento VML, a unidade padrão será um pixel (mas em, cm, mm, pt, pc também poderá ser especificado). O padrão é 10,10.

**Atributo padrão VML**

**Exemplo**

A linha termina em um local 100 pontos para baixo e 100 pontos à direita do canto superior esquerdo do espaço pai.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 