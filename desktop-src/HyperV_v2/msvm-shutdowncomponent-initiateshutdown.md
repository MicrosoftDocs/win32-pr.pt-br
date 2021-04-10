---
description: Inicia uma operação de desligamento do sistema operacional na máquina virtual filho associada. Se zero (0) for retornado, o desligamento foi iniciado com êxito. Qualquer outro código de retorno indica uma condição de erro.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Método InitiateShutdown da classe Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170251"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="efaf0-105">Método InitiateShutdown da \_ classe ShutdownComponent Msvm</span><span class="sxs-lookup"><span data-stu-id="efaf0-105">InitiateShutdown method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="efaf0-106">Inicia uma operação de desligamento do sistema operacional na máquina virtual filho associada.</span><span class="sxs-lookup"><span data-stu-id="efaf0-106">Initiates an operating system shutdown operation on the associated child virtual machine.</span></span> <span data-ttu-id="efaf0-107">Se zero (0) for retornado, o desligamento foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="efaf0-107">If zero (0) is returned, then the shutdown was initiated successfully.</span></span> <span data-ttu-id="efaf0-108">Qualquer outro código de retorno indica uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="efaf0-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="efaf0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efaf0-109">Syntax</span></span>


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a><span data-ttu-id="efaf0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efaf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efaf0-111">*Forçar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efaf0-111">*Force* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efaf0-112">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="efaf0-112">Type: **boolean**</span></span>

<span data-ttu-id="efaf0-113">Um sinalizador que, se **verdadeiro**, força os aplicativos a serem fechados, apesar de terem dados não salvos.</span><span class="sxs-lookup"><span data-stu-id="efaf0-113">A flag which, if **True**, forces applications to be closed despite having unsaved data.</span></span>

</dd> <dt>

<span data-ttu-id="efaf0-114">*Motivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efaf0-114">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efaf0-115">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="efaf0-115">Type: **string**</span></span>

<span data-ttu-id="efaf0-116">O motivo para a operação de desligamento.</span><span class="sxs-lookup"><span data-stu-id="efaf0-116">The reason for the shutdown operation.</span></span> <span data-ttu-id="efaf0-117">Esta é uma cadeia de caracteres definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="efaf0-117">This is a user-defined string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efaf0-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efaf0-118">Return value</span></span>

<span data-ttu-id="efaf0-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efaf0-119">Type: **uint32**</span></span>

<dl> <dt>

<span data-ttu-id="efaf0-120">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="efaf0-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="efaf0-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-122">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="efaf0-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-123">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="efaf0-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-124">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="efaf0-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-125">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="efaf0-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-126">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="efaf0-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-127">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="efaf0-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-128">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="efaf0-128">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-129">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="efaf0-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-130">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="efaf0-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-131">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="efaf0-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-132">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="efaf0-132">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-133">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="efaf0-133">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-134">**O sistema não está pronto** (32780)</span><span class="sxs-lookup"><span data-stu-id="efaf0-134">**The system is not ready** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-135">**A máquina está bloqueada e não pode ser desligada sem a opção Force** (32781)</span><span class="sxs-lookup"><span data-stu-id="efaf0-135">**The machine is locked and cannot be shut down without the force option** (32781)</span></span>
</dt> <dt>

<span data-ttu-id="efaf0-136">**Um desligamento do sistema está em andamento** (32782)</span><span class="sxs-lookup"><span data-stu-id="efaf0-136">**A system shutdown is in progress** (32782)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="efaf0-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="efaf0-137">Remarks</span></span>

<span data-ttu-id="efaf0-138">O acesso à classe [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="efaf0-138">Access to the [**Msvm\_ShutdownComponent**](msvm-shutdowncomponent.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="efaf0-139">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="efaf0-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="efaf0-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efaf0-140">Requirements</span></span>



| <span data-ttu-id="efaf0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="efaf0-141">Requirement</span></span> | <span data-ttu-id="efaf0-142">Valor</span><span class="sxs-lookup"><span data-stu-id="efaf0-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efaf0-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efaf0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="efaf0-144">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="efaf0-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="efaf0-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efaf0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="efaf0-146">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="efaf0-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="efaf0-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="efaf0-147">Namespace</span></span><br/>                | <span data-ttu-id="efaf0-148">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="efaf0-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="efaf0-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="efaf0-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="efaf0-150"><dt>Winreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="efaf0-150"><dt>Winreg.h</dt></span></span> </dl>                     |
| <span data-ttu-id="efaf0-151">MOF</span><span class="sxs-lookup"><span data-stu-id="efaf0-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efaf0-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efaf0-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efaf0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="efaf0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efaf0-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efaf0-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="efaf0-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="efaf0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efaf0-156">**Msvm \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="efaf0-156">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

