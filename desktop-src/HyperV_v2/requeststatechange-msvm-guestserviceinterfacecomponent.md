---
description: Solicita que o estado do componente de interface do serviço de convidado seja alterado para o valor especificado.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Método Msvm_GuestServiceInterfaceComponent:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759399"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="f96b7-103">\_Método Msvm GuestServiceInterfaceComponent:: RequestStateChange</span><span class="sxs-lookup"><span data-stu-id="f96b7-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="f96b7-104">Solicita que o estado do componente de interface do serviço de convidado seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="f96b7-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f96b7-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="f96b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f96b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96b7-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f96b7-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96b7-108">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f96b7-108">Type: **uint16**</span></span>

<span data-ttu-id="f96b7-109">O novo estado.</span><span class="sxs-lookup"><span data-stu-id="f96b7-109">The new state.</span></span> <span data-ttu-id="f96b7-110">As informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno do método **RequestStateChange** for 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="f96b7-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="f96b7-111">Para obter mais informações, consulte a descrição das propriedades **enabledstate** e **requestedstate** para o elemento.</span><span class="sxs-lookup"><span data-stu-id="f96b7-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="f96b7-112">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f96b7-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f96b7-113">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="f96b7-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f96b7-114">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="f96b7-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="f96b7-115">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="f96b7-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="f96b7-116">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="f96b7-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="f96b7-117">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="f96b7-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="f96b7-118">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="f96b7-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="f96b7-119">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="f96b7-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="f96b7-120">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="f96b7-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="f96b7-121">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="f96b7-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f96b7-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f96b7-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="f96b7-123">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f96b7-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f96b7-124">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f96b7-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f96b7-125">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f96b7-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="f96b7-126">Uma referência opcional a um objeto [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que é retornado se a operação é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f96b7-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="f96b7-127">Se estiver presente, a referência retornada poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="f96b7-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="f96b7-128">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f96b7-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96b7-129">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f96b7-129">Type: **datetime**</span></span>

<span data-ttu-id="f96b7-130">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="f96b7-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="f96b7-131">O formato do intervalo deve ser usado para especificar o período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="f96b7-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="f96b7-132">Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="f96b7-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="f96b7-133">Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="f96b7-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96b7-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f96b7-134">Return value</span></span>

<span data-ttu-id="f96b7-135">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f96b7-135">Type: **uint32**</span></span>

<span data-ttu-id="f96b7-136">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f96b7-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="f96b7-137">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f96b7-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f96b7-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="f96b7-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f96b7-139"><dt>**Concluído sem erro**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="f96b7-140">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f96b7-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="f96b7-141"><dt>**Sem suporte**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="f96b7-142"><dt>**Erro desconhecido/não especificado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="f96b7-143"><dt>**Não é possível concluir dentro do período de tempo limite**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="f96b7-144"><dt>**Com falha**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="f96b7-145"><dt>**Parâmetro inválido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="f96b7-146"><dt>**Em uso**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="f96b7-147"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="f96b7-148"><dt>**Parâmetros de método verificados-transição iniciada**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="f96b7-149"><dt>**Transição de estado inválida**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="f96b7-150"><dt>**Uso do parâmetro timeout sem suporte**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="f96b7-151"><dt>**Ocupado**</dt> em <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="f96b7-152"><dt>**Método reservado**</dt> <dt>4100.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="f96b7-153">32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="f96b7-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f96b7-154">Requirements</span></span>



| <span data-ttu-id="f96b7-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96b7-155">Requirement</span></span> | <span data-ttu-id="f96b7-156">Valor</span><span class="sxs-lookup"><span data-stu-id="f96b7-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96b7-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f96b7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f96b7-158">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f96b7-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f96b7-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f96b7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f96b7-160">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f96b7-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f96b7-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="f96b7-161">Namespace</span></span><br/>                | <span data-ttu-id="f96b7-162">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f96b7-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="f96b7-163">MOF</span><span class="sxs-lookup"><span data-stu-id="f96b7-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f96b7-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f96b7-165">DLL</span><span class="sxs-lookup"><span data-stu-id="f96b7-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f96b7-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f96b7-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f96b7-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="f96b7-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96b7-168">**Msvm \_ GuestServiceInterfaceComponent**</span><span class="sxs-lookup"><span data-stu-id="f96b7-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

