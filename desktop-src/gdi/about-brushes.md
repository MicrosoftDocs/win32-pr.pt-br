---
description: 'Há dois tipos de pincéis: lógico e físico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Sobre pincéis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090979"
---
# <a name="about-brushes"></a><span data-ttu-id="5054f-103">Sobre pincéis</span><span class="sxs-lookup"><span data-stu-id="5054f-103">About Brushes</span></span>

<span data-ttu-id="5054f-104">Há dois tipos de pincéis: lógico e físico.</span><span class="sxs-lookup"><span data-stu-id="5054f-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="5054f-105">Um *pincel lógico* é uma descrição do bitmap ideal que um aplicativo usa para pintar formas.</span><span class="sxs-lookup"><span data-stu-id="5054f-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="5054f-106">Um *pincel físico* é o bitmap real que um driver de dispositivo cria com base na definição de pincel lógico de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5054f-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="5054f-107">Para obter mais informações sobre bitmaps, consulte [bitmaps](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="5054f-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="5054f-108">Quando um aplicativo chama uma das funções que cria um pincel, ele recupera um identificador que identifica um pincel lógico.</span><span class="sxs-lookup"><span data-stu-id="5054f-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="5054f-109">Quando o aplicativo passa esse identificador para a função [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , o driver de dispositivo para a exibição ou impressora correspondente cria o pincel físico.</span><span class="sxs-lookup"><span data-stu-id="5054f-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="5054f-110">Os tópicos a seguir descrevem os pincéis:</span><span class="sxs-lookup"><span data-stu-id="5054f-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="5054f-111">Origem do pincel</span><span class="sxs-lookup"><span data-stu-id="5054f-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="5054f-112">Tipos de pincel lógico</span><span class="sxs-lookup"><span data-stu-id="5054f-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="5054f-113">Transferência de bloco de padrão</span><span class="sxs-lookup"><span data-stu-id="5054f-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="5054f-114">Funções de pincel habilitadas para ICM</span><span class="sxs-lookup"><span data-stu-id="5054f-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



