---
description: Cria uma nova réplica de uma máquina virtual com o instantâneo especificado para fins de teste.
ms.assetid: 447f3c8f-8c57-4874-9466-91c6aea533bc
title: Método TestReplicaSystem da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicaSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 029130e619aa36d0aa9b9c1c85a877fb26e1b22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836856"
---
# <a name="testreplicasystem-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f0a1b-103">Método TestReplicaSystem da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="f0a1b-103">TestReplicaSystem method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f0a1b-104">Cria uma nova réplica de uma máquina virtual com o instantâneo especificado para fins de teste.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-104">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0a1b-105">Syntax</span></span>


```mof
uint32 TestReplicaSystem(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f0a1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0a1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0a1b-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0a1b-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a1b-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a replicação deve ser testada.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be tested.</span></span>

</dd> <dt>

<span data-ttu-id="f0a1b-109">*SnapshotSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0a1b-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a1b-110">Uma referência a uma instância de [**\_ VirtualSystemSettingData do CIM**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo usado para criar o sistema de failover de teste.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used to create the test failover system.</span></span> <span data-ttu-id="f0a1b-111">Se esse parâmetro for **nulo**, o failover será executado fora do último ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-111">If this parameter is **Null**, the failover is to be performed off the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="f0a1b-112">*ResultingSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f0a1b-112">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a1b-113">Se uma máquina virtual for definida com êxito, o receberá uma referência a uma instância da classe de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual de teste recentemente definida.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-113">If a virtual machine is successfully defined, receives a reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly defined test virtual machine.</span></span> <span data-ttu-id="f0a1b-114">Quando esse sistema não for mais necessário, destrua-o chamando o método [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1b-114">When this system is no longer needed, destroy it by calling the [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="f0a1b-115">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f0a1b-115">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0a1b-116">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0a1b-116">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0a1b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0a1b-117">Return value</span></span>

<span data-ttu-id="f0a1b-118">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0a1b-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f0a1b-119">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-121">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-122">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-123">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-124">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-125">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-126">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-127">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-127">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-128">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-129">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-130">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-131">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-131">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f0a1b-132">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="f0a1b-132">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f0a1b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a1b-133">Requirements</span></span>



| <span data-ttu-id="f0a1b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a1b-134">Requirement</span></span> | <span data-ttu-id="f0a1b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f0a1b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a1b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a1b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a1b-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f0a1b-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0a1b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0a1b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a1b-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f0a1b-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0a1b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0a1b-140">Namespace</span></span><br/>                | <span data-ttu-id="f0a1b-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f0a1b-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0a1b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f0a1b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0a1b-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0a1b-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0a1b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f0a1b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a1b-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0a1b-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0a1b-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0a1b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a1b-147">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="f0a1b-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

