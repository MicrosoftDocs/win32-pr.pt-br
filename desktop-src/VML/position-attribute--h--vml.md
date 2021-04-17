---
title: Atributo de posição (H) (VML)
description: Atributo de posição (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811401"
---
# <a name="position-attribute-hvml"></a>Atributo de posição (H) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica os valores de thex e y do identificador. **VgVector2D** de leitura/gravação.

**Aplica-se a**

[H](msdn-online-vml-h-element.md) (subelemento de [identificadores](msdn-online-vml-handles-element.md))

**Sintaxe de marca**

<v: *elemento* position = " *expressão* " >

**Comentários**

os valores x e y podem ser um dos seguintes tipos:

-   constante
-   fórmula (por exemplo, @2 )
-   ajustar (por exemplo, \# 3)
-   centro
-   topleft
-   bottomright

Se qualquer um dos tipos acima, exceto *ajuste* , for especificado, a posição do identificador será corrigida nessa dimensão. Se um identificador de ajuste for especificado, o identificador será livre para mover nessa dimensão e o valor de ajuste será determinado pela posição do identificador.

Se um atributo [polar](msdn-online-vml-polar-attribute.md) for especificado, o atributo **Position** representará os valores de raio e ângulo da alça em vez de x e y.

O valor padrão é 0,0.

*Atributo padrão da VML*

 

 