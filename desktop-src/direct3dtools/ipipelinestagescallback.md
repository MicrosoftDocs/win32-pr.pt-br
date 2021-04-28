---
description: <span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback – não usada. Anteriormente, um retorno de chamada para dados de estágios de pipeline.
MS-HAID: vspixengine.IPipeLineStagesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2F5B84DB-3D06-4D82-BF1D-E5853CC4B835
api_name:
- IPipeLineStagesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7782985f4317a02d2b159722f7a5897978b952b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087894"
---
# <a name="span-idvspixengineipipelinestagescallbackspanipipelinestagescallback-interface"></a><span data-ttu-id="1ad7c-104"><span id="vspixengine.ipipelinestagescallback"></span>Interface IPipeLineStagesCallback</span><span class="sxs-lookup"><span data-stu-id="1ad7c-104"><span id="vspixengine.ipipelinestagescallback"></span>IPipeLineStagesCallback interface</span></span>

<span data-ttu-id="1ad7c-105">Não usado.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-105">Not used.</span></span> <span data-ttu-id="1ad7c-106">Anteriormente, um retorno de chamada para dados de estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-106">Formerly a callback for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="1ad7c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1ad7c-107">Members</span></span>

<span data-ttu-id="1ad7c-108">A interface **IPipeLineStagesCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1ad7c-108">The **IPipeLineStagesCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1ad7c-109">**IPipeLineStagesCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1ad7c-109">**IPipeLineStagesCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="1ad7c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ad7c-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="1ad7c-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="1ad7c-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="1ad7c-112">A interface **IPipeLineStagesCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-112">The **IPipeLineStagesCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="1ad7c-113">Método</span><span class="sxs-lookup"><span data-stu-id="1ad7c-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="1ad7c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ad7c-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1ad7c-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span><span class="sxs-lookup"><span data-stu-id="1ad7c-115"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-getsupportedstages-dword-pipelinestage-arr-uint-uint"><strong>GetSupportedStages</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1ad7c-116">Um retorno de chamada que notifica o host de quais estágios de pipeline são usados pela chamada de desenho da solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-116">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="1ad7c-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1ad7c-117"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatanotavailablecallback-uint-pipelinestageerror-arr-uint-uint-eventid"><strong>MeshDataNotAvailableCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1ad7c-118">Um retorno de chamada que notifica o host de quais estágios de pipeline não podem retornar dados de malha para o evento especificado na solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-118">A callback that notifies the host of which pipeline stages are not able to return mesh data for the event specified in the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1ad7c-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1ad7c-119"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-meshdatavertcallback-uint-uint-meshdatabufferlayoutentry-arr-uint-uint-byte-arr-uint-byte-arr-uint-uint-uint-uint-bool-uint-uint"><strong>MeshDataVertCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1ad7c-120">Um retorno de chamada que notifica o host do pipeline prepara as informações de malha retornadas pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-120">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="1ad7c-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="1ad7c-121"><a href="/windows/desktop/direct3dtools/ipipelinestagescallback-resultcallback-pipelinestagesid-eventid-dword-dword-dword-dword-byte-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1ad7c-122">Um retorno de chamada que notifica o host de fases de estágios de pipeline informações de imagem retornadas pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="1ad7c-122">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="1ad7c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ad7c-123">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1ad7c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ad7c-124">Header</span></span></p></td><td><span data-ttu-id="1ad7c-125">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1ad7c-125">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
