---
title: Tempo (multimídia do Windows)
description: Timing
ms.assetid: 9ab284c7-eebc-4b44-b9e1-cc95efde22c1
keywords:
- DrawDib, tempo
- Função DrawDibTime
- DrawDib, depuração
- Depurando DrawDib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adddd43ff5067d08334a40f2e52e79109c8a8bb7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454528"
---
# <a name="timing-windows-multimedia"></a><span data-ttu-id="3dd2b-107">Tempo (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="3dd2b-107">Timing (Windows Multimedia)</span></span>

<span data-ttu-id="3dd2b-108">Como parte da depuração de um aplicativo, você pode obter informações sobre a quantidade de tempo necessária para concluir operações DrawDib repetitivas.</span><span class="sxs-lookup"><span data-stu-id="3dd2b-108">As part of debugging an application, you can obtain information about the amount of time required to complete repetitive DrawDib operations.</span></span> <span data-ttu-id="3dd2b-109">A função [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) retorna informações de tempo para as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="3dd2b-109">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function returns timing information for the following operations:</span></span>

-   <span data-ttu-id="3dd2b-110">Desenhando um bitmap</span><span class="sxs-lookup"><span data-stu-id="3dd2b-110">Drawing a bitmap</span></span>
-   <span data-ttu-id="3dd2b-111">Descompactando um bitmap</span><span class="sxs-lookup"><span data-stu-id="3dd2b-111">Decompressing a bitmap</span></span>
-   <span data-ttu-id="3dd2b-112">Pontilhamento de um bitmap</span><span class="sxs-lookup"><span data-stu-id="3dd2b-112">Dithering a bitmap</span></span>
-   <span data-ttu-id="3dd2b-113">Alongando um bitmap</span><span class="sxs-lookup"><span data-stu-id="3dd2b-113">Stretching a bitmap</span></span>
-   <span data-ttu-id="3dd2b-114">Transferindo um bitmap usando a função [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt)</span><span class="sxs-lookup"><span data-stu-id="3dd2b-114">Transferring a bitmap by using the [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) function</span></span>
-   <span data-ttu-id="3dd2b-115">Transferindo um bitmap usando a função [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)</span><span class="sxs-lookup"><span data-stu-id="3dd2b-115">Transferring a bitmap by using the [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) function</span></span>

<span data-ttu-id="3dd2b-116">Depois de recuperar um conjunto de valores, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) redefine a contagem e o valor de cada operação.</span><span class="sxs-lookup"><span data-stu-id="3dd2b-116">After retrieving a set of values, [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) resets the count and value for each operation.</span></span>

<span data-ttu-id="3dd2b-117">A função [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) está disponível apenas na versão de depuração das funções DrawDib.</span><span class="sxs-lookup"><span data-stu-id="3dd2b-117">The [**DrawDibTime**](/windows/desktop/api/Vfw/nf-vfw-drawdibtime) function is available only in the debug version of the DrawDib functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dd2b-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3dd2b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dd2b-119">Renderização de imagem</span><span class="sxs-lookup"><span data-stu-id="3dd2b-119">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 
