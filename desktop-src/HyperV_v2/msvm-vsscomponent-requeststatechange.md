---
description: Solicita uma alteração de estado.
ms.assetid: 27a8ab6e-afbd-4d87-afd6-8da0cc5e3fba
title: Método RequestStateChange da classe Msvm_VssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7aa40cb65caf41d731085c10aedf21932992e1dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758976"
---
# <a name="requeststatechange-method-of-the-msvm_vsscomponent-class"></a><span data-ttu-id="3ed4e-103">Método RequestStateChange da classe Msvm \_ VssComponent</span><span class="sxs-lookup"><span data-stu-id="3ed4e-103">RequestStateChange method of the Msvm\_VssComponent class</span></span>

<span data-ttu-id="3ed4e-104">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed4e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ed4e-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3ed4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ed4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ed4e-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ed4e-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed4e-108">O novo estado.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-108">The new state.</span></span> <span data-ttu-id="3ed4e-109">As informações serão colocadas na propriedade **requestedstate** da instância se o código de retorno do método **RequestStateChange** for 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="3ed4e-110">Para obter mais informações, consulte a descrição das propriedades **enabledstate** e **requestedstate** para o elemento.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="3ed4e-111">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3ed4e-112">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3ed4e-113">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="3ed4e-114">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="3ed4e-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="3ed4e-116">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="3ed4e-117">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="3ed4e-118">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="3ed4e-119">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="3ed4e-120">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3ed4e-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3ed4e-122">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="3ed4e-123">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3ed4e-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed4e-124">Pode conter uma referência para o [**CIM \_ ConcreteJob**](cim-concretejob.md) criado para acompanhar a transição de estado iniciada pela invocação de método.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="3ed4e-125">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ed4e-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ed4e-126">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="3ed4e-127">O formato do intervalo deve ser usado para especificar o **TimeoutPeriod**.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-127">The interval format must be used to specify the **TimeoutPeriod**.</span></span> <span data-ttu-id="3ed4e-128">Um valor 0 ou um parâmetro nulo indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="3ed4e-129">Se essa propriedade não contiver 0 ou NULL e a implementação não oferecer suporte a esse parâmetro, um código de retorno de ' uso do parâmetro de tempo limite não suportado ' será retornado.</span><span class="sxs-lookup"><span data-stu-id="3ed4e-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ed4e-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ed4e-130">Return value</span></span>

<span data-ttu-id="3ed4e-131">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3ed4e-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3ed4e-132">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ed4e-133">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3ed4e-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3ed4e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed4e-134">Requirements</span></span>



| <span data-ttu-id="3ed4e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed4e-135">Requirement</span></span> | <span data-ttu-id="3ed4e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3ed4e-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed4e-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed4e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed4e-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3ed4e-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3ed4e-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ed4e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed4e-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3ed4e-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3ed4e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ed4e-141">Namespace</span></span><br/>                | <span data-ttu-id="3ed4e-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3ed4e-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3ed4e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="3ed4e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ed4e-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ed4e-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ed4e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed4e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed4e-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ed4e-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ed4e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ed4e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed4e-148">**Msvm \_ VssComponent**</span><span class="sxs-lookup"><span data-stu-id="3ed4e-148">**Msvm\_VssComponent**</span></span>](msvm-vsscomponent.md)
</dt> </dl>

 

 




