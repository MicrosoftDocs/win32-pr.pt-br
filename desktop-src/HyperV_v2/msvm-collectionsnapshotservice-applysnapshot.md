---
description: Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Método ApplySnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782810"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="66bc4-103">Método ApplySnapshot da \_ classe CollectionSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="66bc4-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="66bc4-104">Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="66bc4-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66bc4-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="66bc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66bc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66bc4-107">*Instantâneocollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66bc4-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66bc4-108">Uma referência a uma [**\_ coleção CIM**](cim-collection.md) que representa a coleção de instantâneos a ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="66bc4-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="66bc4-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="66bc4-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66bc4-110">Uma referência opcional que será retornada se a operação for executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="66bc4-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="66bc4-111">Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.</span><span class="sxs-lookup"><span data-stu-id="66bc4-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66bc4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66bc4-112">Return value</span></span>

<span data-ttu-id="66bc4-113">Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="66bc4-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="66bc4-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="66bc4-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="66bc4-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="66bc4-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="66bc4-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="66bc4-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="66bc4-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-120">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="66bc4-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="66bc4-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="66bc4-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-123">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="66bc4-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="66bc4-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="66bc4-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="66bc4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66bc4-125">Requirements</span></span>



| <span data-ttu-id="66bc4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="66bc4-126">Requirement</span></span> | <span data-ttu-id="66bc4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="66bc4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bc4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66bc4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66bc4-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="66bc4-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66bc4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66bc4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66bc4-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="66bc4-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="66bc4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="66bc4-132">Namespace</span></span><br/>                | <span data-ttu-id="66bc4-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="66bc4-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="66bc4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="66bc4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66bc4-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66bc4-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="66bc4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="66bc4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66bc4-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="66bc4-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="66bc4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="66bc4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66bc4-139">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="66bc4-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




