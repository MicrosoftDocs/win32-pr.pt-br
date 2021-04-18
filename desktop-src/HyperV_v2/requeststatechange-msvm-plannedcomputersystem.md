---
description: Solicita que o estado do sistema planejado seja alterado para o valor especificado.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Método RequestStateChange da classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757403"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="58c82-103">Método RequestStateChange da classe Msvm \_ PlannedComputerSystem</span><span class="sxs-lookup"><span data-stu-id="58c82-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="58c82-104">Solicita que o estado do sistema planejado seja alterado para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="58c82-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58c82-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="58c82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58c82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c82-107">*Requestedstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58c82-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c82-108">O estado solicitado para o sistema planejado.</span><span class="sxs-lookup"><span data-stu-id="58c82-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="58c82-109">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="58c82-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="58c82-110">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="58c82-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="58c82-111">**Desligar** (4)</span><span class="sxs-lookup"><span data-stu-id="58c82-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="58c82-112">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="58c82-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="58c82-113">**Teste** (7)</span><span class="sxs-lookup"><span data-stu-id="58c82-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="58c82-114">**Defer** (8)</span><span class="sxs-lookup"><span data-stu-id="58c82-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="58c82-115">**Desativar** (9)</span><span class="sxs-lookup"><span data-stu-id="58c82-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="58c82-116">**Reinicializar** (10)</span><span class="sxs-lookup"><span data-stu-id="58c82-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="58c82-117">**Redefinir** (11)</span><span class="sxs-lookup"><span data-stu-id="58c82-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="58c82-118">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="58c82-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="58c82-119">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="58c82-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="58c82-120">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="58c82-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58c82-121">Esse parâmetro não é usado e deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="58c82-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="58c82-122">*TimeoutPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58c82-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c82-123">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="58c82-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c82-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58c82-124">Return value</span></span>

<span data-ttu-id="58c82-125">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="58c82-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="58c82-126">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="58c82-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="58c82-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="58c82-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58c82-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="58c82-129">Êxito</span><span class="sxs-lookup"><span data-stu-id="58c82-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="58c82-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="58c82-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="58c82-133">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="58c82-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="58c82-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="58c82-140">Não há suporte para o valor especificado no parâmetro *requestedstate* .</span><span class="sxs-lookup"><span data-stu-id="58c82-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="58c82-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="58c82-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="58c82-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58c82-144">Requirements</span></span>



| <span data-ttu-id="58c82-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="58c82-145">Requirement</span></span> | <span data-ttu-id="58c82-146">Valor</span><span class="sxs-lookup"><span data-stu-id="58c82-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c82-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58c82-147">Minimum supported client</span></span><br/> | <span data-ttu-id="58c82-148">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="58c82-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="58c82-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58c82-149">Minimum supported server</span></span><br/> | <span data-ttu-id="58c82-150">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="58c82-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58c82-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="58c82-151">Namespace</span></span><br/>                | <span data-ttu-id="58c82-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="58c82-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="58c82-153">MOF</span><span class="sxs-lookup"><span data-stu-id="58c82-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58c82-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58c82-155">DLL</span><span class="sxs-lookup"><span data-stu-id="58c82-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c82-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58c82-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58c82-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="58c82-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58c82-158">**Msvm \_ PlannedComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="58c82-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




