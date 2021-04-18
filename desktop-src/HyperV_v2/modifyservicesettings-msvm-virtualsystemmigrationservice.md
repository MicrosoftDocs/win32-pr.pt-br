---
description: Modifica os dados de configuração para o serviço de migração.
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Método ModifyServiceSettings da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766900"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e91dd-103">Método ModifyServiceSettings da \_ classe VirtualSystemMigrationService Msvm</span><span class="sxs-lookup"><span data-stu-id="e91dd-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e91dd-104">Modifica os dados de configuração para o serviço de migração.</span><span class="sxs-lookup"><span data-stu-id="e91dd-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91dd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e91dd-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e91dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e91dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e91dd-107">*ServiceSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e91dd-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e91dd-108">Uma instância inserida da classe [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) que contém as novas configurações de serviço.</span><span class="sxs-lookup"><span data-stu-id="e91dd-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="e91dd-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e91dd-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e91dd-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e91dd-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e91dd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e91dd-111">Return value</span></span>

<span data-ttu-id="e91dd-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e91dd-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e91dd-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e91dd-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e91dd-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e91dd-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e91dd-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e91dd-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e91dd-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e91dd-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e91dd-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e91dd-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e91dd-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e91dd-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e91dd-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e91dd-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e91dd-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e91dd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e91dd-126">Requirements</span></span>



| <span data-ttu-id="e91dd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e91dd-127">Requirement</span></span> | <span data-ttu-id="e91dd-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e91dd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e91dd-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e91dd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e91dd-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e91dd-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e91dd-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e91dd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e91dd-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e91dd-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e91dd-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e91dd-133">Namespace</span></span><br/>                | <span data-ttu-id="e91dd-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e91dd-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e91dd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e91dd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e91dd-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e91dd-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e91dd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e91dd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e91dd-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e91dd-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e91dd-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e91dd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91dd-140">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="e91dd-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

