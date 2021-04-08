---
title: Para atributo (curva) (VML)
description: Para atributo (curva) (VML)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823976"
---
# <a name="to-attribute-curvevml"></a>Para atributo (curva) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ponto final de uma curva. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxe de marca**

<v: *Element* para = " *expression* " >

**Sintaxe do script**

*elemento* . to = "*expression*"

*expressão* = de *elemento*. para

**Comentários**

Define o ponto final de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O padrão é 30, 20.

**Atributo padrão da VML**

**Exemplo**

A curva é sorrindo. Ele começa à esquerda e termina à direita. Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 