---
title: Função MpThreatQuery (MpClient. h)
description: Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição da categoria e conselhos) sobre uma determinada ameaça.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Recursos do ambiente Windows herdado da função MpThreatQuery
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757178"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="cac5e-104">Função MpThreatQuery</span><span class="sxs-lookup"><span data-stu-id="cac5e-104">MpThreatQuery function</span></span>

<span data-ttu-id="cac5e-105">Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição da categoria e conselhos) sobre uma determinada ameaça.</span><span class="sxs-lookup"><span data-stu-id="cac5e-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac5e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cac5e-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cac5e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cac5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac5e-108">*hMpHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cac5e-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac5e-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="cac5e-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="cac5e-110">Identificador para a interface do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="cac5e-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="cac5e-111">Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="cac5e-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="cac5e-112">*Threatid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cac5e-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac5e-113">Tipo: **\_ ID de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cac5e-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="cac5e-114">Identificador de ameaça para o qual as informações são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="cac5e-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="cac5e-115">*ppThreatInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cac5e-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cac5e-116">Tipo: \**PMPTHREAT \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="cac5e-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="cac5e-117">Retorna um ponteiro para uma estrutura de informações de ameaça, [_ *MPTHREAT \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="cac5e-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="cac5e-118">A estrutura contém informações como ID de ameaça, nome e severidade.</span><span class="sxs-lookup"><span data-stu-id="cac5e-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="cac5e-119">*ppThreatLocalizedInfo* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cac5e-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cac5e-120">Tipo: \**PMPTHREAT \_ \_ informações \* localizadas* _</span><span class="sxs-lookup"><span data-stu-id="cac5e-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="cac5e-121">Retorna um ponteiro para uma estrutura que contém informações localizadas sobre a ameaça.</span><span class="sxs-lookup"><span data-stu-id="cac5e-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="cac5e-122">Você pode passar _ *NULL*\* se não estiver interessado em informações localizadas sobre a ameaça.</span><span class="sxs-lookup"><span data-stu-id="cac5e-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="cac5e-123">Consulte [**\_ informações localizadas \_ sobre o MPTHREAT**](mpthreat-localized-info.md).</span><span class="sxs-lookup"><span data-stu-id="cac5e-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac5e-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cac5e-124">Return value</span></span>

<span data-ttu-id="cac5e-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cac5e-125">Type: **HRESULT**</span></span>

<span data-ttu-id="cac5e-126">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cac5e-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="cac5e-127">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="cac5e-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="cac5e-128">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="cac5e-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac5e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac5e-129">Requirements</span></span>



| <span data-ttu-id="cac5e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac5e-130">Requirement</span></span> | <span data-ttu-id="cac5e-131">Valor</span><span class="sxs-lookup"><span data-stu-id="cac5e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cac5e-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac5e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cac5e-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cac5e-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cac5e-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac5e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cac5e-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cac5e-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cac5e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cac5e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac5e-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac5e-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cac5e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cac5e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac5e-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac5e-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac5e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="cac5e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac5e-141">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="cac5e-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="cac5e-142">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="cac5e-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="cac5e-143">**informações de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="cac5e-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="cac5e-144">**\_informações localizadas do MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="cac5e-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





