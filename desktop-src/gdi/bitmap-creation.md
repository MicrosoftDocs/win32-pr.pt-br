---
description: Para criar um bitmap, use a função CreateBitmap, CreateBitmapIndirect ou CreateCompatibleBitmap, CreateDIBitmap e CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Criação de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165096"
---
# <a name="bitmap-creation"></a><span data-ttu-id="d531f-103">Criação de bitmap</span><span class="sxs-lookup"><span data-stu-id="d531f-103">Bitmap Creation</span></span>

<span data-ttu-id="d531f-104">Para criar um bitmap, use a função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span><span class="sxs-lookup"><span data-stu-id="d531f-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="d531f-105">Essas funções permitem que você especifique a largura e a altura, em pixels, do bitmap.</span><span class="sxs-lookup"><span data-stu-id="d531f-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="d531f-106">A função [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) também permitem que você especifique o número de planos de cores e o número de bits necessários para identificar a cor.</span><span class="sxs-lookup"><span data-stu-id="d531f-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="d531f-107">Por outro lado, as funções [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) e [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) usam um contexto de dispositivo especificado para obter o número de planos de cores e o número de bits necessários para identificar a cor.</span><span class="sxs-lookup"><span data-stu-id="d531f-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="d531f-108">A função [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) cria um bitmap dependente de dispositivo de um bitmap independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d531f-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="d531f-109">Ele contém uma tabela de cores que descreve como os valores de pixel correspondem aos valores de cor RGB.</span><span class="sxs-lookup"><span data-stu-id="d531f-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="d531f-110">Para obter mais informações, consulte [bitmaps dependentes de dispositivo](device-dependent-bitmaps.md) e [bitmaps independentes de dispositivo](device-independent-bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="d531f-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="d531f-111">Depois que o bitmap tiver sido criado, você não poderá alterar seu tamanho, o número de planos de cores ou o número de bits necessários para identificar a cor.</span><span class="sxs-lookup"><span data-stu-id="d531f-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="d531f-112">Quando você não precisar mais de um bitmap, chame a função [**ExcluirObjeto**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) para excluí-lo.</span><span class="sxs-lookup"><span data-stu-id="d531f-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



