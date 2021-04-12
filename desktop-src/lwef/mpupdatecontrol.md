---
title: Função MpUpdateControl (MpClient. h)
description: Permite o controle de uma operação de atualização de assinatura que foi iniciada de forma assíncrona via MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Recursos do ambiente Windows herdado da função MpUpdateControl
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455459"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="f57cb-104">Função MpUpdateControl</span><span class="sxs-lookup"><span data-stu-id="f57cb-104">MpUpdateControl function</span></span>

<span data-ttu-id="f57cb-105">Permite o controle de uma operação de atualização de assinatura que foi iniciada de forma assíncrona via [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="f57cb-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="f57cb-106">Chamar essa função requer privilégio de administrador, pois permite o cancelamento de uma atualização de assinatura em todo o sistema.</span><span class="sxs-lookup"><span data-stu-id="f57cb-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="f57cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f57cb-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="f57cb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f57cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f57cb-109">*hUpdateHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f57cb-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f57cb-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="f57cb-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="f57cb-111">Identificador para uma operação de atualização de assinatura assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f57cb-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="f57cb-112">Esse identificador é retornado pela função [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="f57cb-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f57cb-113">*UpdateControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f57cb-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f57cb-114">Tipo: **MPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="f57cb-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="f57cb-115">Especifica a opção de controle de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f57cb-115">Specifies the signature update control option.</span></span> <span data-ttu-id="f57cb-116">Ele deve ser o seguinte valor:</span><span class="sxs-lookup"><span data-stu-id="f57cb-116">It must be the following value:</span></span>



| <span data-ttu-id="f57cb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f57cb-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="f57cb-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f57cb-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="f57cb-119"><dt>**\_anular MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="f57cb-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="f57cb-120">Anule a operação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f57cb-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f57cb-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f57cb-121">Return value</span></span>

<span data-ttu-id="f57cb-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f57cb-122">Type: **HRESULT**</span></span>

<span data-ttu-id="f57cb-123">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f57cb-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="f57cb-124">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="f57cb-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="f57cb-125">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="f57cb-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f57cb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f57cb-126">Requirements</span></span>



| <span data-ttu-id="f57cb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f57cb-127">Requirement</span></span> | <span data-ttu-id="f57cb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f57cb-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f57cb-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f57cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f57cb-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f57cb-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f57cb-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f57cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f57cb-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f57cb-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f57cb-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f57cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f57cb-134"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f57cb-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f57cb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f57cb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f57cb-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f57cb-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f57cb-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f57cb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f57cb-138">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="f57cb-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="f57cb-139">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="f57cb-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





