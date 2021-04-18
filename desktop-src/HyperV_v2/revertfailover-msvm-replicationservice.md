---
description: Reverte o failover atual de uma máquina virtual descartando o disco de failover atual.
ms.assetid: 99d3a3d3-49e4-4410-b979-47b62ebc6aa6
title: Método RevertFailover da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RevertFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: db20abf34fdad2e0eba499fd1b4cc390bf93b754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753468"
---
# <a name="revertfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="767ee-103">Método RevertFailover da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="767ee-103">RevertFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="767ee-104">Reverte o failover atual de uma máquina virtual descartando o disco de failover atual.</span><span class="sxs-lookup"><span data-stu-id="767ee-104">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span> <span data-ttu-id="767ee-105">Após essa operação, o [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) pode ser chamado novamente.</span><span class="sxs-lookup"><span data-stu-id="767ee-105">After this operation, [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) can be called again.</span></span>

## <a name="syntax"></a><span data-ttu-id="767ee-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="767ee-106">Syntax</span></span>


```mof
uint32 RevertFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="767ee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="767ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="767ee-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="767ee-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="767ee-109">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual reverter o failover.</span><span class="sxs-lookup"><span data-stu-id="767ee-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to revert the failover.</span></span>

</dd> <dt>

<span data-ttu-id="767ee-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="767ee-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="767ee-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="767ee-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="767ee-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="767ee-112">Return value</span></span>

<span data-ttu-id="767ee-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="767ee-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="767ee-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="767ee-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="767ee-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="767ee-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="767ee-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="767ee-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="767ee-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="767ee-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="767ee-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="767ee-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="767ee-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="767ee-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="767ee-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="767ee-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="767ee-127">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="767ee-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="767ee-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="767ee-128">Requirements</span></span>



| <span data-ttu-id="767ee-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="767ee-129">Requirement</span></span> | <span data-ttu-id="767ee-130">Valor</span><span class="sxs-lookup"><span data-stu-id="767ee-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="767ee-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="767ee-131">Minimum supported client</span></span><br/> | <span data-ttu-id="767ee-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="767ee-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="767ee-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="767ee-133">Minimum supported server</span></span><br/> | <span data-ttu-id="767ee-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="767ee-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="767ee-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="767ee-135">Namespace</span></span><br/>                | <span data-ttu-id="767ee-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="767ee-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="767ee-137">MOF</span><span class="sxs-lookup"><span data-stu-id="767ee-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="767ee-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="767ee-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="767ee-139">DLL</span><span class="sxs-lookup"><span data-stu-id="767ee-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="767ee-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="767ee-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="767ee-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="767ee-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767ee-142">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="767ee-142">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="767ee-143">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="767ee-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="767ee-144">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="767ee-144">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md)
</dt> </dl>

 

