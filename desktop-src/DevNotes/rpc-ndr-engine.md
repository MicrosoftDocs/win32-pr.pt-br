---
description: Mecanismo de NDR de RPC
ms.assetid: FD6365A9-6EC2-407D-B397-09A91BF02379
title: Mecanismo NDR de RPC (notas do desenvolvedor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39eeb38d99e01dd8ab5683cf0289b3e7e09d45f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750395"
---
# <a name="rpc-ndr-engine-developer-notes"></a><span data-ttu-id="5acaa-103">Mecanismo NDR de RPC (notas do desenvolvedor)</span><span class="sxs-lookup"><span data-stu-id="5acaa-103">RPC NDR Engine (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5acaa-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5acaa-104">In this section</span></span>

-   [<span data-ttu-id="5acaa-105">**NdrComplexArrayBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5acaa-105">**NdrComplexArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraybuffersize)
-   [<span data-ttu-id="5acaa-106">**NdrComplexArrayMarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-106">**NdrComplexArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraymarshall)
-   [<span data-ttu-id="5acaa-107">**NdrComplexArrayUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-107">**NdrComplexArrayUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarrayunmarshall)
-   [<span data-ttu-id="5acaa-108">**NdrComplexStructBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5acaa-108">**NdrComplexStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructbuffersize)
-   [<span data-ttu-id="5acaa-109">**NdrComplexStructMarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-109">**NdrComplexStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructmarshall)
-   [<span data-ttu-id="5acaa-110">**NdrComplexStructUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-110">**NdrComplexStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructunmarshall)
-   [<span data-ttu-id="5acaa-111">**NdrComformantArrayBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5acaa-111">**NdrComformantArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraybuffersize)
-   [<span data-ttu-id="5acaa-112">**NdrComformantArrayMarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-112">**NdrComformantArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraymarshall)
-   [<span data-ttu-id="5acaa-113">**NdrSimpleStructBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5acaa-113">**NdrSimpleStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructbuffersize)
-   [<span data-ttu-id="5acaa-114">**NdrSimpleStructMarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-114">**NdrSimpleStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructmarshall)
-   [<span data-ttu-id="5acaa-115">**NdrSimpleStructUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-115">**NdrSimpleStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructunmarshall)
-   [<span data-ttu-id="5acaa-116">**NdrUserMarshalUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="5acaa-116">**NdrUserMarshalUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalunmarshall)

 

 



