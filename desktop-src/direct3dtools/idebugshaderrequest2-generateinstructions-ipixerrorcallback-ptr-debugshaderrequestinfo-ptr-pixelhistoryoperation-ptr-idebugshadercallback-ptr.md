---
description: Solicitações para gerar instruções de rastreamento de sombreador em uma solicitação de depuração. A depuração baseada em rastreamento ocorre na CPU (Warp) em vez da GPU.
MS-HAID: vspixengine.IDebugShaderRequest2\_GenerateInstructions\_IPixErrorCallback\_ptr\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr\_IDebugShaderCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IDebugShaderRequest2:: GenerateInstructions'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50685D38-AA85-43D7-9199-12B3776708C2
api_name:
- IDebugShaderRequest2.GenerateInstructions
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9c1bc2f6b3f885159f21cd7e644545d7639d6b3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500502"
---
# <a name="span-idvspixengineidebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptrspanidebugshaderrequest2generateinstructions-method"></a><span data-ttu-id="0023a-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>Método IDebugShaderRequest2:: GenerateInstructions</span><span class="sxs-lookup"><span data-stu-id="0023a-104"><span id="vspixengine.idebugshaderrequest2_generateinstructions_ipixerrorcallback_ptr_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr_idebugshadercallback_ptr"></span>IDebugShaderRequest2::GenerateInstructions method</span></span>

<span data-ttu-id="0023a-105">Solicitações para gerar instruções de rastreamento de sombreador em uma solicitação de depuração.</span><span class="sxs-lookup"><span data-stu-id="0023a-105">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="0023a-106">A depuração baseada em rastreamento ocorre na CPU (Warp) em vez da GPU.</span><span class="sxs-lookup"><span data-stu-id="0023a-106">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="0023a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0023a-107">Syntax</span></span>


```C++
HRESULT GenerateInstructions(
   IPixErrorCallback *      errorCallback,
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory,
   IDebugShaderCallback *   pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="0023a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0023a-108">Parameters</span></span>

<span data-ttu-id="0023a-109">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="0023a-109">*errorCallback* </span></span>  
<span data-ttu-id="0023a-110">O endereço de um retorno de chamada para erros que podem ocorrer durante a geração de instruções de rastreamento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0023a-110">The address of a callback for errors that might occur while generating shader trace instructions.</span></span>

<span data-ttu-id="0023a-111">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="0023a-111">*requestInfo* </span></span>  
<span data-ttu-id="0023a-112">O endereço de uma estrutura DebugShaderRequestInfo que descreve o evento/vértice/pixel solicitado.</span><span class="sxs-lookup"><span data-stu-id="0023a-112">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="0023a-113">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="0023a-113">*pPixelHistory* </span></span>  
<span data-ttu-id="0023a-114">O endereço dos resultados do histórico de pixel usado para localizar o pixel associado a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="0023a-114">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="0023a-115">Aplica-se somente ao depurar um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="0023a-115">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="0023a-116">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="0023a-116">*pCallback* </span></span>  
<span data-ttu-id="0023a-117">O endereço de um retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="0023a-117">The address of a callback used to notify the host of results.</span></span>

## <a name="return-value"></a><span data-ttu-id="0023a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0023a-118">Return value</span></span>

<span data-ttu-id="0023a-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0023a-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0023a-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0023a-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0023a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0023a-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0023a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0023a-122">Header</span></span></p></td><td><span data-ttu-id="0023a-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0023a-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0023a-124"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="0023a-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0023a-125">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="0023a-125">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
