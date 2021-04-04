---
description: Solicita que o estado do serviço convidado seja alterado para o valor especificado.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Método Msvm_GuestService:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662538"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="11b7b-103">\_Método Msvm GuestService:: RequestStateChange</span><span class="sxs-lookup"><span data-stu-id="11b7b-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="11b7b-104">Solicita que o estado do serviço convidado seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="11b7b-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11b7b-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="11b7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11b7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11b7b-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11b7b-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b7b-108">O novo estado.</span><span class="sxs-lookup"><span data-stu-id="11b7b-108">The new state.</span></span> <span data-ttu-id="11b7b-109">As informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno do método **RequestStateChange** for 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="11b7b-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="11b7b-110">Para obter mais informações, consulte a descrição das propriedades **enabledstate** e **requestedstate** para o elemento.</span><span class="sxs-lookup"><span data-stu-id="11b7b-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="11b7b-111">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="11b7b-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11b7b-112">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="11b7b-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11b7b-113">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="11b7b-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="11b7b-114">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="11b7b-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="11b7b-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="11b7b-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="11b7b-116">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="11b7b-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="11b7b-117">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="11b7b-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="11b7b-118">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="11b7b-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="11b7b-119">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="11b7b-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="11b7b-120">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="11b7b-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="11b7b-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="11b7b-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="11b7b-122">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="11b7b-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="11b7b-123">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="11b7b-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11b7b-124">Uma referência opcional a um objeto [**CIM \_ ConcreteJob**](cim-concretejob.md) que é retornado se a operação é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="11b7b-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="11b7b-125">Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="11b7b-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="11b7b-126">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11b7b-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b7b-127">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="11b7b-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="11b7b-128">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="11b7b-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="11b7b-129">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="11b7b-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="11b7b-130">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="11b7b-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11b7b-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11b7b-131">Return value</span></span>

<span data-ttu-id="11b7b-132">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="11b7b-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="11b7b-133">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="11b7b-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="11b7b-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="11b7b-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11b7b-135"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="11b7b-136">Êxito.</span><span class="sxs-lookup"><span data-stu-id="11b7b-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="11b7b-137"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="11b7b-138"><dt>**Parâmetros de método verificados-transição iniciada**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="11b7b-139">A transição é assíncrona.</span><span class="sxs-lookup"><span data-stu-id="11b7b-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="11b7b-140"><dt>**Uso do parâmetro timeout sem suporte**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="11b7b-141"><dt>**Acesso negado**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="11b7b-142">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="11b7b-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="11b7b-143"><dt>**Estado inválido para esta operação**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="11b7b-144">Não há suporte para o valor especificado no parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="11b7b-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="11b7b-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11b7b-145">Requirements</span></span>



| <span data-ttu-id="11b7b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="11b7b-146">Requirement</span></span> | <span data-ttu-id="11b7b-147">Valor</span><span class="sxs-lookup"><span data-stu-id="11b7b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11b7b-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11b7b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="11b7b-149">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11b7b-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="11b7b-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11b7b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="11b7b-151">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="11b7b-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="11b7b-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="11b7b-152">Namespace</span></span><br/>                | <span data-ttu-id="11b7b-153">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="11b7b-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="11b7b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="11b7b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11b7b-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11b7b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="11b7b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b7b-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11b7b-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11b7b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="11b7b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b7b-159">**Msvm \_ GuestService**</span><span class="sxs-lookup"><span data-stu-id="11b7b-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




