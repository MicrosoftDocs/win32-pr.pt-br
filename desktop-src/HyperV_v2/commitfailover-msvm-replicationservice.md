---
description: Confirma o instantâneo de recuperação que o método InitiateFailover usou para um failover.
ms.assetid: 05c27211-adc7-400a-83e2-81792ae7577f
title: Método CommitFailover da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.CommitFailover
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 04687ea29f39645c2407de44faf6bba6ecc75832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810359"
---
# <a name="commitfailover-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="382e4-103">Método CommitFailover da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="382e4-103">CommitFailover method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="382e4-104">Confirma o instantâneo de recuperação que o método [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) usou para um failover.</span><span class="sxs-lookup"><span data-stu-id="382e4-104">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span>

<span data-ttu-id="382e4-105">Esse método mescla os pontos de recuperação na máquina virtual de recuperação aplicando o instantâneo de recuperação.</span><span class="sxs-lookup"><span data-stu-id="382e4-105">This method flattens the recovery points on the recovery virtual machine by applying the recovery snapshot.</span></span> <span data-ttu-id="382e4-106">Depois que isso for feito, a operação de failover não poderá ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="382e4-106">After this is done, the failover operation cannot be canceled.</span></span> <span data-ttu-id="382e4-107">Normalmente, os usuários executarão isso quando o ponto de replicação usado para failover for satisfatório e a máquina virtual de recuperação puder alterar a função para primária.</span><span class="sxs-lookup"><span data-stu-id="382e4-107">Users will typically perform this when the replication point used for failover is satisfactory and the recovery virtual machine can change role to be primary.</span></span>

## <a name="syntax"></a><span data-ttu-id="382e4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="382e4-108">Syntax</span></span>


```mof
uint32 CommitFailover(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="382e4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="382e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="382e4-110">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="382e4-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="382e4-111">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual confirmar o failover.</span><span class="sxs-lookup"><span data-stu-id="382e4-111">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which to commit the failover.</span></span>

</dd> <dt>

<span data-ttu-id="382e4-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="382e4-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="382e4-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="382e4-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="382e4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="382e4-114">Return value</span></span>

<span data-ttu-id="382e4-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="382e4-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="382e4-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="382e4-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="382e4-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="382e4-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="382e4-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="382e4-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="382e4-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="382e4-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="382e4-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="382e4-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="382e4-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="382e4-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="382e4-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="382e4-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="382e4-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="382e4-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="382e4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="382e4-130">Requirements</span></span>



| <span data-ttu-id="382e4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="382e4-131">Requirement</span></span> | <span data-ttu-id="382e4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="382e4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382e4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="382e4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="382e4-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="382e4-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="382e4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="382e4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="382e4-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="382e4-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="382e4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="382e4-137">Namespace</span></span><br/>                | <span data-ttu-id="382e4-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="382e4-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="382e4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="382e4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="382e4-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="382e4-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="382e4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="382e4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="382e4-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="382e4-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="382e4-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="382e4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382e4-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="382e4-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

