---
title: Atributo AutoRotationCenter de VML
description: Atributo AutoRotationCenter de VML
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624ab3f2c37e043a6d478ca8e422a714a83d157
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641354"
---
# <a name="vml-autorotationcenter-attribute"></a>Atributo AutoRotationCenter de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se o centro de rotação será o centro geométrico da extrusão. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *Element* autorotationcenter = " *expressão* " >

**Sintaxe do script**

*Element* . autorotationcenter = "*expressão*"

*expressão* = de *elemento*. autorotationcenter

**Comentários**

O centro geométrico de uma forma extrudada é 0, 0, 0. Se o valor desse atributo for **false**, o centro de rotação será determinado pelo atributo [RotationCenter](msdn-online-vml-rotationcenter-attribute.md) . O padrão é **False**.

*Atributo de extensões de Microsoft Office*

 

 