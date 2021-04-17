---
description: Remove o log de dados associado ao ponto de referência.
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Método RemoveAssociatedData da classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aec1ac249616c08c6abf1f156ad5a3416c8afaff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811873"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="83237-103">Método RemoveAssociatedData da \_ classe CollectionReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="83237-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="83237-104">Remove o log de dados associado ao ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="83237-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="83237-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83237-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="83237-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83237-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83237-107">*AffectedReferencePointCollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83237-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83237-108">Referência à coleção de pontos de referência do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="83237-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="83237-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="83237-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83237-110">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="83237-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83237-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83237-111">Return value</span></span>

<span data-ttu-id="83237-112">Se for bem-sucedido, retornará 0 (sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="83237-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="83237-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="83237-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="83237-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="83237-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="83237-115">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="83237-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="83237-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="83237-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="83237-117">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="83237-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="83237-118">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="83237-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="83237-119">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="83237-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="83237-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="83237-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="83237-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="83237-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="83237-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="83237-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="83237-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="83237-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="83237-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83237-124">Requirements</span></span>



| <span data-ttu-id="83237-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="83237-125">Requirement</span></span> | <span data-ttu-id="83237-126">Valor</span><span class="sxs-lookup"><span data-stu-id="83237-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83237-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83237-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83237-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="83237-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="83237-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83237-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83237-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="83237-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="83237-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="83237-131">Namespace</span></span><br/>                | <span data-ttu-id="83237-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="83237-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="83237-133">MOF</span><span class="sxs-lookup"><span data-stu-id="83237-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83237-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83237-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83237-135">DLL</span><span class="sxs-lookup"><span data-stu-id="83237-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83237-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83237-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83237-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="83237-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83237-138">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="83237-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




