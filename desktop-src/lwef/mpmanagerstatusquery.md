---
title: Função MpManagerStatusQuery (MpClient. h)
description: Retorna informações de status sobre vários componentes do Malware Protection Manager. | Função MpManagerStatusQuery (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Recursos do ambiente Windows herdado da função MpManagerStatusQuery
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298099"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="62508-105">Função MpManagerStatusQuery</span><span class="sxs-lookup"><span data-stu-id="62508-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="62508-106">\[**MpManagerStatusQuery** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="62508-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="62508-107">Em vez disso, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span><span class="sxs-lookup"><span data-stu-id="62508-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="62508-108">Retorna informações de status sobre vários componentes do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="62508-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="62508-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62508-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="62508-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62508-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62508-111">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62508-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62508-112">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="62508-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="62508-113">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="62508-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="62508-114">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="62508-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="62508-115">*pStatusInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62508-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62508-116">Tipo: **\_ informações de PMPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="62508-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="62508-117">Ponteiro para uma estrutura que retorna informações de status sobre as últimas verificações, ameaças ativas e vários status de componente.</span><span class="sxs-lookup"><span data-stu-id="62508-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="62508-118">Consulte [**MPSTATUS \_ info**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="62508-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62508-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62508-119">Return value</span></span>

<span data-ttu-id="62508-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="62508-120">Type: **HRESULT**</span></span>

<span data-ttu-id="62508-121">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62508-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="62508-122">Essa chamada de função tem garantia de sucesso mesmo que um serviço Antimalware não esteja em execução.</span><span class="sxs-lookup"><span data-stu-id="62508-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="62508-123">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="62508-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="62508-124">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="62508-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="62508-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62508-125">Requirements</span></span>



| <span data-ttu-id="62508-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="62508-126">Requirement</span></span> | <span data-ttu-id="62508-127">Valor</span><span class="sxs-lookup"><span data-stu-id="62508-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62508-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62508-128">Minimum supported client</span></span><br/> | <span data-ttu-id="62508-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="62508-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="62508-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62508-130">Minimum supported server</span></span><br/> | <span data-ttu-id="62508-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="62508-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62508-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62508-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="62508-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="62508-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="62508-134">DLL</span><span class="sxs-lookup"><span data-stu-id="62508-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62508-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62508-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62508-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="62508-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62508-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="62508-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="62508-138">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="62508-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="62508-139">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="62508-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="62508-140">**informações de MPSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="62508-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





