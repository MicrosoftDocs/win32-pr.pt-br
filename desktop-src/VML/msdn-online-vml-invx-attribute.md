---
title: Atributo InvX de VML
description: Atributo InvX de VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641293"
---
# <a name="vml-invx-attribute"></a>Atributo InvX de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se a posição x do identificador é invertida. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[H](msdn-online-vml-h-element.md) (subelemento de [identificadores](msdn-online-vml-handles-element.md))

**Sintaxe de marca**

<v: *Element* invx = " *expressão* " >

**Comentários**

Se **for true**, a posição x do identificador será invertida com a subtração do valor x do valor x de **CoordOrigin** adicionado ao valor x de **CoordSize**. O valor padrão é **Falso**.

Este atributo é o equivalente de

coordorigin. x + coordsize. x-h. Position. x

*Atributo padrão da VML*

 

 