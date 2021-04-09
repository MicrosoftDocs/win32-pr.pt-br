---
description: Solicitações para iniciar a depuração da lista de instruções especificada.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IDebugShaderRequest2:: BeginDebugShader'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087642"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="6ccf7-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>Método IDebugShaderRequest2:: BeginDebugShader</span><span class="sxs-lookup"><span data-stu-id="6ccf7-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="6ccf7-104">Solicitações para iniciar a depuração da lista de instruções especificada.</span><span class="sxs-lookup"><span data-stu-id="6ccf7-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ccf7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ccf7-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="6ccf7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ccf7-106">Parameters</span></span>

<span data-ttu-id="6ccf7-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="6ccf7-107">*errorCallback* </span></span>  
<span data-ttu-id="6ccf7-108">O endereço de um retorno de chamada para erros que podem ocorrer durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="6ccf7-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="6ccf7-109">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="6ccf7-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="6ccf7-110">O número de instruções no fluxo de instrução.</span><span class="sxs-lookup"><span data-stu-id="6ccf7-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="6ccf7-111">*count1 \_ instructionStream* </span><span class="sxs-lookup"><span data-stu-id="6ccf7-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="6ccf7-112">O fluxo de instrução especificado.</span><span class="sxs-lookup"><span data-stu-id="6ccf7-112">The specified instruction stream.</span></span>

<span data-ttu-id="6ccf7-113">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="6ccf7-113">*pDevice* </span></span>  
<span data-ttu-id="6ccf7-114">O endereço a ser passado para o mecanismo de depuração para comunicação com esta sessão de depuração (ReadProcessMemory do mecanismo de depuração neste endereço).</span><span class="sxs-lookup"><span data-stu-id="6ccf7-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="6ccf7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ccf7-115">Return value</span></span>

<span data-ttu-id="6ccf7-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6ccf7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ccf7-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ccf7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ccf7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ccf7-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6ccf7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ccf7-119">Header</span></span></p></td><td><span data-ttu-id="6ccf7-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6ccf7-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6ccf7-121"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="6ccf7-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6ccf7-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="6ccf7-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
