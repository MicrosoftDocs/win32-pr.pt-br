---
description: Cria um novo \_ objeto CIM CollectionOfMSEs.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Método definocollection da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767640"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="5a7ad-103">Método definocollection da classe Msvm \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="5a7ad-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="5a7ad-104">Cria um novo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="5a7ad-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a7ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a7ad-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5a7ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a7ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a7ad-107">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5a7ad-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7ad-108">O nome da nova coleção.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="5a7ad-109">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5a7ad-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7ad-110">A ID da nova coleção.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="5a7ad-111">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5a7ad-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7ad-112">O tipo da nova coleção.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="5a7ad-113">**Coleção de sistemas virtuais** (0)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="5a7ad-114">**Coleção de coleções** (1)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="5a7ad-115">*Definedcollection* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5a7ad-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7ad-116">Referência aos objetos que definem a coleção.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5a7ad-117">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5a7ad-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a7ad-118">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="5a7ad-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a7ad-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a7ad-119">Return value</span></span>

<span data-ttu-id="5a7ad-120">Se for bem-sucedido, retornará 0 ou 4096 (trabalho iniciado); caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5a7ad-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5a7ad-121">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-123">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-124">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-125">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-126">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-127">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-128">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-129">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-130">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-131">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-132">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-133">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="5a7ad-134">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="5a7ad-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5a7ad-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a7ad-135">Requirements</span></span>



| <span data-ttu-id="5a7ad-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a7ad-136">Requirement</span></span> | <span data-ttu-id="5a7ad-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5a7ad-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a7ad-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a7ad-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5a7ad-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5a7ad-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5a7ad-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a7ad-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5a7ad-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5a7ad-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5a7ad-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a7ad-142">Namespace</span></span><br/>                | <span data-ttu-id="5a7ad-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5a7ad-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5a7ad-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5a7ad-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a7ad-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a7ad-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a7ad-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5a7ad-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a7ad-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a7ad-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a7ad-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a7ad-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7ad-149">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="5a7ad-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




