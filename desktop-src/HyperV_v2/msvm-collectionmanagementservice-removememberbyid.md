---
description: Remove o elemento gerenciado especificado como um membro do CIM \_ CollectionOfMSEs com o identificador fornecido. Isso terá sucesso mesmo se o objeto com esse identificador não estiver presente.
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Método RemoveMemberById da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172187"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="92e1a-104">Método RemoveMemberById da \_ classe CollectionManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="92e1a-104">RemoveMemberById method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="92e1a-105">Remove o elemento gerenciado especificado como um membro do [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) com o identificador fornecido.</span><span class="sxs-lookup"><span data-stu-id="92e1a-105">Removes the specified managed element as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="92e1a-106">Isso terá sucesso mesmo se o objeto com esse identificador não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="92e1a-106">This will succeed even if the object with that identifier is not present.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e1a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92e1a-107">Syntax</span></span>


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="92e1a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92e1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e1a-109">*Membro* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="92e1a-109">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e1a-110">O membro a ser removido.</span><span class="sxs-lookup"><span data-stu-id="92e1a-110">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="92e1a-111">*CollectionId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92e1a-111">*CollectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e1a-112">A ID da coleção da coleção da qual remover o membro.</span><span class="sxs-lookup"><span data-stu-id="92e1a-112">The collection ID of the collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="92e1a-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="92e1a-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92e1a-114">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="92e1a-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e1a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92e1a-115">Return value</span></span>

<span data-ttu-id="92e1a-116">Retornará 0 se for bem-sucedido ou 4096 se o trabalho for iniciado; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="92e1a-116">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="92e1a-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="92e1a-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="92e1a-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="92e1a-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="92e1a-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="92e1a-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="92e1a-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="92e1a-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="92e1a-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="92e1a-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="92e1a-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="92e1a-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="92e1a-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="92e1a-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="92e1a-130">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="92e1a-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="92e1a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e1a-131">Requirements</span></span>



| <span data-ttu-id="92e1a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e1a-132">Requirement</span></span> | <span data-ttu-id="92e1a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="92e1a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e1a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92e1a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="92e1a-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="92e1a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="92e1a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92e1a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="92e1a-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="92e1a-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="92e1a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="92e1a-138">Namespace</span></span><br/>                | <span data-ttu-id="92e1a-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="92e1a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="92e1a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="92e1a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92e1a-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92e1a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92e1a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="92e1a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92e1a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92e1a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92e1a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="92e1a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e1a-145">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="92e1a-145">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




