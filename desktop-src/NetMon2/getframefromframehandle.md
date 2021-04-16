---
description: A função GetFrameFromFrameHandle retorna um ponteiro para um quadro de um identificador de quadro.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Função GetFrameFromFrameHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757500"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="d988c-103">Função GetFrameFromFrameHandle</span><span class="sxs-lookup"><span data-stu-id="d988c-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="d988c-104">A função **GetFrameFromFrameHandle** retorna um ponteiro para um quadro de um identificador de quadro.</span><span class="sxs-lookup"><span data-stu-id="d988c-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d988c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d988c-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="d988c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d988c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d988c-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d988c-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d988c-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="d988c-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d988c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d988c-109">Return value</span></span>

<span data-ttu-id="d988c-110">Se a função for bem-sucedida, o valor de retorno será um ponteiro para o quadro.</span><span class="sxs-lookup"><span data-stu-id="d988c-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="d988c-111">Se a função não for bem-sucedida, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="d988c-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d988c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d988c-112">Remarks</span></span>

<span data-ttu-id="d988c-113">A função **GetFrameFromFrameHandle** recupera dados que não podem ser recuperados por outras funções auxiliares que o monitor de rede fornece.</span><span class="sxs-lookup"><span data-stu-id="d988c-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="d988c-114">Use as funções a seguir sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="d988c-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="d988c-115">**GetFrameDstAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="d988c-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="d988c-116">**GetFrameSrcAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="d988c-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="d988c-117">**GetFrameCaptureHandle**</span><span class="sxs-lookup"><span data-stu-id="d988c-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="d988c-118">**GetFrameDestAddress**</span><span class="sxs-lookup"><span data-stu-id="d988c-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="d988c-119">**GetFrameSourceAddress**</span><span class="sxs-lookup"><span data-stu-id="d988c-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="d988c-120">**GetFrameMacHeaderLength**</span><span class="sxs-lookup"><span data-stu-id="d988c-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="d988c-121">**GetFrameLength**</span><span class="sxs-lookup"><span data-stu-id="d988c-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="d988c-122">**GetFrameStoredLength**</span><span class="sxs-lookup"><span data-stu-id="d988c-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="d988c-123">**GetFrameMacType**</span><span class="sxs-lookup"><span data-stu-id="d988c-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="d988c-124">**GetFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="d988c-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="d988c-125">**GetFrameTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="d988c-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="d988c-126">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameFromFrameHandle** .</span><span class="sxs-lookup"><span data-stu-id="d988c-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d988c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d988c-127">Requirements</span></span>



| <span data-ttu-id="d988c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d988c-128">Requirement</span></span> | <span data-ttu-id="d988c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d988c-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d988c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d988c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d988c-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d988c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d988c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d988c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d988c-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d988c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d988c-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d988c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d988c-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d988c-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d988c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d988c-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="d988c-137"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d988c-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d988c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d988c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d988c-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d988c-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




