---
description: Solicita que o estado do elemento seja alterado.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Método RequestStateChange da classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921017"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="71f0a-103">Método RequestStateChange da classe de \_ teclado Msvm</span><span class="sxs-lookup"><span data-stu-id="71f0a-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="71f0a-104">Solicita que o estado do elemento seja alterado.</span><span class="sxs-lookup"><span data-stu-id="71f0a-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f0a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71f0a-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="71f0a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71f0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f0a-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71f0a-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f0a-108">O novo estado solicitado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="71f0a-108">The new state requested for the element.</span></span> <span data-ttu-id="71f0a-109">Essas informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno for 0 (' concluído sem erro '), 3 (' timeout ') ou 4096 (0x1000) (' trabalho iniciado ').</span><span class="sxs-lookup"><span data-stu-id="71f0a-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="71f0a-110">Para obter explicações detalhadas dos valores *requestedstate* , consulte a descrição das propriedades **enabledstate** e **requestedstate** .</span><span class="sxs-lookup"><span data-stu-id="71f0a-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="71f0a-111">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="71f0a-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="71f0a-112">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="71f0a-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="71f0a-113">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="71f0a-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="71f0a-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="71f0a-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="71f0a-115">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="71f0a-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="71f0a-116">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="71f0a-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="71f0a-117">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="71f0a-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="71f0a-118">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="71f0a-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="71f0a-119">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="71f0a-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="71f0a-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="71f0a-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="71f0a-121">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="71f0a-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="71f0a-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="71f0a-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71f0a-123">Uma referência ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="71f0a-123">A reference to the job.</span></span> <span data-ttu-id="71f0a-124">Esse parâmetro poderá ser **nulo** se a tarefa for concluída.</span><span class="sxs-lookup"><span data-stu-id="71f0a-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="71f0a-125">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71f0a-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f0a-126">A quantidade máxima de tempo que o cliente espera que a transição para o novo estado seja executada.</span><span class="sxs-lookup"><span data-stu-id="71f0a-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="71f0a-127">O formato do intervalo deve ser usado para especificar esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="71f0a-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="71f0a-128">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="71f0a-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="71f0a-129">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno de 4098 ("uso de parâmetro de tempo limite não suportado") será retornado.</span><span class="sxs-lookup"><span data-stu-id="71f0a-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f0a-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71f0a-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="71f0a-131">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="71f0a-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-132">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="71f0a-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-133">**Erro desconhecido ou não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="71f0a-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-134">**Não é possível concluir dentro do período de tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="71f0a-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-135">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="71f0a-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-136">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="71f0a-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-137">**Em uso** (6)</span><span class="sxs-lookup"><span data-stu-id="71f0a-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-138">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="71f0a-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-139">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="71f0a-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-140">**Transição de estado inválida** (4097)</span><span class="sxs-lookup"><span data-stu-id="71f0a-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-141">**Não há suporte para o uso do parâmetro timeout** (4098)</span><span class="sxs-lookup"><span data-stu-id="71f0a-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-142">**Ocupado** (4099)</span><span class="sxs-lookup"><span data-stu-id="71f0a-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-143">**Método reservado** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="71f0a-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="71f0a-144">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="71f0a-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="71f0a-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71f0a-145">Requirements</span></span>



| <span data-ttu-id="71f0a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="71f0a-146">Requirement</span></span> | <span data-ttu-id="71f0a-147">Valor</span><span class="sxs-lookup"><span data-stu-id="71f0a-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71f0a-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71f0a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="71f0a-149">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="71f0a-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="71f0a-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71f0a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="71f0a-151">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="71f0a-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="71f0a-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="71f0a-152">Namespace</span></span><br/>                | <span data-ttu-id="71f0a-153">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="71f0a-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="71f0a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="71f0a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71f0a-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71f0a-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71f0a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="71f0a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71f0a-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71f0a-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71f0a-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="71f0a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f0a-159">**\_Teclado Msvm**</span><span class="sxs-lookup"><span data-stu-id="71f0a-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




