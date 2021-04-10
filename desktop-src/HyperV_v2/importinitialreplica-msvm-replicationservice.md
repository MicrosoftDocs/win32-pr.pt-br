---
description: Importa a replicação inicial para uma máquina virtual.
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Método ImportInitialReplica da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091147"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="f1656-103">Método ImportInitialReplica da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="f1656-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="f1656-104">Importa a replicação inicial para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f1656-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1656-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1656-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f1656-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1656-107">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1656-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1656-108">Uma referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual para a qual a replicação inicial deve ser importada.</span><span class="sxs-lookup"><span data-stu-id="f1656-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="f1656-109">*InitialReplicationImportLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f1656-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1656-110">O caminho totalmente qualificado do diretório do qual a replicação inicial deve ser importada.</span><span class="sxs-lookup"><span data-stu-id="f1656-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="f1656-111">Isso não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f1656-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="f1656-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f1656-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1656-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1656-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1656-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1656-114">Return value</span></span>

<span data-ttu-id="f1656-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1656-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f1656-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f1656-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f1656-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f1656-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f1656-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f1656-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f1656-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f1656-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f1656-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f1656-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f1656-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f1656-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f1656-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f1656-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f1656-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="f1656-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f1656-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1656-130">Requirements</span></span>



| <span data-ttu-id="f1656-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1656-131">Requirement</span></span> | <span data-ttu-id="f1656-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f1656-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1656-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1656-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f1656-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f1656-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f1656-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1656-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f1656-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f1656-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1656-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1656-137">Namespace</span></span><br/>                | <span data-ttu-id="f1656-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f1656-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f1656-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f1656-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1656-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1656-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1656-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f1656-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1656-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1656-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1656-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1656-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1656-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="f1656-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

