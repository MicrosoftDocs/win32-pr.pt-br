---
title: Atributo de metal de VML
description: Atributo de metal de VML
ms.assetid: 4d2efaed-d391-494f-9f0c-d57ad019f71d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d318724f0a8f3c5fbce1ee9045ed5d6e0d49686
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366053"
---
# <a name="vml-metal-attribute"></a>Atributo de metal de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se a superfície da forma extrudada será semelhante a um metal. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* metal = " *expressão* " >

**Sintaxe do script**

*Element* . metal = "*expressão*"

*expressão* = de *elemento*. metal

**Comentários**

Se definido como **true**, esse atributo fará com que a luz refletida de forma especulada seja a cor do material em vez da cor da fonte de luz, tornando o objeto aparentemente mais metálico. Para aproximar ainda mais um material metálico, é necessário que a especulação seja relativamente alta (cerca de 1,2) e a didifusão seja relativamente baixa (cerca de 0,6). O valor padrão é **Falso**.

*Atributo de extensões de Microsoft Office*

 

 