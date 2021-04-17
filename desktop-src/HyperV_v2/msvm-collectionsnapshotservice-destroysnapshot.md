---
description: Destrói um instantâneo existente da coleção do sistema virtual. Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Método DestroySnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 399737a95db7725718b2e0ec620d2b6b7a7ae93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770407"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="447c8-104">Método DestroySnapshot da \_ classe CollectionSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="447c8-104">DestroySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="447c8-105">Destrói um instantâneo existente da coleção do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="447c8-105">Destroys an existing snapshot of virtual system collection.</span></span> <span data-ttu-id="447c8-106">Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.</span><span class="sxs-lookup"><span data-stu-id="447c8-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="447c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="447c8-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="447c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="447c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="447c8-109">*AffectedSnapshotCollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="447c8-109">*AffectedSnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="447c8-110">Referência a uma [**\_ coleção CIM**](cim-collection.md) que descreve a coleção de instantâneos do sistema virtual afetada.</span><span class="sxs-lookup"><span data-stu-id="447c8-110">Reference to a [**CIM\_Collection**](cim-collection.md) that describes the affected virtual system snapshot collection.</span></span>

</dd> <dt>

<span data-ttu-id="447c8-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="447c8-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="447c8-112">Uma referência opcional que será retornada se a operação for executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="447c8-112">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="447c8-113">Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="447c8-113">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="447c8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="447c8-114">Return value</span></span>

<span data-ttu-id="447c8-115">Em caso de sucesso, retorna 0 (completo) ou 4096 (trabalho iniciado); caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="447c8-115">On success, returns either 0 (Complete) or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="447c8-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="447c8-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="447c8-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="447c8-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="447c8-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="447c8-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="447c8-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-122">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="447c8-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="447c8-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="447c8-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="447c8-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="447c8-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="447c8-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="447c8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="447c8-127">Requirements</span></span>



| <span data-ttu-id="447c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="447c8-128">Requirement</span></span> | <span data-ttu-id="447c8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="447c8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="447c8-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="447c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="447c8-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="447c8-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="447c8-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="447c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="447c8-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="447c8-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="447c8-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="447c8-134">Namespace</span></span><br/>                | <span data-ttu-id="447c8-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="447c8-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="447c8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="447c8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="447c8-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="447c8-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="447c8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="447c8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="447c8-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="447c8-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="447c8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="447c8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="447c8-141">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="447c8-141">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




