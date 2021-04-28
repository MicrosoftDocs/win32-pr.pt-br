---
description: <span id="vspixengine.ipipelinestagesrequest2"></span>Interface IPipeLineStagesRequest2 – não usada. Anteriormente uma solicitação de dados de estágios de pipeline.
MS-HAID: vspixengine.IPipeLineStagesRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B40E0701-3F17-4B3A-B150-D4B243662042
api_name:
- IPipeLineStagesRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9dd185ba709aa4439deb98f92be3c8f2f456cea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107064"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="c1938-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Interface IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="c1938-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="c1938-105">Não usado.</span><span class="sxs-lookup"><span data-stu-id="c1938-105">Not used.</span></span> <span data-ttu-id="c1938-106">Anteriormente uma solicitação de dados de estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1938-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="c1938-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c1938-107">Members</span></span>

<span data-ttu-id="c1938-108">A interface **IPipeLineStagesRequest2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c1938-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c1938-109">**IPipeLineStagesRequest2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1938-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="c1938-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c1938-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c1938-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c1938-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c1938-112">A interface **IPipeLineStagesRequest2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c1938-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c1938-113">Método</span><span class="sxs-lookup"><span data-stu-id="c1938-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c1938-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1938-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c1938-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1938-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c1938-116">Uma solicitação assíncrona para obter dados do sombreador de computação para o despacho especificado.</span><span class="sxs-lookup"><span data-stu-id="c1938-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c1938-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="c1938-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c1938-118">Uma solicitação assíncrona para obter se o estágio de sombreador de computação foi usado para o quadro e o evento especificados.</span><span class="sxs-lookup"><span data-stu-id="c1938-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c1938-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1938-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c1938-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1938-120">Header</span></span></p></td><td><span data-ttu-id="c1938-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c1938-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
