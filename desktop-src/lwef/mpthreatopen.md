---
title: Função MpThreatOpen (MpClient. h)
description: Retorna um identificador de enumeração para a finalidade de recuperar ameaças.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Recursos do ambiente Windows herdado da função MpThreatOpen
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769367"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="c0176-104">Função MpThreatOpen</span><span class="sxs-lookup"><span data-stu-id="c0176-104">MpThreatOpen function</span></span>

<span data-ttu-id="c0176-105">Retorna um identificador de enumeração para a finalidade de recuperar ameaças.</span><span class="sxs-lookup"><span data-stu-id="c0176-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="c0176-106">Essa função pode ser usada para abrir ameaças detectadas por uma verificação específica, todas as ameaças ativas no sistema, o histórico de desinfecção de ameaças ou todas as ameaças presentes no banco de dados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c0176-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0176-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0176-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="c0176-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0176-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0176-109">*hScanHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0176-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0176-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="c0176-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="c0176-111">Pode ser um identificador para uma operação de verificação concluída, retornada pela função [**MpScanStart**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="c0176-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="c0176-112">Como alternativa, esse parâmetro pode ser definido como o identificador de interface do Malware Protection Manager retornado por [**MpManagerOpen**](mpmanageropen.md) para enumerar todas as ameaças ativas no sistema, o histórico de desinfecção de ameaças ou ameaças do banco de dados de assinatura.</span><span class="sxs-lookup"><span data-stu-id="c0176-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="c0176-113">*Ameaçador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0176-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0176-114">Tipo: **\_ origem do MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c0176-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="c0176-115">Usado para controlar a origem da enumeração de ameaças.</span><span class="sxs-lookup"><span data-stu-id="c0176-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="c0176-116">Os valores possíveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c0176-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="c0176-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c0176-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="c0176-118">Significado</span><span class="sxs-lookup"><span data-stu-id="c0176-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="c0176-119"><dt>**\_verificação de origem do MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="c0176-120">Ameaças associadas ao identificador de verificação específico.</span><span class="sxs-lookup"><span data-stu-id="c0176-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="c0176-121"><dt>**\_origem MPTHREAT \_ ativa**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="c0176-122">Ameaças atualmente ativas no sistema.</span><span class="sxs-lookup"><span data-stu-id="c0176-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="c0176-123"><dt>**MPTHREAT \_ histórico de origem \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="c0176-124">Ameaças que são acionadas e preservadas como um histórico.</span><span class="sxs-lookup"><span data-stu-id="c0176-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="c0176-125"><dt>**\_quarentena de origem do MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="c0176-126">Ameaças que estão em quarentena.</span><span class="sxs-lookup"><span data-stu-id="c0176-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="c0176-127"><dt>**\_assinatura de origem do MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="c0176-128">Ameaças que são possíveis detectar com o banco de dados de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c0176-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="c0176-129"><dt>**\_estado de origem do MPTHREAT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="c0176-130">Ameaças que foram acionadas recentemente.</span><span class="sxs-lookup"><span data-stu-id="c0176-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="c0176-131">("Recentemente" é definido por uma configuração interna configurável.)</span><span class="sxs-lookup"><span data-stu-id="c0176-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c0176-132">*Threattype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0176-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0176-133">Tipo: **\_ tipo de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="c0176-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="c0176-134">Usado para filtrar ameaças enumeradas com base no tipo de detecção.</span><span class="sxs-lookup"><span data-stu-id="c0176-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="c0176-135">Os valores possíveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c0176-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="c0176-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c0176-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="c0176-137">Significado</span><span class="sxs-lookup"><span data-stu-id="c0176-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="c0176-138"><dt>**MPTHREAT \_ tipo \_ KNOWNBAD**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="c0176-139">A detecção é executada com base em uma assinatura, emulação ou outro método de detecção de ameaças específico.</span><span class="sxs-lookup"><span data-stu-id="c0176-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="c0176-140"><dt>**tipo de MPTHREAT \_ \_ suspeito**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="c0176-141">A detecção é executada com base no monitoramento de comportamento.</span><span class="sxs-lookup"><span data-stu-id="c0176-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="c0176-142"><dt>**tipo de MPTHREAT \_ \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="c0176-143">A detecção é executada com base em ameaças desconhecidas (não classificadas).</span><span class="sxs-lookup"><span data-stu-id="c0176-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="c0176-144"><dt>**MPTHREAT \_ tipo \_ KNOWNGOOD**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="c0176-145">A detecção é realizada com base em ameaças seguras conhecidas.</span><span class="sxs-lookup"><span data-stu-id="c0176-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="c0176-146"><dt>**MPTHREAT \_ tipo \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="c0176-147">A detecção é realizada com base em ameaças NIS.</span><span class="sxs-lookup"><span data-stu-id="c0176-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="c0176-148">*phThreatEnumHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0176-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0176-149">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="c0176-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="c0176-150">Identificador de enumeração de ameaça retornado que identifica o contexto de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c0176-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="c0176-151">Esse identificador pode ser usado para enumerar informações de ameaças usando o [**MpThreatEnumerate**](mpthreatenumerate.md).</span><span class="sxs-lookup"><span data-stu-id="c0176-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="c0176-152">O identificador deve ser fechado com a função [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="c0176-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0176-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0176-153">Return value</span></span>

<span data-ttu-id="c0176-154">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c0176-154">Type: **HRESULT**</span></span>

<span data-ttu-id="c0176-155">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c0176-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="c0176-156">Se a função falhar, o valor de retorno será um código **HRESULT** com falha.</span><span class="sxs-lookup"><span data-stu-id="c0176-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="c0176-157">O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="c0176-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0176-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0176-158">Requirements</span></span>



| <span data-ttu-id="c0176-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0176-159">Requirement</span></span> | <span data-ttu-id="c0176-160">Valor</span><span class="sxs-lookup"><span data-stu-id="c0176-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0176-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0176-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c0176-162">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c0176-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c0176-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0176-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c0176-164">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c0176-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0176-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0176-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0176-166"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0176-167">DLL</span><span class="sxs-lookup"><span data-stu-id="c0176-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0176-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0176-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0176-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0176-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0176-170">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="c0176-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="c0176-171">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="c0176-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="c0176-172">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="c0176-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="c0176-173">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="c0176-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="c0176-174">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="c0176-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 





