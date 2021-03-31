---
description: Destrói um instantâneo de máquina virtual existente.
ms.assetid: 84752bb3-cae1-4a93-89bc-e735c058feda
title: Método DestroySnapshot da classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 91c2e59baa8bb22f5ea9f128130d7dc440e28ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836995"
---
# <a name="destroysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="72514-103">Método DestroySnapshot da \_ classe VirtualSystemSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="72514-103">DestroySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="72514-104">Destrói um instantâneo de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="72514-104">Destroys an existing virtual machine snapshot.</span></span> <span data-ttu-id="72514-105">Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.</span><span class="sxs-lookup"><span data-stu-id="72514-105">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="72514-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72514-106">Syntax</span></span>


```mof
uint32 DestroySnapshot(
  [in]  CIM_VirtualSystemSettingData REF AffectedSnapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="72514-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72514-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72514-108">*AffectedSnapshot* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72514-108">*AffectedSnapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72514-109">Uma referência do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo da máquina virtual a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="72514-109">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="72514-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="72514-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72514-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72514-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72514-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72514-112">Return value</span></span>

<span data-ttu-id="72514-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="72514-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="72514-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="72514-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="72514-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="72514-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="72514-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="72514-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="72514-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="72514-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="72514-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="72514-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="72514-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="72514-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="72514-120">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="72514-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="72514-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="72514-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="72514-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="72514-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="72514-123">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="72514-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="72514-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="72514-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="72514-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72514-125">Requirements</span></span>



| <span data-ttu-id="72514-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="72514-126">Requirement</span></span> | <span data-ttu-id="72514-127">Valor</span><span class="sxs-lookup"><span data-stu-id="72514-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72514-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72514-128">Minimum supported client</span></span><br/> | <span data-ttu-id="72514-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="72514-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="72514-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72514-130">Minimum supported server</span></span><br/> | <span data-ttu-id="72514-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="72514-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="72514-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="72514-132">Namespace</span></span><br/>                | <span data-ttu-id="72514-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="72514-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="72514-134">MOF</span><span class="sxs-lookup"><span data-stu-id="72514-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72514-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72514-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72514-136">DLL</span><span class="sxs-lookup"><span data-stu-id="72514-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72514-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72514-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72514-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="72514-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72514-139">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="72514-139">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="72514-140">**RemoveVirtualSystemSnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="72514-140">**RemoveVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

