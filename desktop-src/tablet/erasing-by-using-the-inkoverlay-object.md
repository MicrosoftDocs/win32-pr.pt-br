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
# <a name="erasing-by-using-the-inkoverlay-object"></a><span data-ttu-id="4681c-103">Apagando usando o objeto InkOverlay</span><span class="sxs-lookup"><span data-stu-id="4681c-103">Erasing by Using the InkOverlay Object</span></span>

<span data-ttu-id="4681c-104">O objeto [**InkOverlay**](inkoverlay-class.md) pode ser anexado a um controle Window e é usado para habilitar a capacidade básica de tinta.</span><span class="sxs-lookup"><span data-stu-id="4681c-104">The [**InkOverlay**](inkoverlay-class.md) object can be attached to a window control and is used to enable basic ink capability.</span></span> <span data-ttu-id="4681c-105">Você pode usar o objeto **InkOverlay** para apagar a tinta definindo a propriedade [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) igual a **delete**.</span><span class="sxs-lookup"><span data-stu-id="4681c-105">You can use the **InkOverlay** object to erase ink by setting the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) property equal to **Delete**.</span></span> <span data-ttu-id="4681c-106">Em seguida, você pode definir a propriedade [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) para os membros de **traço** ou **ponto** de [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span><span class="sxs-lookup"><span data-stu-id="4681c-106">You can then set the [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) property to either the **Stroke** or **Point** members of [**InkOverlayEraserMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode).</span></span> <span data-ttu-id="4681c-107">Definir a propriedade **EraserMode** como **Stroke** apaga traços inteiros.</span><span class="sxs-lookup"><span data-stu-id="4681c-107">Setting the **EraserMode** property to **Stroke** erases entire strokes.</span></span> <span data-ttu-id="4681c-108">Definir a propriedade **EraserMode** como **Point** apaga a tinta que o cursor passa.</span><span class="sxs-lookup"><span data-stu-id="4681c-108">Setting the **EraserMode** property to **Point** erases the ink that the cursor passes over.</span></span>

 

 



