---
title: Função MpScanControl (MpClient. h)
description: Permite o controle de uma verificação que foi iniciada de forma assíncrona via MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Recursos do ambiente Windows herdado da função MpScanControl
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455073"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="1f608-104">Função MpScanControl</span><span class="sxs-lookup"><span data-stu-id="1f608-104">MpScanControl function</span></span>

<span data-ttu-id="1f608-105">Permite o controle de uma verificação que foi iniciada de forma assíncrona via [**MpScanStart**](mpscanstart.md).</span><span class="sxs-lookup"><span data-stu-id="1f608-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f608-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f608-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="1f608-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f608-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f608-108">*hScanHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f608-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f608-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="1f608-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="1f608-110">Identificador para uma operação de verificação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1f608-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="1f608-111">Esse identificador é retornado pela função [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="1f608-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="1f608-112">Esse parâmetro também pode ser definido como o identificador de interface do Malware Protection Manager retornado pela função [**MpManagerOpen**](mpmanageropen.md) para controlar uma verificação iniciada pelo sistema; nesse caso, o chamador deve ter privilégio administrativo.</span><span class="sxs-lookup"><span data-stu-id="1f608-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="1f608-113">*ScanControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f608-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f608-114">Tipo: **MPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="1f608-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="1f608-115">Especifica uma opção de controle de verificação.</span><span class="sxs-lookup"><span data-stu-id="1f608-115">Specifies a scan control option.</span></span> <span data-ttu-id="1f608-116">Esse parâmetro deve ser uma das seguintes opções de controle:</span><span class="sxs-lookup"><span data-stu-id="1f608-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="1f608-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1f608-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="1f608-118">Significado</span><span class="sxs-lookup"><span data-stu-id="1f608-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="1f608-119"><dt>**\_anular MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="1f608-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="1f608-120">Anule a operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="1f608-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="1f608-121"><dt>**Pausar MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f608-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="1f608-122">Pause a operação de verificação.</span><span class="sxs-lookup"><span data-stu-id="1f608-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="1f608-123"><dt>**retomar MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f608-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="1f608-124">Retome a operação de verificação em pausa.</span><span class="sxs-lookup"><span data-stu-id="1f608-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f608-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f608-125">Return value</span></span>

<span data-ttu-id="1f608-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1f608-126">Type: **HRESULT**</span></span>

<span data-ttu-id="1f608-127">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1f608-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="1f608-128">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="1f608-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="1f608-129">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="1f608-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f608-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f608-130">Requirements</span></span>



| <span data-ttu-id="1f608-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f608-131">Requirement</span></span> | <span data-ttu-id="1f608-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1f608-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f608-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f608-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f608-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f608-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1f608-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f608-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f608-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1f608-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f608-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f608-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f608-138"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f608-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f608-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1f608-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f608-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f608-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f608-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f608-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f608-142">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="1f608-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="1f608-143">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="1f608-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="1f608-144">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="1f608-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





