---
description: Uma função de retorno de chamada usada para notificar o host das informações da pilha de chamadas.
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método ICallStackCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825821"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="b48d3-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>Método ICallStackCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="b48d3-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="b48d3-104">Uma função de retorno de chamada usada para notificar o host das informações da pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="b48d3-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b48d3-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="b48d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b48d3-106">Parameters</span></span>

<span data-ttu-id="b48d3-107">*contar* </span><span class="sxs-lookup"><span data-stu-id="b48d3-107">*count* </span></span>  
<span data-ttu-id="b48d3-108">O número de framebuffers de pilha de chamadas retornado.</span><span class="sxs-lookup"><span data-stu-id="b48d3-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="b48d3-109">*count0 \_ callStackFrameBuffer* </span><span class="sxs-lookup"><span data-stu-id="b48d3-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="b48d3-110">As informações de pilha de chamadas.</span><span class="sxs-lookup"><span data-stu-id="b48d3-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="b48d3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b48d3-111">Return value</span></span>

<span data-ttu-id="b48d3-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b48d3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b48d3-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b48d3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48d3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b48d3-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b48d3-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b48d3-115">Header</span></span></p></td><td><span data-ttu-id="b48d3-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b48d3-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b48d3-117"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="b48d3-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b48d3-118">**ICallStackCallback**</span><span class="sxs-lookup"><span data-stu-id="b48d3-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 
