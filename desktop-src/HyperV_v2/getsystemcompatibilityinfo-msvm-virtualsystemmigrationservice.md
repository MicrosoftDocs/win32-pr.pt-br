---
description: Gera um blob opaco de dados que contém informações de compatibilidade para o sistema especificado.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Método GetSystemCompatibilityInfo da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760860"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="9cbee-103">Método GetSystemCompatibilityInfo da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="9cbee-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="9cbee-104">Gera um blob opaco de dados que contém informações de compatibilidade para o sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="9cbee-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="9cbee-105">Esse método é usado em conjunto com o método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) para determinar se uma migração rápida ou dinâmica de uma máquina virtual para outro sistema de computador host é possível sem realmente tentar a migração.</span><span class="sxs-lookup"><span data-stu-id="9cbee-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cbee-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cbee-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="9cbee-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cbee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cbee-108">*ComputerSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cbee-109">Uma referência a uma classe de [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa a máquina virtual para a qual recuperar informações de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="9cbee-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="9cbee-110">Se esse parâmetro se referir ao sistema de computador de hospedagem, os dados retornados no parâmetro *CompatibilityInfo* poderão ser usados para determinar se alguma das máquinas virtuais no sistema do computador de hospedagem pode ser migrada rapidamente para outro sistema de computador de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="9cbee-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="9cbee-111">*CompatibilityInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cbee-112">Um blob de dados opaco que pode ser passado para o método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) em outro sistema de computador host para confirmar a compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="9cbee-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cbee-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cbee-113">Return value</span></span>

<span data-ttu-id="9cbee-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cbee-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9cbee-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="9cbee-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9cbee-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="9cbee-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9cbee-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="9cbee-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9cbee-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="9cbee-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9cbee-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9cbee-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="9cbee-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9cbee-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="9cbee-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9cbee-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9cbee-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9cbee-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbee-128">Requirements</span></span>



| <span data-ttu-id="9cbee-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbee-129">Requirement</span></span> | <span data-ttu-id="9cbee-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9cbee-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbee-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbee-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9cbee-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9cbee-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cbee-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9cbee-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9cbee-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cbee-135">Namespace</span></span><br/>                | <span data-ttu-id="9cbee-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9cbee-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9cbee-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9cbee-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cbee-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cbee-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cbee-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9cbee-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cbee-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9cbee-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9cbee-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cbee-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbee-142">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="9cbee-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




