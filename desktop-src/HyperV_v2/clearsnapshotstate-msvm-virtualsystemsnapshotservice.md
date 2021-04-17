---
description: Limpa o estado de salvamento de um instantâneo existente.
ms.assetid: abb0ed4a-7f89-4d32-93d2-7491d2f2aa83
title: Método ClearSnapshotState da classe Msvm_VirtualSystemSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ClearSnapshotState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a218b600e45d91d8c744d6b49afe97666ddb51ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757150"
---
# <a name="clearsnapshotstate-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="39586-103">Método ClearSnapshotState da \_ classe VirtualSystemSnapshotService Msvm</span><span class="sxs-lookup"><span data-stu-id="39586-103">ClearSnapshotState method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="39586-104">Limpa o estado de salvamento de um instantâneo existente.</span><span class="sxs-lookup"><span data-stu-id="39586-104">Clears save state from an existing snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="39586-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39586-105">Syntax</span></span>


```mof
uint32 ClearSnapshotState(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="39586-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39586-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39586-107">*SnapshotSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39586-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39586-108">Uma referência à instância [**\_ VirtualSystemSettingData do CIM**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo cujo estado deve ser apagado.</span><span class="sxs-lookup"><span data-stu-id="39586-108">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot whose state is to be cleared.</span></span>

</dd> <dt>

<span data-ttu-id="39586-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="39586-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39586-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="39586-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39586-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39586-111">Return value</span></span>

<span data-ttu-id="39586-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="39586-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="39586-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="39586-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39586-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="39586-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="39586-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="39586-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="39586-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="39586-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="39586-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="39586-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="39586-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="39586-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="39586-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="39586-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="39586-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="39586-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="39586-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="39586-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="39586-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="39586-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="39586-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="39586-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="39586-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="39586-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="39586-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="39586-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="39586-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39586-126">Requirements</span></span>



| <span data-ttu-id="39586-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="39586-127">Requirement</span></span> | <span data-ttu-id="39586-128">Valor</span><span class="sxs-lookup"><span data-stu-id="39586-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39586-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39586-129">Minimum supported client</span></span><br/> | <span data-ttu-id="39586-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="39586-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39586-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39586-131">Minimum supported server</span></span><br/> | <span data-ttu-id="39586-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="39586-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39586-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="39586-133">Namespace</span></span><br/>                | <span data-ttu-id="39586-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="39586-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39586-135">MOF</span><span class="sxs-lookup"><span data-stu-id="39586-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39586-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39586-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39586-137">DLL</span><span class="sxs-lookup"><span data-stu-id="39586-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39586-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39586-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39586-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="39586-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39586-140">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="39586-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

