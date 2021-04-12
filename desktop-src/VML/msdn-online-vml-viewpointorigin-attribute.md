---
title: Atributo ViewpointOrigin de VML
description: Atributo ViewpointOrigin de VML
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454132"
---
# <a name="vml-viewpointorigin-attribute"></a>Atributo ViewpointOrigin de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a origem do ponto de vista dentro da caixa delimitadora da forma. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *Element* viewpointorigin = " *expressão* " >

**Sintaxe do script**

*Element* . viewpointorigin = "*expressão*"

*expressão* = de *elemento*. viewpointorigin

**Comentários**

Define o ponto de vista em termos dos valores x e y da forma original. Os valores x e y variam de 0,5 a-0,5 (50% a-50% da origem da coordenada da forma). O padrão é 0, 0.

*Atributo de extensões de Microsoft Office*

 

 