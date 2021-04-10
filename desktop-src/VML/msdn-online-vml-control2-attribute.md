---
title: Atributo Control2 de VML
description: Atributo Control2 de VML
ms.assetid: fd0f92fa-ae70-46c9-bfbe-fad8deea34f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7af3871981e26ff7eff471651de555483fd540
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084566"
---
# <a name="vml-control2-attribute"></a>Atributo Control2 de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o segundo ponto de controle de uma curva de Bézier. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxe de marca**

<v: *Element* Control2 = " *expressão* " >

**Sintaxe do script**

*Element* . Control2 = "*expressão*"

*expressão* = de *elemento*. Control2

**Comentários**

Define o segundo ponto de controle de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O padrão é 20,0.

*Atributo padrão da VML*

**Exemplo**

A curva é sorrindo. Ele começa à esquerda e termina à direita. Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 