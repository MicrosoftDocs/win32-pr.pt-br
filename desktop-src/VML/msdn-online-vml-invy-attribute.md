---
title: Atributo VML InvY
description: Atributo VML InvY
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d012e8ac6afe0e7808236c36d8dd3088ce9fa3552b4b7efa0542ea8612e4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599864"
---
# <a name="vml-invy-attribute"></a>Atributo VML InvY

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se a posição y do alça é invertida. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[H](msdn-online-vml-h-element.md) (subelemento de [alças](msdn-online-vml-handles-element.md))

**Sintaxe de marca**

<v: *element* invy=" *expressão* ">

**Comentários**

Se **True**, a posição y do handle será invertida subtraindo o valor y do valor y de **CoordOrigin** adicionado ao valor y **de CoordSize.** O valor padrão é **Falso**.

Esse atributo é o equivalente de


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*Atributo padrão VML*

 

 