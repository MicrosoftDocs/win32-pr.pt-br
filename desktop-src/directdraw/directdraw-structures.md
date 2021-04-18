---
title: Estruturas do DirectDraw
description: Esta seção contém informações sobre as seguintes estruturas usadas com o DirectDraw
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "105781386"
---
# <a name="directdraw-structures"></a><span data-ttu-id="4e572-103">Estruturas do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="4e572-103">DirectDraw Structures</span></span>

<span data-ttu-id="4e572-104">Esta seção contém informações sobre as seguintes estruturas usadas com o DirectDraw:</span><span class="sxs-lookup"><span data-stu-id="4e572-104">This section contains information about the following structures used with DirectDraw:</span></span>

-   [<span data-ttu-id="4e572-105">**DDBLTBATCH**</span><span class="sxs-lookup"><span data-stu-id="4e572-105">**DDBLTBATCH**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [<span data-ttu-id="4e572-106">**DDBLTFX**</span><span class="sxs-lookup"><span data-stu-id="4e572-106">**DDBLTFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [<span data-ttu-id="4e572-107">**DDCAPS**</span><span class="sxs-lookup"><span data-stu-id="4e572-107">**DDCAPS**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [<span data-ttu-id="4e572-108">**DDCOLORCONTROL**</span><span class="sxs-lookup"><span data-stu-id="4e572-108">**DDCOLORCONTROL**</span></span>](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [<span data-ttu-id="4e572-109">**DDCOLORKEY**</span><span class="sxs-lookup"><span data-stu-id="4e572-109">**DDCOLORKEY**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [<span data-ttu-id="4e572-110">**DDDEVICEIDENTIFIER2**</span><span class="sxs-lookup"><span data-stu-id="4e572-110">**DDDEVICEIDENTIFIER2**</span></span>](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [<span data-ttu-id="4e572-111">**DDGAMMARAMP**</span><span class="sxs-lookup"><span data-stu-id="4e572-111">**DDGAMMARAMP**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [<span data-ttu-id="4e572-112">**DDOVERLAYFX**</span><span class="sxs-lookup"><span data-stu-id="4e572-112">**DDOVERLAYFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [<span data-ttu-id="4e572-113">**DDPIXELFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4e572-113">**DDPIXELFORMAT**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   <span data-ttu-id="4e572-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e572-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span></span>
-   <span data-ttu-id="4e572-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e572-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span></span>
-   <span data-ttu-id="4e572-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e572-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span></span>
-   <span data-ttu-id="4e572-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e572-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span></span>

> [!Note]  
> <span data-ttu-id="4e572-118">Você deve inicializar a memória para cada estrutura do DirectX para 0 antes de usar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="4e572-118">You should initialize the memory for each DirectX structure to 0 before you use the structure.</span></span> <span data-ttu-id="4e572-119">Além disso, para todas as estruturas que contêm um membro **dwSize** , você deve definir o membro como o tamanho da estrutura, em bytes, antes que a estrutura seja usada.</span><span class="sxs-lookup"><span data-stu-id="4e572-119">In addition, for all structures that contain a **dwSize** member, you should set the member to the size of the structure, in bytes, before the structure is used.</span></span> <span data-ttu-id="4e572-120">O exemplo a seguir executa essas tarefas em uma estrutura comum, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span><span class="sxs-lookup"><span data-stu-id="4e572-120">The following example performs these tasks on a common structure, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span></span>

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




