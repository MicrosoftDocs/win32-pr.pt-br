---
description: Remove um instantâneo existente e todos os seus filhos de uma máquina virtual.
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Método DestroySnapshotTree da classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5658e954766531765c47f8bef80d5509f2ad27c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756767"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="a2b91-103">Método DestroySnapshotTree da \_ classe VirtualSystemSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="a2b91-103">DestroySnapshotTree method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="a2b91-104">Remove um instantâneo existente e todos os seus filhos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a2b91-104">Removes an existing snapshot, and all its children, of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b91-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2b91-105">Syntax</span></span>


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a2b91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2b91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b91-107">*SnapshotSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a2b91-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2b91-108">Uma referência do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa a árvore de instantâneo da máquina virtual a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="a2b91-108">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot tree to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="a2b91-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a2b91-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2b91-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2b91-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b91-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2b91-111">Return value</span></span>

<span data-ttu-id="a2b91-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a2b91-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a2b91-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a2b91-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a2b91-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a2b91-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a2b91-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a2b91-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a2b91-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a2b91-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a2b91-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a2b91-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a2b91-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a2b91-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a2b91-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a2b91-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a2b91-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a2b91-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2b91-126">Requirements</span></span>



| <span data-ttu-id="a2b91-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2b91-127">Requirement</span></span> | <span data-ttu-id="a2b91-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a2b91-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b91-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2b91-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b91-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a2b91-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a2b91-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2b91-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b91-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a2b91-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2b91-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2b91-133">Namespace</span></span><br/>                | <span data-ttu-id="a2b91-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a2b91-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a2b91-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a2b91-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2b91-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2b91-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2b91-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a2b91-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2b91-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a2b91-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a2b91-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2b91-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b91-140">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="a2b91-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="a2b91-141">**RemoveVirtualSystemSnapshotTree (v1)**</span><span class="sxs-lookup"><span data-stu-id="a2b91-141">**RemoveVirtualSystemSnapshotTree (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

