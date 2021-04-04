---
title: Atributo StartAngle de VML
description: Atributo StartAngle de VML
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007793"
---
# <a name="vml-startangle-attribute"></a>Atributo StartAngle de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ponto inicial do arco. Leitura/gravação. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .

**Aplica-se a**

[Arc](msdn-online-vml-arc-element.md)

**Sintaxe de marca**

<v: *Element* arângulo = " *expression* " >

**Sintaxe do script**

*elemento* . endângulo = "*expressão*"

*expressão* = de ângulo de *elemento*.

**Comentários**

O arco é definido como um traço desenhado ao longo de uma oval limitada pelos atributos de **estilo** de uma forma. O início do traço é definido por um ângulo medido de forma direta (12 horas) no sentido horário. O valor padrão é 0 graus.

Atributo padrão da VML

**Exemplo**

O arco é sorrindo. O ponto de partida está no ponto de 90 graus de uma elipse inscrita dentro da caixa delimitadora de forma. O ponto de extremidade está no ponto de 270 graus da elipse.


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 