---
description: 'Solicitação para iniciar a depuração de um sombreador. Essa solicitação contém duas partes: gerar um rastreamento e depurar um rastreamento.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087640"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="295bc-104"><span id="vspixengine.idebugshaderrequest2"></span>Interface IDebugShaderRequest2</span><span class="sxs-lookup"><span data-stu-id="295bc-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="295bc-105">Solicitação para iniciar a depuração de um sombreador.</span><span class="sxs-lookup"><span data-stu-id="295bc-105">Request to start debugging a shader.</span></span> <span data-ttu-id="295bc-106">Essa solicitação contém duas partes: gerar um rastreamento e depurar um rastreamento.</span><span class="sxs-lookup"><span data-stu-id="295bc-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="295bc-107">Membros</span><span class="sxs-lookup"><span data-stu-id="295bc-107">Members</span></span>

<span data-ttu-id="295bc-108">A interface **IDebugShaderRequest2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="295bc-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="295bc-109">**IDebugShaderRequest2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="295bc-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="295bc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="295bc-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="295bc-111"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="295bc-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="295bc-112">A interface **IDebugShaderRequest2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="295bc-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="295bc-113">Método</span><span class="sxs-lookup"><span data-stu-id="295bc-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="295bc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="295bc-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="295bc-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="295bc-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="295bc-116">Solicitações para iniciar a depuração da lista de instruções especificada.</span><span class="sxs-lookup"><span data-stu-id="295bc-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="295bc-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="295bc-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="295bc-118">Solicitações para gerar instruções de rastreamento de sombreador em uma solicitação de depuração.</span><span class="sxs-lookup"><span data-stu-id="295bc-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="295bc-119">A depuração baseada em rastreamento ocorre na CPU (Warp) em vez da GPU.</span><span class="sxs-lookup"><span data-stu-id="295bc-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="295bc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="295bc-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="295bc-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="295bc-121">Header</span></span></p></td><td><span data-ttu-id="295bc-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="295bc-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
