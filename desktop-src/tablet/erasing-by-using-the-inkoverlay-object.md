---
description: O objeto InkOverlay pode ser anexado a um controle de janela e é usado para habilitar a funcionalidade básica de tinta.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Apagando usando o objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110936"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Apagando usando o objeto InkOverlay

O [**objeto InkOverlay**](inkoverlay-class.md) pode ser anexado a um controle de janela e é usado para habilitar a funcionalidade básica de tinta. Você pode usar o **objeto InkOverlay** para apagar tinta definindo a [**propriedade EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) igual a **Delete**. Em seguida, você pode definir a [**propriedade EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) como os membros **Stroke** ou **Point** de [**InkOverlayEraserMode.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode) Definir a **propriedade EraserMode** como **Traço** apaga traços inteiros. Definir a **propriedade EraserMode** como **Point** apaga a tinta que o cursor passa.

 

 



