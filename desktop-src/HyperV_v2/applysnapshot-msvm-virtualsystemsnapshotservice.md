---
description: Aplica um instantâneo de máquina virtual à máquina virtual da qual ele foi criado.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Método ApplySnapshot da classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828441"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="d2e6f-103">Método ApplySnapshot da \_ classe VirtualSystemSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="d2e6f-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="d2e6f-104">Aplica um instantâneo de máquina virtual à máquina virtual da qual ele foi criado.</span><span class="sxs-lookup"><span data-stu-id="d2e6f-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e6f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2e6f-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d2e6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2e6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e6f-107">*Instantâneo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2e6f-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e6f-108">Uma referência a uma classe derivada do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo da máquina virtual a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="d2e6f-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="d2e6f-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d2e6f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e6f-110">Essa operação é sempre executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d2e6f-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="d2e6f-111">Esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2e6f-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e6f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2e6f-112">Return value</span></span>

<span data-ttu-id="d2e6f-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2e6f-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d2e6f-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-120">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-123">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-125">**Estado inválido** (32775)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-126">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d2e6f-127">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d2e6f-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d2e6f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e6f-128">Requirements</span></span>



| <span data-ttu-id="d2e6f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e6f-129">Requirement</span></span> | <span data-ttu-id="d2e6f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d2e6f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e6f-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e6f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e6f-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d2e6f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2e6f-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2e6f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e6f-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d2e6f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2e6f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2e6f-135">Namespace</span></span><br/>                | <span data-ttu-id="d2e6f-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d2e6f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2e6f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d2e6f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2e6f-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2e6f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2e6f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d2e6f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2e6f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2e6f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2e6f-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2e6f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e6f-142">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="d2e6f-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="d2e6f-143">**ApplyVirtualSystemSnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="d2e6f-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="d2e6f-144">**ApplyVirtualSystemSnapshotEx (v1)**</span><span class="sxs-lookup"><span data-stu-id="d2e6f-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

