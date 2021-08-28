---
title: From Attribute (Line)(VML)
description: From Attribute (Line)(VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a8bf41462f698397b193835d08655f8d6acefb2df77b17e035ec170c3c4781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099306"
---
# <a name="from-attribute-linevml"></a>From Attribute (Line)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o ponto inicial de uma linha. Leitura/gravação. **VgVector2D.**

**Aplica-se a**

[Linha](msdn-online-vml-line-element.md)

**Sintaxe de marca**

<v: *elemento* from=" *expressão* ">

**Sintaxe do script**

*elemento* .from="*expression*"

*expressão* = *elemento*.from

**Comentários**

Define o ponto inicial da linha no espaço de coordenadas do elemento pai. Se o pai não for um [](msdn-online-vml-units.md) elemento VML, a unidade padrão será um pixel (mas em, cm, mm, pt, pc também poderá ser especificado). O padrão é 0,0.

*Atributo padrão VML*

**Exemplo**

A linha começa em um local 10 pontos para baixo e 10 aponta para a direita do canto superior esquerdo do espaço pai.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 