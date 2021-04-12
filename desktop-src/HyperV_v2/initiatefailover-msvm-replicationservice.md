---
description: Inicia um failover para uma máquina virtual para um aplicativo ou uma imagem de ponto de replicação padrão.
ms.assetid: cd7e9398-c234-4637-906d-69b46ebf3f51
title: Método InitiateFailover da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f05a9b126028b741782d253ac12b79f9f88e1e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296557"
---
# <a name="initiatefailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b87c1-103">Método InitiateFailover da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="b87c1-103">InitiateFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b87c1-104">Inicia um failover para uma máquina virtual para um aplicativo ou uma imagem de ponto de replicação padrão.</span><span class="sxs-lookup"><span data-stu-id="b87c1-104">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b87c1-105">Syntax</span></span>


```mof
uint32 InitiateFailover(
  [in]  CIM_ComputerSystem           REF ComputerSystem,
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b87c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b87c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b87c1-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b87c1-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b87c1-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual iniciar um failover.</span><span class="sxs-lookup"><span data-stu-id="b87c1-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to initiate a failover.</span></span>

</dd> <dt>

<span data-ttu-id="b87c1-109">*SnapshotSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b87c1-109">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b87c1-110">Uma referência a uma instância de [**\_ VirtualSystemSettingData do CIM**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo usado para o failover.</span><span class="sxs-lookup"><span data-stu-id="b87c1-110">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot used for the failover.</span></span> <span data-ttu-id="b87c1-111">Se esse parâmetro for **nulo**, o failover será executado para o último ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="b87c1-111">If this parameter is **Null**, the failover is to be performed to the latest point in time.</span></span>

</dd> <dt>

<span data-ttu-id="b87c1-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b87c1-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b87c1-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b87c1-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b87c1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b87c1-114">Return value</span></span>

<span data-ttu-id="b87c1-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b87c1-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b87c1-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b87c1-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b87c1-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="b87c1-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b87c1-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="b87c1-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b87c1-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="b87c1-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b87c1-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b87c1-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="b87c1-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b87c1-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="b87c1-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b87c1-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b87c1-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="b87c1-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b87c1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b87c1-130">Requirements</span></span>



| <span data-ttu-id="b87c1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b87c1-131">Requirement</span></span> | <span data-ttu-id="b87c1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b87c1-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b87c1-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b87c1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b87c1-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b87c1-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b87c1-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b87c1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b87c1-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b87c1-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b87c1-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b87c1-137">Namespace</span></span><br/>                | <span data-ttu-id="b87c1-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b87c1-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b87c1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b87c1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b87c1-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b87c1-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b87c1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b87c1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b87c1-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b87c1-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b87c1-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b87c1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87c1-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="b87c1-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b87c1-145">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="b87c1-145">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="b87c1-146">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="b87c1-146">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

