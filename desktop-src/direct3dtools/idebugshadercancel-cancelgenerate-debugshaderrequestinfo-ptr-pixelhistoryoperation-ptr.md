---
description: Solicitações para cancelar a geração de instruções de rastreamento de sombreador em uma solicitação de depuração.
MS-HAID: vspixengine.IDebugShaderCancel\_CancelGenerate\_DebugShaderRequestInfo\_ptr\_PixelHistoryOperation\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IDebugShaderCancel:: CancelGenerate'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10DA5080-3AA6-47AA-BFE7-774BC26C7F95
api_name:
- IDebugShaderCancel.CancelGenerate
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c2754f0d390960775b11ac5da121d5e6a20705a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105798444"
---
# <a name="span-idvspixengineidebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptrspanidebugshadercancelcancelgenerate-method"></a><span data-ttu-id="aed8a-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>Método IDebugShaderCancel:: CancelGenerate</span><span class="sxs-lookup"><span data-stu-id="aed8a-103"><span id="vspixengine.idebugshadercancel_cancelgenerate_debugshaderrequestinfo_ptr_pixelhistoryoperation_ptr"></span>IDebugShaderCancel::CancelGenerate method</span></span>

<span data-ttu-id="aed8a-104">Solicitações para cancelar a geração de instruções de rastreamento de sombreador em uma solicitação de depuração.</span><span class="sxs-lookup"><span data-stu-id="aed8a-104">Requests to cancel generation of shader trace instructions in a debug request.</span></span>

## <a name="syntax"></a><span data-ttu-id="aed8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aed8a-105">Syntax</span></span>


```C++
HRESULT CancelGenerate(
   DebugShaderRequestInfo * requestInfo,
   PixelHistoryOperation *  pPixelHistory
);
```

## <a name="parameters"></a><span data-ttu-id="aed8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aed8a-106">Parameters</span></span>

<span data-ttu-id="aed8a-107">*requestInfo* </span><span class="sxs-lookup"><span data-stu-id="aed8a-107">*requestInfo* </span></span>  
<span data-ttu-id="aed8a-108">O endereço de uma estrutura DebugShaderRequestInfo que descreve o evento/vértice/pixel solicitado.</span><span class="sxs-lookup"><span data-stu-id="aed8a-108">The address of a DebugShaderRequestInfo structure that describes the requested event/vertex/pixel.</span></span>

<span data-ttu-id="aed8a-109">*pPixelHistory* </span><span class="sxs-lookup"><span data-stu-id="aed8a-109">*pPixelHistory* </span></span>  
<span data-ttu-id="aed8a-110">O endereço dos resultados do histórico de pixel usado para localizar o pixel associado a ser depurado.</span><span class="sxs-lookup"><span data-stu-id="aed8a-110">The address of pixel history results used for finding the associated pixel to debug.</span></span> <span data-ttu-id="aed8a-111">Aplica-se somente ao depurar um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="aed8a-111">Only applies when debugging a pixel shader.</span></span>

## <a name="return-value"></a><span data-ttu-id="aed8a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aed8a-112">Return value</span></span>

<span data-ttu-id="aed8a-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aed8a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aed8a-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aed8a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aed8a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aed8a-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="aed8a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aed8a-116">Header</span></span></p></td><td><span data-ttu-id="aed8a-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="aed8a-117">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="aed8a-118"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="aed8a-118"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="aed8a-119">**IDebugShaderCancel**</span><span class="sxs-lookup"><span data-stu-id="aed8a-119">**IDebugShaderCancel**</span></span>](/windows/desktop/direct3dtools/idebugshadercancel)

 

 
