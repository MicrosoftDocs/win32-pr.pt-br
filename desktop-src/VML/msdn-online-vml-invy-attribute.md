---
title: Atributo InvY de VML
description: Atributo InvY de VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294193"
---
# <a name="vml-invy-attribute"></a>Atributo InvY de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se a posição y do identificador é invertida. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[H](msdn-online-vml-h-element.md) (subelemento de [identificadores](msdn-online-vml-handles-element.md))

**Sintaxe de marca**

<v: *Element* invy = " *expressão* " >

**Comentários**

Se **for true**, a posição y do identificador será invertida com a subtração do valor y do valor y de **CoordOrigin** adicionado ao valor y de **CoordSize**. O valor padrão é **Falso**.

Este atributo é o equivalente de


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Atributo padrão da VML*

 

 