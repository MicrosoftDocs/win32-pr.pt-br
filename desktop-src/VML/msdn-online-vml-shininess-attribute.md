---
title: Atributo de luminosidade de VML
description: Atributo de luminosidade de VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294090"
---
# <a name="vml-shininess-attribute"></a>Atributo de luminosidade de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a concentração da luz refletida em uma superfície de extrusão. Leitura/gravação. **VgNumber**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* luminosidade = " *expressão* " >

**Sintaxe do script**

*elemento* . luminosidade = "*expressão*"

*expressão* = de *elemento*. luminosidade

**Comentários**

Valores altos (8-10) aproximam a luminosidade de um espelho e valores baixos (2-3) aproximariam um efeito manchado. Os valores de 4-7 são típicos. Os reflexos não espelham outros objetos; apenas as fontes de luz do Pinpoint são refletidas. O valor padrão é 5.

*Atributo de extensões de Microsoft Office*

 

 