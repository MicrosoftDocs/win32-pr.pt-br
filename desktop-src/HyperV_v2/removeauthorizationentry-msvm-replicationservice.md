---
description: Remove uma entrada de autorização de um servidor de recuperação.
ms.assetid: 1647b35d-1c2f-4fb5-84c0-10b357326abf
title: Método RemoveAuthorizationEntry da classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.RemoveAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0bb0d24c9cf4936c6e0187e5091b9fac14ee28c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812930"
---
# <a name="removeauthorizationentry-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="d51b0-103">Método RemoveAuthorizationEntry da \_ classe ReplicationService Msvm</span><span class="sxs-lookup"><span data-stu-id="d51b0-103">RemoveAuthorizationEntry method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="d51b0-104">Remove uma entrada de autorização de um servidor de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d51b0-104">Removes an authorization entry from a recovery server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d51b0-105">Syntax</span></span>


```mof
uint32 RemoveAuthorizationEntry(
  [in]  string              AllowedPrimaryHostSystem,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d51b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d51b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d51b0-107">*AllowedPrimaryHostSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d51b0-107">*AllowedPrimaryHostSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d51b0-108">O servidor primário para o qual a entrada de autorização será removida do servidor.</span><span class="sxs-lookup"><span data-stu-id="d51b0-108">The primary server for which the authorization entry will be removed from the server.</span></span> <span data-ttu-id="d51b0-109">Isso é o mesmo que a propriedade **AllowedPrimaryHostSystem** da classe [**Msvm \_ ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d51b0-109">This is the same as the **AllowedPrimaryHostSystem** property of the [**Msvm\_ReplicationAuthorizationSettingData**](msvm-replicationauthorizationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="d51b0-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d51b0-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d51b0-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d51b0-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d51b0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d51b0-112">Return value</span></span>

<span data-ttu-id="d51b0-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d51b0-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d51b0-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d51b0-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d51b0-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="d51b0-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d51b0-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="d51b0-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d51b0-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="d51b0-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d51b0-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d51b0-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="d51b0-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d51b0-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="d51b0-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d51b0-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d51b0-127">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="d51b0-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d51b0-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d51b0-128">Remarks</span></span>

<span data-ttu-id="d51b0-129">A remoção de uma entrada de autorização interromperá a replicação de qualquer máquina virtual que esteja autorizada com a entrada.</span><span class="sxs-lookup"><span data-stu-id="d51b0-129">Removing an authorization entry will stop replication for any virtual machines that are authorized with the entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="d51b0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d51b0-130">Requirements</span></span>



| <span data-ttu-id="d51b0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d51b0-131">Requirement</span></span> | <span data-ttu-id="d51b0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d51b0-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51b0-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d51b0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d51b0-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d51b0-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d51b0-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d51b0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d51b0-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d51b0-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d51b0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d51b0-137">Namespace</span></span><br/>                | <span data-ttu-id="d51b0-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d51b0-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d51b0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d51b0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d51b0-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d51b0-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d51b0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d51b0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d51b0-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d51b0-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d51b0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d51b0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51b0-144">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="d51b0-144">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d51b0-145">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="d51b0-145">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d51b0-146">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="d51b0-146">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="d51b0-147">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="d51b0-147">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

