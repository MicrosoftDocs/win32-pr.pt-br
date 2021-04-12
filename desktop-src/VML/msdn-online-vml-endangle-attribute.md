---
title: Atributo de ângulo de fim da VML
description: Atributo de ângulo de fim da VML
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294468"
---
# <a name="vml-endangle-attribute"></a>Atributo de ângulo de fim da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ponto de extremidade do arco. Leitura/gravação. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .

**Aplica-se a**

[Arc](msdn-online-vml-arc-element.md)

**Sintaxe de marca**

<v: *Element* arângulo = " *expression* " >

**Sintaxe do script**

*elemento* . endângulo = "*expressão*"

*expressão* = de ângulo de *elemento*.

**Comentários**

O arco é definido como um traço desenhado ao longo de uma oval limitada pelos atributos de **estilo** de uma forma. O final do traço é definido por um ângulo medido de forma direta (12 horas) no sentido horário. O valor padrão é 90 graus.

*Atributo padrão da VML*

**Exemplo**

O arco é sorrindo. O ponto de partida está no ponto de 90 graus de uma elipse inscrita dentro da caixa delimitadora de forma. O ponto de extremidade está no ponto de 270 graus da elipse.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 