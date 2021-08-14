---
title: Atributo de Control1 de VML
description: Atributo de Control1 de VML
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b4c57a936a2820e5189be78cab119b4455d20af22735a47a66c444f721723f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601929"
---
# <a name="vml-control1-attribute"></a>Atributo de Control1 de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o primeiro ponto de controle de uma curva de Bézier. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Curva](msdn-online-vml-curve-element.md)

**Sintaxe de marca**

<v: *Element* Control1 = " *expressão* " >

**Sintaxe do script**

*Element* . Control1 = "*expressão*"

*expressão* = de *elemento*. Control1

**Comentários**

Define o primeiro ponto de controle de uma curva de Bézier cúbica no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O padrão é 10, 10.

*Atributo padrão da VML*

**Exemplo**

A curva é sorrindo. Ele começa à esquerda e termina à direita. Os dois pontos de controle estão situados ao longo do caminho para puxar a curva para dar a aparência de um sorriso.


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 