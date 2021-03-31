---
title: Para atributo (linha) (VML)
description: Para atributo (linha) (VML)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641807"
---
# <a name="to-attribute-linevml"></a>Para atributo (linha) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ponto final de uma linha. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Linha](msdn-online-vml-line-element.md)

**Sintaxe de marca**

<v: *Element* para = " *expression* " >

**Sintaxe do script**

*elemento* . to = "*expression*"

*expressão* = de *elemento*. para

**Comentários**

Define o ponto final da linha no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O padrão é 10, 10.

**Atributo padrão da VML**

**Exemplo**

A linha termina em um local 100 aponta para baixo e 100 pontos à direita do canto superior esquerdo do espaço pai.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 