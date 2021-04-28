---
description: O método RequestStateChange da classe Msvm_DisketteDrive-solicita uma alteração de estado.
ms.assetid: 349081c0-65d8-470d-8d84-7c616c0f81b6
title: Método RequestStateChange da classe Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06d61557ca765721660937592f59667f5e6b3fc9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119164"
---
# <a name="requeststatechange-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="aa436-103">Método RequestStateChange da classe Msvm \_ DisketteDrive</span><span class="sxs-lookup"><span data-stu-id="aa436-103">RequestStateChange method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="aa436-104">Solicita uma alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="aa436-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa436-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa436-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="aa436-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa436-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa436-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa436-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa436-108">O estado solicitado para o elemento.</span><span class="sxs-lookup"><span data-stu-id="aa436-108">The state requested for the element.</span></span> <span data-ttu-id="aa436-109">Essas informações serão colocadas na propriedade Requestedstate da instância se o código de retorno do método RequestStateChange for 0 (' concluído sem erro ') ou 4096 (0x1000) (' trabalho iniciado ').</span><span class="sxs-lookup"><span data-stu-id="aa436-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="aa436-110">Consulte a descrição das propriedades Enabledstate e Requestedstate para obter as explicações detalhadas dos valores Requestedstate.</span><span class="sxs-lookup"><span data-stu-id="aa436-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa436-111">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="aa436-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa436-112">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aa436-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="aa436-113">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="aa436-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="aa436-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="aa436-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="aa436-115">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="aa436-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="aa436-116">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="aa436-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="aa436-117">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="aa436-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="aa436-118">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="aa436-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="aa436-119">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="aa436-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="aa436-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="aa436-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="aa436-121">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="aa436-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="aa436-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="aa436-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa436-123">Pode conter uma referência para o ConcreteJob criado para acompanhar a transição de estado iniciada pela invocação de método.</span><span class="sxs-lookup"><span data-stu-id="aa436-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="aa436-124">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa436-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa436-125">Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha.</span><span class="sxs-lookup"><span data-stu-id="aa436-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="aa436-126">O formato do intervalo deve ser usado para especificar o TimeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="aa436-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="aa436-127">Um valor 0 ou um parâmetro nulo indica que o cliente não tem requisitos de tempo para a transição.</span><span class="sxs-lookup"><span data-stu-id="aa436-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="aa436-128">Se essa propriedade não contiver 0 ou NULL e a implementação não oferecer suporte a esse parâmetro, um código de retorno de ' uso do parâmetro de tempo limite não suportado ' será retornado.</span><span class="sxs-lookup"><span data-stu-id="aa436-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa436-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aa436-129">Return value</span></span>

<span data-ttu-id="aa436-130">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="aa436-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="aa436-131">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="aa436-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa436-132">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="aa436-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aa436-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa436-133">Requirements</span></span>



| <span data-ttu-id="aa436-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa436-134">Requirement</span></span> | <span data-ttu-id="aa436-135">Valor</span><span class="sxs-lookup"><span data-stu-id="aa436-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa436-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa436-136">Minimum supported client</span></span><br/> | <span data-ttu-id="aa436-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="aa436-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="aa436-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa436-138">Minimum supported server</span></span><br/> | <span data-ttu-id="aa436-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="aa436-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="aa436-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa436-140">Namespace</span></span><br/>                | <span data-ttu-id="aa436-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="aa436-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa436-142">MOF</span><span class="sxs-lookup"><span data-stu-id="aa436-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa436-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa436-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa436-144">DLL</span><span class="sxs-lookup"><span data-stu-id="aa436-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa436-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa436-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa436-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="aa436-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa436-147">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="aa436-147">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




