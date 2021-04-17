---
description: Inicia o failback para uma máquina virtual de recuperação.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Método Msvm_ReplicationService:: InitiateFailback'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758983"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a><span data-ttu-id="85fa0-103">\_Método Msvm ReplicationService:: InitiateFailback</span><span class="sxs-lookup"><span data-stu-id="85fa0-103">Msvm\_ReplicationService::InitiateFailback method</span></span>

<span data-ttu-id="85fa0-104">Inicia o failback para uma máquina virtual de recuperação.</span><span class="sxs-lookup"><span data-stu-id="85fa0-104">Initiates the failback for a recovery virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="85fa0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85fa0-105">Syntax</span></span>


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="85fa0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85fa0-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85fa0-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fa0-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual iniciar um failback.</span><span class="sxs-lookup"><span data-stu-id="85fa0-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failback.</span></span>

</dd> <dt>

<span data-ttu-id="85fa0-109">*ReplicationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85fa0-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fa0-110">Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as configurações de replicação para o failback.</span><span class="sxs-lookup"><span data-stu-id="85fa0-110">A string representation of an embedded instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings for the failback.</span></span>

</dd> <dt>

<span data-ttu-id="85fa0-111">*RecoveryPointIdentifier* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85fa0-111">*RecoveryPointIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85fa0-112">Entrada opcional que identifica o ponto de recuperação para o qual o failback é solicitado.</span><span class="sxs-lookup"><span data-stu-id="85fa0-112">Optional input that identifies the recovery point to which failback is requested.</span></span>

</dd> <dt>

<span data-ttu-id="85fa0-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="85fa0-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85fa0-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="85fa0-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="85fa0-115">Essa referência pode ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="85fa0-115">This reference can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85fa0-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85fa0-116">Return value</span></span>

<span data-ttu-id="85fa0-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="85fa0-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="85fa0-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="85fa0-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="85fa0-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="85fa0-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="85fa0-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="85fa0-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="85fa0-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="85fa0-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="85fa0-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="85fa0-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="85fa0-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="85fa0-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="85fa0-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="85fa0-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="85fa0-131">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="85fa0-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="85fa0-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="85fa0-132">Remarks</span></span>

<span data-ttu-id="85fa0-133">O **InitiateFailback** funciona em uma máquina virtual de recuperação e leva a máquina virtual para o estado *WaitingForFailback* .</span><span class="sxs-lookup"><span data-stu-id="85fa0-133">**InitiateFailback** works on a recovery virtual machine and takes the virtual machine to *WaitingForFailback* state.</span></span> <span data-ttu-id="85fa0-134">O **InitiateFailback** encaminha a solicitação de failback para o provedor correspondente, que reverte a ressincronização do ponto de recuperação do lado primário novo.</span><span class="sxs-lookup"><span data-stu-id="85fa0-134">**InitiateFailback** forwards the failback request to the corresponding provider, which reverse-resyncs the recovery point from new-primary side.</span></span> <span data-ttu-id="85fa0-135">Após a conclusão do failback do ponto de recuperação solicitado, o estado de replicação passa para o estado *FailbackCompleted* .</span><span class="sxs-lookup"><span data-stu-id="85fa0-135">After failback of the requested recovery point completes, the replication state moves to *FailbackCompleted* state.</span></span>

## <a name="requirements"></a><span data-ttu-id="85fa0-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85fa0-136">Requirements</span></span>



| <span data-ttu-id="85fa0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="85fa0-137">Requirement</span></span> | <span data-ttu-id="85fa0-138">Valor</span><span class="sxs-lookup"><span data-stu-id="85fa0-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85fa0-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85fa0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="85fa0-140">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="85fa0-140">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="85fa0-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85fa0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="85fa0-142">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="85fa0-142">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85fa0-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="85fa0-143">Namespace</span></span><br/>                | <span data-ttu-id="85fa0-144">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="85fa0-144">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="85fa0-145">MOF</span><span class="sxs-lookup"><span data-stu-id="85fa0-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85fa0-146"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85fa0-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85fa0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="85fa0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85fa0-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85fa0-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85fa0-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="85fa0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85fa0-150">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="85fa0-150">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

