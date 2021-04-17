---
description: Per-Pixel mesclagem alfa
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel mesclagem alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789826"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="6a887-103">Per-Pixel mesclagem alfa</span><span class="sxs-lookup"><span data-stu-id="6a887-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="6a887-104">Quatro subtipos de mídia foram definidos para mesclagem alfa por pixel.</span><span class="sxs-lookup"><span data-stu-id="6a887-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="6a887-105">Esses subtipos só têm suporte quando o VMR está no modo de mistura.</span><span class="sxs-lookup"><span data-stu-id="6a887-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="6a887-106">O VMR rejeitará a conexão se não estiver no modo de mistura quando um filtro upstream tentar se conectar usando um desses subtipos.</span><span class="sxs-lookup"><span data-stu-id="6a887-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="6a887-107">Esses subtipos são definidos em UUIDs. h:</span><span class="sxs-lookup"><span data-stu-id="6a887-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="6a887-108">MEDIASUBTYPE \_ ARGB1555</span><span class="sxs-lookup"><span data-stu-id="6a887-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="6a887-109">MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="6a887-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="6a887-110">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="6a887-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="6a887-111">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="6a887-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="6a887-112">Para obter mais informações, consulte [subtipos de vídeo RGB não compactados](uncompressed-rgb-video-subtypes.md) e [**subtipos de vídeo YUV**](yuv-video-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="6a887-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



