---
description: Consultando recursos de busca
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Consultando recursos de busca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825907"
---
# <a name="querying-for-seeking-capabilities"></a><span data-ttu-id="a1bcd-103">Consultando recursos de busca</span><span class="sxs-lookup"><span data-stu-id="a1bcd-103">Querying for Seeking Capabilities</span></span>

<span data-ttu-id="a1bcd-104">O Microsoft® DirectShow® oferece suporte à busca pela interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="a1bcd-104">Microsoft® DirectShow® supports seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="a1bcd-105">O Gerenciador de gráfico de filtro expõe essa interface, mas a funcionalidade de busca sempre é implementada por filtros no grafo.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-105">The Filter Graph Manager exposes this interface, but the seeking functionality is always implemented by filters in the graph.</span></span>

<span data-ttu-id="a1bcd-106">Alguns dados não podem ser procurados.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-106">Some data cannot be seeked.</span></span> <span data-ttu-id="a1bcd-107">Por exemplo, você não pode buscar um fluxo de vídeo ao vivo de uma câmera.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-107">For example, you cannot seek a live video stream from a camera.</span></span> <span data-ttu-id="a1bcd-108">No entanto, se um fluxo é pesquisável, há vários tipos de busca que ele pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-108">If a stream is seekable, however, there are various types of seeking it might support.</span></span> <span data-ttu-id="a1bcd-109">Estão incluídos:</span><span class="sxs-lookup"><span data-stu-id="a1bcd-109">These include:</span></span>

-   <span data-ttu-id="a1bcd-110">Buscando uma posição arbitrária no fluxo.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-110">Seeking to an arbitrary position in the stream.</span></span>
-   <span data-ttu-id="a1bcd-111">Recuperando a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-111">Retrieving the duration of the stream.</span></span>
-   <span data-ttu-id="a1bcd-112">Recuperando a posição atual dentro do fluxo.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-112">Retrieving the current position within the stream.</span></span>
-   <span data-ttu-id="a1bcd-113">Tocando em ordem inversa.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-113">Playing in reverse.</span></span>

<span data-ttu-id="a1bcd-114">A interface **IMediaSeeking** define um conjunto de sinalizadores, [**está \_ buscando \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), que descrevem os possíveis recursos de busca.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-114">The **IMediaSeeking** interface defines a set of flags, [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), that describe the possible seeking capabilities.</span></span> <span data-ttu-id="a1bcd-115">Para recuperar os recursos do Stream, chame o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="a1bcd-115">To retrieve the stream's capabilities, call the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="a1bcd-116">O método retorna uma combinação de bits de bit que não é possível.</span><span class="sxs-lookup"><span data-stu-id="a1bcd-116">The method returns a bitwise combination of flags.</span></span> <span data-ttu-id="a1bcd-117">O aplicativo pode testá-los usando o operador de & ( **and** and).</span><span class="sxs-lookup"><span data-stu-id="a1bcd-117">The application can test them using the & (bitwise **AND**) operator.</span></span> <span data-ttu-id="a1bcd-118">Por exemplo, o código a seguir verifica se o grafo pode buscar uma posição arbitrária:</span><span class="sxs-lookup"><span data-stu-id="a1bcd-118">For example, the following code checks whether the graph can seek to an arbitrary position:</span></span>


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



