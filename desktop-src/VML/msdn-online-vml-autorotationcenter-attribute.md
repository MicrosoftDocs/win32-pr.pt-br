---
title: Atributo VML AutoRotationCenter
description: Atributo VML AutoRotationCenter
ms.assetid: beb6771f-42f4-458a-b525-4eb67bc1eff0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54b363b34a6b2f943be45d457e252eebcf597afd7f82b7992cf151b0c2eda4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347098"
---
# <a name="vml-autorotationcenter-attribute"></a>Atributo VML AutoRotationCenter

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se o centro de rotação será o centro geométrico daion. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* autorotationcenter=" *expressão* ">

**Sintaxe do script**

*element* .autorotationcenter="*expression*"

*expressão* = *elemento*.autorotationcenter

**Comentários**

O centro geométrico de uma forma extrudada é 0,0,0. Se o valor desse atributo for **False**, o centro de rotação será determinado pelo [atributo RotationCenter.](msdn-online-vml-rotationcenter-attribute.md) O padrão é **False**.

*Microsoft Office Atributo Extensions*

 

 