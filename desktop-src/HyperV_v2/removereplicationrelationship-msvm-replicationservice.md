---
description: Remove uma relação de replicação de máquina virtual e age na relação de replicação primária da máquina virtual.
ms.assetid: a9a20aa1-378d-4a2a-9ebc-9786ab2dfda7
title: Método RemoveReplicationRelationship da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb897ff72cd927390362f076114fc8757baa6c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827295"
---
# <a name="removereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="2d1f8-103">Método RemoveReplicationRelationship da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="2d1f8-103">RemoveReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="2d1f8-104">Remove uma relação de replicação de máquina virtual e age na relação de replicação primária da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2d1f8-104">Removes a virtual machine replication relationship and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="2d1f8-105">A partir do Windows 8.1, recomendamos não usar **RemoveReplicationRelationship** para remover um relacionamento de replicação de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2d1f8-105">Starting with Windows 8.1, we recommend not to use **RemoveReplicationRelationship** anymore to remove a virtual machine replication relationship.</span></span> <span data-ttu-id="2d1f8-106">Em vez disso, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="2d1f8-106">Instead, use [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2d1f8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d1f8-107">Syntax</span></span>


```mof
uint32 RemoveReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2d1f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d1f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d1f8-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d1f8-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d1f8-110">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a relação de replicação deve ser removida.</span><span class="sxs-lookup"><span data-stu-id="2d1f8-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication relationship should be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2d1f8-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="2d1f8-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d1f8-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2d1f8-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d1f8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d1f8-113">Return value</span></span>

<span data-ttu-id="2d1f8-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d1f8-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2d1f8-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2d1f8-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="2d1f8-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2d1f8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d1f8-129">Requirements</span></span>



| <span data-ttu-id="2d1f8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d1f8-130">Requirement</span></span> | <span data-ttu-id="2d1f8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2d1f8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d1f8-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d1f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2d1f8-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2d1f8-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2d1f8-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d1f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2d1f8-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2d1f8-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d1f8-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d1f8-136">Namespace</span></span><br/>                | <span data-ttu-id="2d1f8-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2d1f8-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2d1f8-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2d1f8-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d1f8-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d1f8-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d1f8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2d1f8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d1f8-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2d1f8-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2d1f8-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d1f8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d1f8-143">**CreateReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="2d1f8-143">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="2d1f8-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="2d1f8-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

