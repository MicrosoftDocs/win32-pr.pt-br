---
description: Acesso a superfícies do DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Acesso a superfícies do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825994"
---
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="63d84-103">Acesso a superfícies do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="63d84-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="63d84-104">Os objetos de exemplo de mídia fornecidos pelo VMR para filtros upstream dão suporte à interface [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) .</span><span class="sxs-lookup"><span data-stu-id="63d84-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="63d84-105">Para obter a interface, chame QueryInterface na interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) e especifique IID \_ IVMRSurface.</span><span class="sxs-lookup"><span data-stu-id="63d84-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="63d84-106">Os filtros upstream podem usar os métodos IVMRSurface para acessar e manipular a superfície que foi criada pelo VMR.</span><span class="sxs-lookup"><span data-stu-id="63d84-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63d84-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="63d84-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63d84-108">Usando o VMR para desenvolvedores de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="63d84-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



