---
title: Atributo from (curva) (VML)
description: Atributo from (curva) (VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366622"
---
# <a name="from-attribute-curvevml"></a>Atributo from (curva) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ponto de partida de uma curva. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxe de marca**

<v: *Element* de = " *expression* " >

**Sintaxe do script**

*elemento* . from = "*expressão*"

*expressão* = de *elemento*. from

**Comentários**

Define o ponto inicial de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O padrão é 0, 0.

*Atributo padrão da VML*

**Exemplo**

A curva é sorrindo. Ele começa à esquerda e termina à direita. Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 