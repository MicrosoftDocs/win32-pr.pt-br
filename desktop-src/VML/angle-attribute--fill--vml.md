---
title: Atributo Angle (preenchimento) (VML)
description: Atributo Angle (preenchimento) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008076"
---
# <a name="angle-attribute-fillvml"></a>Atributo Angle (preenchimento) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ângulo de um preenchimento gradual. Leitura/gravação. [VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* Angle = " *expressão* " >

**Sintaxe do script**

*elemento* . Angle = "*expressão*"

*expressão* = de *elemento*. Angle

**Comentários**

O vetor de um gradiente é perpendicular ao vetor da direção de mistura de uma cor para outra. O valor padrão é 0 (zero) graus, que é um vetor horizontal da esquerda para a direita. Ângulos positivos giram o gradiente em uma direção do sentido anti-horário.

*Atributo padrão da VML*

**Exemplo**

O preenchimento da forma é composto de um gradiente de duas cores, sendo executado de azul para vermelho em um ângulo de 45 graus. Vermelho estará no canto superior esquerdo e azul estará no canto inferior direito.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 