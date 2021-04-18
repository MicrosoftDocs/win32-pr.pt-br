---
description: Altera a relação de replicação estendida para a relação primária de uma máquina virtual de réplica. A máquina virtual de réplica deve estar em um estado de failover confirmado.
ms.assetid: B593A155-B5E6-44E5-8835-09DEB1FF868E
title: 'Método Msvm_ReplicationService:: ChangeReplicationModeToPrimary'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ChangeReplicationModeToPrimary
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0a18b3c9f1003ff7b263f5c6b7cc89abedccfd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769350"
---
# <a name="msvm_replicationservicechangereplicationmodetoprimary-method"></a><span data-ttu-id="bba79-104">\_Método Msvm ReplicationService:: ChangeReplicationModeToPrimary</span><span class="sxs-lookup"><span data-stu-id="bba79-104">Msvm\_ReplicationService::ChangeReplicationModeToPrimary method</span></span>

<span data-ttu-id="bba79-105">Altera a relação de replicação estendida para a relação primária de uma máquina virtual de réplica.</span><span class="sxs-lookup"><span data-stu-id="bba79-105">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="bba79-106">A máquina virtual de réplica deve estar em um estado de failover confirmado.</span><span class="sxs-lookup"><span data-stu-id="bba79-106">The replica virtual machine must be in a failover committed state.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba79-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba79-107">Syntax</span></span>


```C++
uint32 ChangeReplicationModeToPrimary(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationRelationship,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a><span data-ttu-id="bba79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba79-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba79-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba79-110">Uma referência a uma instância de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual esse método altera a relação de replicação estendida para a relação primária.</span><span class="sxs-lookup"><span data-stu-id="bba79-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which this method changes the extended replication relationship to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="bba79-111">*ReplicationRelationship* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bba79-111">*ReplicationRelationship* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bba79-112">Uma representação de cadeia de caracteres de uma instância inserida da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que define a relação de replicação estendida que esse método altera para a relação primária.</span><span class="sxs-lookup"><span data-stu-id="bba79-112">A string representation of an embedded instance of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class that defines the extended replication relationship that this method changes to the primary relationship.</span></span>

</dd> <dt>

<span data-ttu-id="bba79-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="bba79-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bba79-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bba79-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span> <span data-ttu-id="bba79-115">Essa referência poderá ser **nula** se a tarefa for concluída.</span><span class="sxs-lookup"><span data-stu-id="bba79-115">This reference can be **NULL** if the task is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba79-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bba79-116">Return value</span></span>

<span data-ttu-id="bba79-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bba79-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bba79-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="bba79-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-119">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="bba79-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-120">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="bba79-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-121">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="bba79-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-122">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="bba79-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-123">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="bba79-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-124">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="bba79-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-125">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bba79-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-126">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bba79-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-127">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="bba79-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-128">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bba79-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-129">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="bba79-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-130">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bba79-130">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bba79-131">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="bba79-131">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bba79-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba79-132">Requirements</span></span>



| <span data-ttu-id="bba79-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba79-133">Requirement</span></span> | <span data-ttu-id="bba79-134">Valor</span><span class="sxs-lookup"><span data-stu-id="bba79-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bba79-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bba79-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bba79-136">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bba79-136">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bba79-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bba79-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bba79-138">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="bba79-138">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bba79-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="bba79-139">Namespace</span></span><br/>                | <span data-ttu-id="bba79-140">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="bba79-140">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="bba79-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bba79-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba79-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bba79-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bba79-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bba79-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba79-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bba79-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bba79-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="bba79-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba79-146">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="bba79-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

