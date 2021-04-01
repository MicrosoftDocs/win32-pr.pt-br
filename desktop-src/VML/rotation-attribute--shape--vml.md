---
title: Atributo de rotação (forma) (VML)
description: Atributo de rotação (forma) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008314"
---
# <a name="rotation-attribute-shapevml"></a>Atributo de rotação (forma) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ângulo em que uma forma é girada. Leitura/gravação. [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "rotação: *expressão* " >

**Sintaxe do script**

*elemento* . Rotation = "*expressão*"

*expressão* = de *elemento*. Rotation

**Comentários**

O valor em graus pode ser positivo ou negativo, e valores maiores que 360 são modularizados para um círculo de 360 graus. Os ângulos positivos são no sentido horário. O valor padrão é 0.

Observe que a forma é reposicionada após a rotação para refletir as novas coordenadas da caixa delimitadora.

Observe também que para scripts, o atributo **Style** não é usado e essa **rotação** é tratada como um atributo direto da forma.

O atributo de **rotação** é semelhante ao atributo de **rotação** HTML padrão para estilos.

*Atributo padrão da VML*

**Consulte também**

**Exemplo**

O retângulo será inclinado 45 graus.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Exemplo de atributo de rotação](/previous-versions/bb264091(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 