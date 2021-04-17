---
description: Redefine as estatísticas de replicação para uma máquina virtual e atua na relação de replicação primária da máquina virtual.
ms.assetid: da4b60f8-6964-45af-8412-935234c7c0ff
title: Método ResetReplicationStatistics da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ResetReplicationStatistics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8407e20cb38c9aecac26ab0bcee99ce0c8a6be2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782346"
---
# <a name="resetreplicationstatistics-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="773ca-103">Método ResetReplicationStatistics da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="773ca-103">ResetReplicationStatistics method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="773ca-104">Redefine as estatísticas de replicação para uma máquina virtual e atua na relação de replicação primária da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="773ca-104">Resets the replication statistics for a virtual machine and acts on the primary replication relationship of the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="773ca-105">A partir do Windows 8.1, recomendamos não usar o **ResetReplicationStatistics** para redefinir as estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="773ca-105">Starting with Windows 8.1, we recommend not to use **ResetReplicationStatistics** anymore to reset replication statistics.</span></span> <span data-ttu-id="773ca-106">Em vez disso, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span><span class="sxs-lookup"><span data-stu-id="773ca-106">Instead, use [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="773ca-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="773ca-107">Syntax</span></span>


```mof
uint32 ResetReplicationStatistics(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="773ca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="773ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773ca-109">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="773ca-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773ca-110">Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual para a qual redefinir as estatísticas de replicação.</span><span class="sxs-lookup"><span data-stu-id="773ca-110">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to reset the replication statistics for.</span></span>

</dd> <dt>

<span data-ttu-id="773ca-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="773ca-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="773ca-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="773ca-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="773ca-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="773ca-113">Return value</span></span>

<span data-ttu-id="773ca-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="773ca-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="773ca-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="773ca-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="773ca-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="773ca-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="773ca-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="773ca-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="773ca-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="773ca-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="773ca-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="773ca-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="773ca-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="773ca-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="773ca-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="773ca-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="773ca-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="773ca-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="773ca-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="773ca-129">Requirements</span></span>



| <span data-ttu-id="773ca-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="773ca-130">Requirement</span></span> | <span data-ttu-id="773ca-131">Valor</span><span class="sxs-lookup"><span data-stu-id="773ca-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="773ca-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="773ca-132">Minimum supported client</span></span><br/> | <span data-ttu-id="773ca-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="773ca-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="773ca-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="773ca-134">Minimum supported server</span></span><br/> | <span data-ttu-id="773ca-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="773ca-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="773ca-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="773ca-136">Namespace</span></span><br/>                | <span data-ttu-id="773ca-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="773ca-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="773ca-138">MOF</span><span class="sxs-lookup"><span data-stu-id="773ca-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="773ca-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="773ca-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="773ca-140">DLL</span><span class="sxs-lookup"><span data-stu-id="773ca-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="773ca-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="773ca-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="773ca-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="773ca-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773ca-143">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="773ca-143">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="773ca-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="773ca-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

