---
title: Função MpManagerStatusQueryEx (MpClient. h)
description: Retorna informações de status sobre vários componentes do Malware Protection Manager. | Função MpManagerStatusQueryEx (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Recursos do ambiente Windows herdado da função MpManagerStatusQueryEx
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105758146"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="403e4-105">Função MpManagerStatusQueryEx</span><span class="sxs-lookup"><span data-stu-id="403e4-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="403e4-106">Retorna informações de status sobre vários componentes do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="403e4-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="403e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="403e4-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="403e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="403e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403e4-109">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="403e4-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403e4-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="403e4-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="403e4-111">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="403e4-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="403e4-112">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="403e4-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="403e4-113">*dwFlag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="403e4-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403e4-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="403e4-114">Type: **DWORD**</span></span>

<span data-ttu-id="403e4-115">Controla quais informações de consulta são retornadas.</span><span class="sxs-lookup"><span data-stu-id="403e4-115">Controls which query information is returned.</span></span> <span data-ttu-id="403e4-116">Algumas informações são caras e podem não ser necessárias.</span><span class="sxs-lookup"><span data-stu-id="403e4-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="403e4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="403e4-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="403e4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="403e4-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="403e4-119"><dt>**sinalizadores de consulta de status do MP \_ \_ \_ \_ nenhum**</dt></span><span class="sxs-lookup"><span data-stu-id="403e4-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="403e4-120">Padrão.</span><span class="sxs-lookup"><span data-stu-id="403e4-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="403e4-121"><dt>**sinalizador de consulta de status do MP \_ \_ \_ \_ nostate**</dt></span><span class="sxs-lookup"><span data-stu-id="403e4-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="403e4-122">Não consulte informações de estado.</span><span class="sxs-lookup"><span data-stu-id="403e4-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="403e4-123">*pStatusInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="403e4-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="403e4-124">Tipo: **\_ informações de PMPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="403e4-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="403e4-125">Ponteiro para uma estrutura que retorna informações de status sobre as últimas verificações, ameaças ativas e vários status de componente.</span><span class="sxs-lookup"><span data-stu-id="403e4-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="403e4-126">Consulte [**MPSTATUS \_ info**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="403e4-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403e4-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="403e4-127">Return value</span></span>

<span data-ttu-id="403e4-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="403e4-128">Type: **HRESULT**</span></span>

<span data-ttu-id="403e4-129">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="403e4-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="403e4-130">Essa chamada de função tem garantia de sucesso mesmo que um serviço Antimalware não esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="403e4-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="403e4-131">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="403e4-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="403e4-132">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="403e4-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="403e4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="403e4-133">Requirements</span></span>



| <span data-ttu-id="403e4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="403e4-134">Requirement</span></span> | <span data-ttu-id="403e4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="403e4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="403e4-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="403e4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="403e4-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="403e4-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="403e4-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="403e4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="403e4-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="403e4-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="403e4-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="403e4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="403e4-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="403e4-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="403e4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="403e4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="403e4-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="403e4-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="403e4-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="403e4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403e4-145">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="403e4-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="403e4-146">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="403e4-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="403e4-147">**informações de MPSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="403e4-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





