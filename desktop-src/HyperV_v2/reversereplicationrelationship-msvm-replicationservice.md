---
description: Replica uma máquina virtual com failover de volta para o servidor primário.
ms.assetid: 21806a66-85b4-4d9e-8a50-52d2b1933b67
title: Método ReverseReplicationRelationship da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ReverseReplicationRelationship
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 25ab0c754c5139b0b3419db74162a8ac0495cf1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782345"
---
# <a name="reversereplicationrelationship-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="3267b-103">Método ReverseReplicationRelationship da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="3267b-103">ReverseReplicationRelationship method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="3267b-104">Replica uma máquina virtual com failover de volta para o servidor primário.</span><span class="sxs-lookup"><span data-stu-id="3267b-104">Replicates a failed-over virtual machine back to the primary server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3267b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3267b-105">Syntax</span></span>


```mof
uint32 ReverseReplicationRelationship(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3267b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3267b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3267b-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3267b-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3267b-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a replicação deve ser revertida.</span><span class="sxs-lookup"><span data-stu-id="3267b-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the replication should be reversed.</span></span>

</dd> <dt>

<span data-ttu-id="3267b-109">*ReplicationSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3267b-109">*ReplicationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3267b-110">Uma representação de cadeia de caracteres de uma instância da classe [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) que define as configurações de replicação.</span><span class="sxs-lookup"><span data-stu-id="3267b-110">A string representation of an instance of the [**Msvm\_ReplicationSettingData**](msvm-replicationsettingdata.md) class that defines the replication settings.</span></span>

</dd> <dt>

<span data-ttu-id="3267b-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3267b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3267b-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3267b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3267b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3267b-113">Return value</span></span>

<span data-ttu-id="3267b-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3267b-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3267b-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3267b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3267b-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="3267b-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="3267b-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="3267b-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="3267b-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="3267b-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="3267b-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="3267b-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="3267b-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="3267b-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="3267b-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="3267b-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="3267b-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="3267b-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3267b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3267b-129">Requirements</span></span>



| <span data-ttu-id="3267b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3267b-130">Requirement</span></span> | <span data-ttu-id="3267b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3267b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3267b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3267b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3267b-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3267b-133">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3267b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3267b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3267b-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3267b-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3267b-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3267b-136">Namespace</span></span><br/>                | <span data-ttu-id="3267b-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3267b-137">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3267b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3267b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3267b-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3267b-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3267b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3267b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3267b-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3267b-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3267b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3267b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3267b-143">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="3267b-143">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

