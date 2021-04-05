---
description: Solicita que o estado do TPM seja alterado para o valor especificado no parâmetro RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Método RequestTPMStateChange da classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921387"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="b3ee4-103">Método RequestTPMStateChange da classe CIM \_ TPM</span><span class="sxs-lookup"><span data-stu-id="b3ee4-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="b3ee4-104">Solicita que o estado do TPM seja alterado para o valor especificado no parâmetro *RequestedTPMState* .</span><span class="sxs-lookup"><span data-stu-id="b3ee4-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="b3ee4-105">Se a invocação do método for concluída com êxito, a propriedade **TPMState** deverá ser igual ao parâmetro **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="b3ee4-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="b3ee4-106">Invocar o método **RequestTPMStateChange** várias vezes pode resultar em solicitações anteriores sendo substituídas ou perdidas.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ee4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3ee4-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b3ee4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3ee4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ee4-109">*RequestedTPMState* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3ee4-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ee4-110">Os Estados de TPM solicitados.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="b3ee4-111">**S1 habilitado – ativo-de propriedade** (2)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="b3ee4-112">**S2 desabilitado-ativo-proprietário** (3)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="b3ee4-113">**S3 habilitado-inativo-de propriedade** (4)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="b3ee4-114">**S4 desabilitado-inativo-de propriedade** (5)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="b3ee4-115">**S5 habilitado-ativo-sem proprietário** (6)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="b3ee4-116">**S6 desabilitado – ativo-sem proprietário** (7)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="b3ee4-117">**S7 habilitado – inativo – sem proprietário** (8)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="b3ee4-118">**S8 desabilitado-inativo – sem proprietário** (9)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b3ee4-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b3ee4-120">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b3ee4-121">*AuthorizationToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3ee4-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ee4-122">Token de autorização que pode ser necessário para que a ação entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="b3ee4-123">O parâmetro *AuthorizationToken* pode ser necessário para estabelecer a presença física ou para passar o OwnerAuth, a senha de autorização do proprietário definido pelo TCG.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="b3ee4-124">No caso do OwnerAuth, o SharedCredential CIM \_ com valor não nulo do CIM \_ SharedCredential. Secret pode ser necessário.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="b3ee4-125">A \_ Propriedade CIM SharedCredential. Algorithm também pode ser especificada com base na propriedade CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="b3ee4-126">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b3ee4-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ee4-127">Pode conter uma referência para o [**CIM \_ ConcreteJob**](cim-concretejob.md) criado para acompanhar a transição de estado iniciada pela invocação de método.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="b3ee4-128">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3ee4-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3ee4-129">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="b3ee4-130">O formato do intervalo deve ser usado para especificar o *TimeoutPeriod*.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="b3ee4-131">Um valor 0 ou um parâmetro nulo indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ee4-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3ee4-132">Return value</span></span>

<span data-ttu-id="b3ee4-133">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="b3ee4-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b3ee4-134">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-135">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-136">**Erro desconhecido ou não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-137">**Não é possível concluir dentro do período de tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-138">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-139">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-140">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-141">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-142">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-143">**Transição de estado inválida** (4097)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-144">**Não há suporte para o uso do parâmetro timeout** (4098)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-145">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-146">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b3ee4-147">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b3ee4-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b3ee4-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3ee4-148">Requirements</span></span>



| <span data-ttu-id="b3ee4-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3ee4-149">Requirement</span></span> | <span data-ttu-id="b3ee4-150">Valor</span><span class="sxs-lookup"><span data-stu-id="b3ee4-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ee4-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3ee4-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b3ee4-152">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b3ee4-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b3ee4-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3ee4-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b3ee4-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b3ee4-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b3ee4-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3ee4-155">Namespace</span></span><br/>                | <span data-ttu-id="b3ee4-156">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b3ee4-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b3ee4-157">MOF</span><span class="sxs-lookup"><span data-stu-id="b3ee4-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3ee4-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3ee4-159">DLL</span><span class="sxs-lookup"><span data-stu-id="b3ee4-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3ee4-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3ee4-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3ee4-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3ee4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ee4-162">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="b3ee4-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




