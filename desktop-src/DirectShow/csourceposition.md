---
description: CSourcePosition é uma classe abstrata para implementar a interface IMediaPosition em um filtro de origem.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Classe CSourcePosition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105748017"
---
# <a name="csourceposition-class"></a><span data-ttu-id="1390f-103">Classe CSourcePosition</span><span class="sxs-lookup"><span data-stu-id="1390f-103">CSourcePosition class</span></span>

<span data-ttu-id="1390f-104">`CSourcePosition` é uma classe abstrata para implementar a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) em um filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="1390f-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="1390f-105">Essa classe está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="1390f-105">This class is obsolete.</span></span> <span data-ttu-id="1390f-106">Se o filtro de origem for pesquisável, ele deverá expor a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) em vez de **IMediaPosition**.</span><span class="sxs-lookup"><span data-stu-id="1390f-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="1390f-107">Você pode usar a classe base [**CSourceSeeking**](csourceseeking.md) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="1390f-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



