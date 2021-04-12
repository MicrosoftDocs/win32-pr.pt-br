---
description: Executa uma operação de ressincronização na máquina virtual especificada.
ms.assetid: a3d06780-f43b-45c4-a186-a3544f9c7963
title: Resincronizar o método da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.Resynchronize
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dcd4865d110843de27f0a242b31253310439e1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296920"
---
# <a name="resynchronize-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="42bab-103">Resincronizar o método da \_ classe Msvm ReplicationService</span><span class="sxs-lookup"><span data-stu-id="42bab-103">Resynchronize method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="42bab-104">Executa uma operação de ressincronização na máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="42bab-104">Performs a resynchronization operation on the specified virtual machine.</span></span> <span data-ttu-id="42bab-105">Quando um cliente chama esse método para uma máquina virtual de réplica, ele é ressincronizado com a réplica estendida.</span><span class="sxs-lookup"><span data-stu-id="42bab-105">When a client calls this method for a replica virtual machine, it resynchronizes with extended replica.</span></span>

<span data-ttu-id="42bab-106">Esse método compara os discos habilitados para replicação nas máquinas virtuais primárias e de recuperação e corrige quaisquer problemas de integridade de dados de replicação, replicando os diferentes blocos do primário para a recuperação.</span><span class="sxs-lookup"><span data-stu-id="42bab-106">This methods compares the replication enabled disks on the primary and recovery virtual machines, and fixes any replication data integrity issues by replicating the different blocks from the primary to the recovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="42bab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42bab-107">Syntax</span></span>


```mof
uint32 Resynchronize(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  datetime               StartTime,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="42bab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42bab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42bab-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42bab-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42bab-110">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual a ser ressincronizada.</span><span class="sxs-lookup"><span data-stu-id="42bab-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine to be resynchronized.</span></span>

</dd> <dt>

<span data-ttu-id="42bab-111">*StartTime* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42bab-111">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42bab-112">A hora de início agendada para iniciar a operação de ressincronização.</span><span class="sxs-lookup"><span data-stu-id="42bab-112">The scheduled start time for the resynchronization operation to begin.</span></span> <span data-ttu-id="42bab-113">Se esse parâmetro for **nulo**, a operação de ressincronização será iniciada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="42bab-113">If this parameter is **Null**, the resynchronization operation starts immediately.</span></span>

</dd> <dt>

<span data-ttu-id="42bab-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="42bab-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42bab-115">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42bab-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42bab-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42bab-116">Return value</span></span>

<span data-ttu-id="42bab-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="42bab-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="42bab-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="42bab-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="42bab-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="42bab-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="42bab-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="42bab-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="42bab-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="42bab-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="42bab-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="42bab-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="42bab-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="42bab-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="42bab-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="42bab-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="42bab-131">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="42bab-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="42bab-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42bab-132">Requirements</span></span>



| <span data-ttu-id="42bab-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="42bab-133">Requirement</span></span> | <span data-ttu-id="42bab-134">Valor</span><span class="sxs-lookup"><span data-stu-id="42bab-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42bab-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42bab-135">Minimum supported client</span></span><br/> | <span data-ttu-id="42bab-136">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="42bab-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42bab-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42bab-137">Minimum supported server</span></span><br/> | <span data-ttu-id="42bab-138">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="42bab-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42bab-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="42bab-139">Namespace</span></span><br/>                | <span data-ttu-id="42bab-140">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="42bab-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42bab-141">MOF</span><span class="sxs-lookup"><span data-stu-id="42bab-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42bab-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42bab-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42bab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="42bab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42bab-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42bab-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="42bab-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="42bab-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42bab-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="42bab-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

