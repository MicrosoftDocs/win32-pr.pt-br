---
title: Função MpManagerOpen (MpClient. h)
description: Estabelece uma conexão com o Malware Protection Manager no computador local.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Recursos do ambiente Windows herdado da função MpManagerOpen
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645070"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="69b02-104">Função MpManagerOpen</span><span class="sxs-lookup"><span data-stu-id="69b02-104">MpManagerOpen function</span></span>

<span data-ttu-id="69b02-105">Estabelece uma conexão com o Malware Protection Manager no computador local.</span><span class="sxs-lookup"><span data-stu-id="69b02-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69b02-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="69b02-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69b02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b02-108">*dwReserved* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69b02-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b02-109">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="69b02-109">Type: **DWORD**</span></span>

<span data-ttu-id="69b02-110">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="69b02-110">Reserved for future use.</span></span> <span data-ttu-id="69b02-111">Deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="69b02-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="69b02-112">*phMpHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="69b02-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69b02-113">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="69b02-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="69b02-114">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="69b02-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="69b02-115">Esse identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="69b02-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b02-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69b02-116">Return value</span></span>

<span data-ttu-id="69b02-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="69b02-117">Type: **HRESULT**</span></span>

<span data-ttu-id="69b02-118">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69b02-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="69b02-119">Essa chamada de função tem garantia de sucesso mesmo que um serviço Antimalware não esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="69b02-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="69b02-120">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="69b02-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="69b02-121">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="69b02-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b02-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69b02-122">Requirements</span></span>



| <span data-ttu-id="69b02-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="69b02-123">Requirement</span></span> | <span data-ttu-id="69b02-124">Valor</span><span class="sxs-lookup"><span data-stu-id="69b02-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69b02-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b02-125">Minimum supported client</span></span><br/> | <span data-ttu-id="69b02-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="69b02-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="69b02-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69b02-127">Minimum supported server</span></span><br/> | <span data-ttu-id="69b02-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="69b02-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="69b02-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69b02-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b02-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="69b02-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="69b02-131">DLL</span><span class="sxs-lookup"><span data-stu-id="69b02-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69b02-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69b02-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b02-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="69b02-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b02-134">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="69b02-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="69b02-135">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="69b02-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





