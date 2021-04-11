---
description: Não usado. Anteriormente uma solicitação de dados de estágios de pipeline.
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
ms.openlocfilehash: 9d344b7e128adf344f50a99ba41a420ca794baec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087428"
---
# <a name="span-idvspixengineipipelinestagesrequest2spanipipelinestagesrequest2-interface"></a><span data-ttu-id="b4c53-104"><span id="vspixengine.ipipelinestagesrequest2"></span>Interface IPipeLineStagesRequest2</span><span class="sxs-lookup"><span data-stu-id="b4c53-104"><span id="vspixengine.ipipelinestagesrequest2"></span>IPipeLineStagesRequest2 interface</span></span>

<span data-ttu-id="b4c53-105">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b4c53-105">Not used.</span></span> <span data-ttu-id="b4c53-106">Anteriormente uma solicitação de dados de estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b4c53-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="b4c53-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b4c53-107">Members</span></span>

<span data-ttu-id="b4c53-108">A interface **IPipeLineStagesRequest2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b4c53-108">The **IPipeLineStagesRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b4c53-109">**IPipeLineStagesRequest2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b4c53-109">**IPipeLineStagesRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="b4c53-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4c53-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="b4c53-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="b4c53-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="b4c53-112">A interface **IPipeLineStagesRequest2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b4c53-112">The **IPipeLineStagesRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="b4c53-113">Método</span><span class="sxs-lookup"><span data-stu-id="b4c53-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="b4c53-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4c53-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="b4c53-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4c53-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderdataasync-eventid-ipipelinestagescallback2-ptr-dword-dword"><strong>RequestComputeShaderDataAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b4c53-116">Uma solicitação assíncrona para obter dados do sombreador de computação para o despacho especificado.</span><span class="sxs-lookup"><span data-stu-id="b4c53-116">An asynchronous request to get compute shader data for the specified dispatch.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="b4c53-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4c53-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest2-requestcomputeshaderstageasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestComputeShaderStageAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b4c53-118">Uma solicitação assíncrona para obter se o estágio de sombreador de computação foi usado para o quadro e o evento especificados.</span><span class="sxs-lookup"><span data-stu-id="b4c53-118">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="b4c53-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4c53-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b4c53-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4c53-120">Header</span></span></p></td><td><span data-ttu-id="b4c53-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b4c53-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
