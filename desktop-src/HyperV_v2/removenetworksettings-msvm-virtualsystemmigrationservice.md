---
description: Remove as sub-redes da rede de migração do serviço de migração do sistema virtual.
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Método RemoveNetworkSettings da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789794"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e68e8-103">Método RemoveNetworkSettings da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="e68e8-103">RemoveNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e68e8-104">Remove as sub-redes da rede de migração do serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e68e8-104">Removes migration network subnets from the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e68e8-105">Syntax</span></span>


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e68e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e68e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e68e8-107">*NetworkSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e68e8-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e68e8-108">Uma matriz de instâncias inseridas da classe [**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que representa as sub-redes de rede a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="e68e8-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represent the network subnets to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="e68e8-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e68e8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e68e8-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e68e8-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e68e8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e68e8-111">Return value</span></span>

<span data-ttu-id="e68e8-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e68e8-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e68e8-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e68e8-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e68e8-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e68e8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e68e8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e68e8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e68e8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e68e8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e68e8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e68e8-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e68e8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e68e8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e68e8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e68e8-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e68e8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e68e8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e68e8-126">Requirements</span></span>



| <span data-ttu-id="e68e8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e68e8-127">Requirement</span></span> | <span data-ttu-id="e68e8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e68e8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e68e8-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e68e8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e68e8-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e68e8-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e68e8-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e68e8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e68e8-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e68e8-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e68e8-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e68e8-133">Namespace</span></span><br/>                | <span data-ttu-id="e68e8-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e68e8-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e68e8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e68e8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e68e8-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e68e8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e68e8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e68e8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e68e8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e68e8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e68e8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e68e8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68e8-140">**AddNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="e68e8-140">**AddNetworkSettings**</span></span>](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="e68e8-141">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="e68e8-141">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="e68e8-142">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="e68e8-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

