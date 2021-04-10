---
description: Solicitações para iniciar uma sessão de depuração de sombreador para o estágio de pipeline especificado, pixel/vértice, se aplicável, evento e quadro.
MS-HAID: vspixengine.IDebugShaderRequest\_BeginDebugShader\_IPixErrorCallback\_ptr\_EventID\_DWORD\_DWORD\_Point2D\_PipeLineStages\_PixelHistoryOperation\_ptr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IDebugShaderRequest:: BeginDebugShader'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC93D31C-8593-4B03-B974-87B886B9431D
api_name:
- IDebugShaderRequest.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b6512dc8aa67b3f4d128be3cd2dcd2b622ba2035
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087643"
---
# <a name="span-idvspixengineidebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptrspanidebugshaderrequestbegindebugshader-method"></a><span data-ttu-id="6b7b4-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>Método IDebugShaderRequest:: BeginDebugShader</span><span class="sxs-lookup"><span data-stu-id="6b7b4-103"><span id="vspixengine.idebugshaderrequest_begindebugshader_ipixerrorcallback_ptr_eventid_dword_dword_point2d_pipelinestages_pixelhistoryoperation_ptr_dword_ptr"></span>IDebugShaderRequest::BeginDebugShader method</span></span>

<span data-ttu-id="6b7b4-104">Solicitações para iniciar uma sessão de depuração de sombreador para o estágio de pipeline especificado, pixel/vértice, se aplicável, evento e quadro.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-104">Requests to start a shader debugging session for the specified pipeline stage, pixel/vertex if applicable, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b7b4-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback *     errorCallback,
   EventID                 eventID,
   DWORD                   frameNumber,
   DWORD                   vertex,
   Point2D                 pixel,
   PipeLineStages          stage,
   PixelHistoryOperation * pPixelHistory,
   DWORD *                 pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="6b7b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b7b4-106">Parameters</span></span>

<span data-ttu-id="6b7b4-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-107">*errorCallback* </span></span>  
<span data-ttu-id="6b7b4-108">O endereço de um retorno de chamada para erros que podem ocorrer durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="6b7b4-109">*1008* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-109">*eventID* </span></span>  
<span data-ttu-id="6b7b4-110">O evento especificado.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-110">The specified event.</span></span>

<span data-ttu-id="6b7b4-111">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-111">*frameNumber* </span></span>  
<span data-ttu-id="6b7b4-112">O quadro especificado.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-112">The specified frame.</span></span>

<span data-ttu-id="6b7b4-113">*deles* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-113">*vertex* </span></span>  
<span data-ttu-id="6b7b4-114">O vértice especificado.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-114">The specified vertex.</span></span> <span data-ttu-id="6b7b4-115">Aplica-se somente ao depurar um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-115">Only applies when debugging a vertex shader.</span></span>

<span data-ttu-id="6b7b4-116">*16x16* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-116">*pixel* </span></span>  
<span data-ttu-id="6b7b4-117">O pixel especificado.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-117">The specified pixel.</span></span> <span data-ttu-id="6b7b4-118">Aplica-se somente ao depurar um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-118">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="6b7b4-119">*Test* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-119">*stage* </span></span>  
<span data-ttu-id="6b7b4-120">O estágio de pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-120">The specified pipeline stage.</span></span>

<span data-ttu-id="6b7b4-121">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-121">*pPixelHistory* </span></span>  
<span data-ttu-id="6b7b4-122">O endereço dos resultados do histórico de pixel usado para localizar o pixel associado a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-122">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="6b7b4-123">Aplica-se somente ao depurar um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-123">Only applies when debugging a pixel shader.</span></span>

<span data-ttu-id="6b7b4-124">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="6b7b4-124">*pDevice* </span></span>  
<span data-ttu-id="6b7b4-125">O endereço a ser passado para o mecanismo de depuração para comunicação com esta sessão de depuração (ReadProcessMemory do mecanismo de depuração neste endereço).</span><span class="sxs-lookup"><span data-stu-id="6b7b4-125">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="6b7b4-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b7b4-126">Return value</span></span>

<span data-ttu-id="6b7b4-127">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6b7b4-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b7b4-128">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b7b4-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7b4-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b7b4-129">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6b7b4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b7b4-130">Header</span></span></p></td><td><span data-ttu-id="6b7b4-131">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6b7b4-131">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6b7b4-132"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="6b7b4-132"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6b7b4-133">**IDebugShaderRequest**</span><span class="sxs-lookup"><span data-stu-id="6b7b4-133">**IDebugShaderRequest**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest)

 

 
