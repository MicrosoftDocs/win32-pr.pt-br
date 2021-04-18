---
description: Adiciona sub-redes de rede de migração para o serviço de migração de sistema virtual.
ms.assetid: b0e0f187-beeb-4fdf-a91c-f6c5500f0f6d
title: Método AddNetworkSettings da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.AddNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 75d168b1a49d8ac44ab66ba9da13d1e598c647b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757155"
---
# <a name="addnetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="a8dee-103">Método AddNetworkSettings da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="a8dee-103">AddNetworkSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="a8dee-104">Adiciona sub-redes de rede de migração para o serviço de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="a8dee-104">Adds migration network subnets for the virtual system migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8dee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8dee-105">Syntax</span></span>


```mof
uint32 AddNetworkSettings(
  [in]  string              NetworkSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a8dee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8dee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8dee-107">*NetworkSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8dee-107">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8dee-108">Uma matriz de instâncias inseridas da classe [**Msvm \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que contém as configurações de rede de migração.</span><span class="sxs-lookup"><span data-stu-id="a8dee-108">An array of embedded instances of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that contain the migration network settings.</span></span>

</dd> <dt>

<span data-ttu-id="a8dee-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="a8dee-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8dee-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a8dee-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8dee-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8dee-111">Return value</span></span>

<span data-ttu-id="a8dee-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8dee-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a8dee-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="a8dee-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a8dee-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="a8dee-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a8dee-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="a8dee-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a8dee-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="a8dee-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a8dee-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a8dee-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="a8dee-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a8dee-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="a8dee-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a8dee-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a8dee-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a8dee-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8dee-126">Requirements</span></span>



| <span data-ttu-id="a8dee-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8dee-127">Requirement</span></span> | <span data-ttu-id="a8dee-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a8dee-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dee-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8dee-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a8dee-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a8dee-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8dee-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8dee-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a8dee-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a8dee-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8dee-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8dee-133">Namespace</span></span><br/>                | <span data-ttu-id="a8dee-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a8dee-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a8dee-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a8dee-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8dee-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8dee-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8dee-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a8dee-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8dee-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a8dee-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a8dee-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8dee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8dee-140">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="a8dee-140">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="a8dee-141">**RemoveNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="a8dee-141">**RemoveNetworkSettings**</span></span>](removenetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="a8dee-142">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="a8dee-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

