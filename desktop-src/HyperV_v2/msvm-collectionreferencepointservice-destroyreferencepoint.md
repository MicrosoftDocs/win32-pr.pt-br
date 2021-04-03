---
description: Destrói uma coleção de pontos de referência existente. Esse método pode, como efeito colateral, destruir outros pontos de referência que dependem da coleção de pontos de referência afetada.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Método DestroyReferencePoint da classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091804"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="8ad15-104">Método DestroyReferencePoint da \_ classe CollectionReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="8ad15-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="8ad15-105">Destrói uma coleção de pontos de referência existente.</span><span class="sxs-lookup"><span data-stu-id="8ad15-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="8ad15-106">Esse método pode, como efeito colateral, destruir outros pontos de referência que dependem da coleção de pontos de referência afetada.</span><span class="sxs-lookup"><span data-stu-id="8ad15-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad15-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ad15-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8ad15-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ad15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ad15-109">*AffectedReferencePointCollection* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8ad15-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad15-110">Referência à coleção de pontos de referência do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="8ad15-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="8ad15-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8ad15-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ad15-112">Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="8ad15-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ad15-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ad15-113">Return value</span></span>

<span data-ttu-id="8ad15-114">Se for bem-sucedido, retornará 0 (sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="8ad15-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="8ad15-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8ad15-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="8ad15-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-117">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="8ad15-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="8ad15-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-119">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="8ad15-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-120">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="8ad15-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-121">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="8ad15-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8ad15-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8ad15-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8ad15-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8ad15-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8ad15-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8ad15-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ad15-126">Requirements</span></span>



| <span data-ttu-id="8ad15-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ad15-127">Requirement</span></span> | <span data-ttu-id="8ad15-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8ad15-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ad15-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ad15-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ad15-130">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8ad15-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8ad15-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ad15-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ad15-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8ad15-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8ad15-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ad15-133">Namespace</span></span><br/>                | <span data-ttu-id="8ad15-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8ad15-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8ad15-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8ad15-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ad15-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ad15-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ad15-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8ad15-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ad15-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ad15-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ad15-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ad15-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad15-140">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="8ad15-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




