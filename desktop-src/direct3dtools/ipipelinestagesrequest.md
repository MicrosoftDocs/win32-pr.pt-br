---
description: Não usado. Anteriormente uma solicitação de dados de estágios de pipeline.
MS-HAID: vspixengine.IPipeLineStagesRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPipeLineStagesRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6EB81F-F60F-49CF-9F34-FABDA05ED3F8
api_name:
- IPipeLineStagesRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4dfa67e0770b1c709ee80bffd01831859ad4c45a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105781639"
---
# <a name="span-idvspixengineipipelinestagesrequestspanipipelinestagesrequest-interface"></a><span data-ttu-id="439e7-104"><span id="vspixengine.ipipelinestagesrequest"></span>Interface IPipeLineStagesRequest</span><span class="sxs-lookup"><span data-stu-id="439e7-104"><span id="vspixengine.ipipelinestagesrequest"></span>IPipeLineStagesRequest interface</span></span>

<span data-ttu-id="439e7-105">Não usado.</span><span class="sxs-lookup"><span data-stu-id="439e7-105">Not used.</span></span> <span data-ttu-id="439e7-106">Anteriormente uma solicitação de dados de estágios de pipeline.</span><span class="sxs-lookup"><span data-stu-id="439e7-106">Formerly a request for pipeline stages data.</span></span>

## <a name="members"></a><span data-ttu-id="439e7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="439e7-107">Members</span></span>

<span data-ttu-id="439e7-108">A interface **IPipeLineStagesRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="439e7-108">The **IPipeLineStagesRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="439e7-109">**IPipeLineStagesRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="439e7-109">**IPipeLineStagesRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="439e7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="439e7-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="439e7-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="439e7-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="439e7-112">A interface **IPipeLineStagesRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="439e7-112">The **IPipeLineStagesRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="439e7-113">Método</span><span class="sxs-lookup"><span data-stu-id="439e7-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="439e7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="439e7-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="439e7-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="439e7-115"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestasync-eventid-dword-pipelinestagesid-arr-dword-dword-ipipelinestagescallback-ptr-bool-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="439e7-116">Uma solicitação assíncrona para obter imagens de visualização para a janela de estágios de pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="439e7-116">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="439e7-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="439e7-117"><a href="/windows/desktop/direct3dtools/ipipelinestagesrequest-requestsupportedstagesasync-dword-eventid-ipipelinestagescallback-ptr-dword-dword"><strong>RequestSupportedStagesAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="439e7-118">Uma solicitação assíncrona para obter uma lista de estágios usados para o quadro e o evento especificados.</span><span class="sxs-lookup"><span data-stu-id="439e7-118">An asynchronous request to get a list of stages used for the specified frame and event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="439e7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="439e7-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="439e7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="439e7-120">Header</span></span></p></td><td><span data-ttu-id="439e7-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="439e7-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
