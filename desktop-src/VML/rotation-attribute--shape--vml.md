---
title: Atributo Rotation (Forma)(VML)
description: Atributo Rotation (Forma)(VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f73b55b57a7b9d9d7f14cdae4ec71a38a1e38246a4430339db23f35a339430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754131"
---
# <a name="rotation-attribute-shapevml"></a>Atributo Rotation (Forma)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o ângulo em que uma forma é girada. Leitura/gravação. [VgAngleInDegrees.](msdn-online-vml-vgangleindegrees-data-type.md)

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="rotation: *expression* ">

**Sintaxe do script**

*elemento* .rotation="*expression*"

*expressão* = *elemento*.rotation

**Comentários**

O valor em graus pode ser positivo ou negativo e valores maiores que 360 são modularizados para um círculo de 360 graus. Ângulos positivos são no sentido horário. O valor padrão é 0.

Observe que a forma é reposicionada após a rotação para refletir as novas coordenadas da caixa delimitada.

Observe também que, para scripts, o atributo **de** estilo não é usado e que Rotation **é** tratado como um atributo direto da forma.

O **atributo Rotation** é semelhante ao atributo De **rotação** HTML padrão para estilos.

*Atributo padrão VML*

**Consulte também**

**Exemplo**

O retângulo será inclinado em 45 graus.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



[Exemplo de atributo de rotação](/previous-versions/bb264091(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 