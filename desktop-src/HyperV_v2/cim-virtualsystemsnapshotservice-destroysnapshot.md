---
description: Destrua um instantâneo do sistema virtual existente. Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.
ms.assetid: 69f60d0e-50ef-4a38-ad4b-88534b7fb3f8
title: Método DestroySnapshot da classe CIM_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80d618374d2da4a12f2ce31284d7b3fa36ba65ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501896"
---
# <a name="destroysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="9366f-104">Método DestroySnapshot da \_ classe VIRTUALSYSTEMSNAPSHOTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="9366f-104">DestroySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="9366f-105">Destrua um instantâneo do sistema virtual existente.</span><span class="sxs-lookup"><span data-stu-id="9366f-105">Destroy an existing virtual system snapshot.</span></span> <span data-ttu-id="9366f-106">Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.</span><span class="sxs-lookup"><span data-stu-id="9366f-106">This method may as a side effect destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="9366f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9366f-107">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9366f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9366f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9366f-109">*AffectedSnapshot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9366f-109">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9366f-110">Uma referência do [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) ao instantâneo do sistema virtual afetado.</span><span class="sxs-lookup"><span data-stu-id="9366f-110">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="9366f-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="9366f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9366f-112">Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.</span><span class="sxs-lookup"><span data-stu-id="9366f-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="9366f-113">Este parâmetro foi leitura/gravação em Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="9366f-113">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9366f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9366f-114">Return value</span></span>

<span data-ttu-id="9366f-115">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="9366f-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9366f-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="9366f-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="9366f-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="9366f-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="9366f-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="9366f-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="9366f-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-122">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="9366f-122">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9366f-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9366f-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9366f-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9366f-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="9366f-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9366f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9366f-127">Requirements</span></span>



| <span data-ttu-id="9366f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9366f-128">Requirement</span></span> | <span data-ttu-id="9366f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9366f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9366f-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9366f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9366f-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9366f-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9366f-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9366f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9366f-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9366f-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9366f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="9366f-134">Namespace</span></span><br/>                | <span data-ttu-id="9366f-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9366f-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9366f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9366f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9366f-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9366f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9366f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9366f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9366f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9366f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9366f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9366f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9366f-141">**\_VIRTUALSYSTEMSNAPSHOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="9366f-141">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




