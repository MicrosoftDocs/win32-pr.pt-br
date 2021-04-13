---
description: Extensões para a interface IPixEngine original.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixEngine2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456508"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span data-ttu-id="c2f4f-103"><span id="vspixengine.ipixengine2"></span>Interface IPixEngine2</span><span class="sxs-lookup"><span data-stu-id="c2f4f-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 interface</span></span>

<span data-ttu-id="c2f4f-104">Extensões para a interface IPixEngine original.</span><span class="sxs-lookup"><span data-stu-id="c2f4f-104">Extensions to the original IPixEngine interface.</span></span>

## <a name="members"></a><span data-ttu-id="c2f4f-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c2f4f-105">Members</span></span>

<span data-ttu-id="c2f4f-106">A interface **IPixEngine2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c2f4f-106">The **IPixEngine2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c2f4f-107">**IPixEngine2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c2f4f-107">**IPixEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="c2f4f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2f4f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="c2f4f-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="c2f4f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="c2f4f-110">A interface **IPixEngine2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c2f4f-110">The **IPixEngine2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="c2f4f-111">Método</span><span class="sxs-lookup"><span data-stu-id="c2f4f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="c2f4f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2f4f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c2f4f-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>Endexperimento</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2f4f-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c2f4f-114">Encerra o experiement e conclui o log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="c2f4f-114">Ends the experiement and completes the graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c2f4f-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2f4f-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c2f4f-116">Obtém informações sobre o computador de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="c2f4f-116">Gets information about the current playback machine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="c2f4f-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2f4f-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c2f4f-118">Solicitações para indicar que o log de gráficos tem novos dados dentro dele.</span><span class="sxs-lookup"><span data-stu-id="c2f4f-118">Requests to indicate that the graphics log has new data inside of it.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="c2f4f-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="c2f4f-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="c2f4f-120">Define o computador de reprodução atual para o log de gráficos especificado.</span><span class="sxs-lookup"><span data-stu-id="c2f4f-120">Sets the current playback machine for the specified graphics log.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="c2f4f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f4f-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c2f4f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2f4f-122">Header</span></span></p></td><td><span data-ttu-id="c2f4f-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c2f4f-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
