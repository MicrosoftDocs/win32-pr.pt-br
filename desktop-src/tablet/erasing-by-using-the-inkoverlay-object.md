---
description: O objeto InkOverlay pode ser anexado a um controle Window e é usado para habilitar a capacidade básica de tinta.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Apagando usando o objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647253"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Apagando usando o objeto InkOverlay

O objeto [**InkOverlay**](inkoverlay-class.md) pode ser anexado a um controle Window e é usado para habilitar a capacidade básica de tinta. Você pode usar o objeto **InkOverlay** para apagar a tinta definindo a propriedade [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) igual a **delete**. Em seguida, você pode definir a propriedade [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) para os membros de **traço** ou **ponto** de [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). Definir a propriedade **EraserMode** como **Stroke** apaga traços inteiros. Definir a propriedade **EraserMode** como **Point** apaga a tinta que o cursor passa.

 

 



