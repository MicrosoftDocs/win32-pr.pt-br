---
description: Remove as configurações de componente genérico de uma configuração de sistema virtual.
ms.assetid: 54ddb960-65b7-409d-ad80-f3685562a1a1
title: Método RemoveSystemComponentSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93ef7b794b901212fad72a1fcdf6223d8344b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782348"
---
# <a name="removesystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7365d-103">Método RemoveSystemComponentSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="7365d-103">RemoveSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7365d-104">Remove as configurações de componente genérico de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7365d-104">Removes generic component settings from a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7365d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7365d-105">Syntax</span></span>


```mof
uint32 RemoveSystemComponentSettings(
  [in]  Msvm_SystemComponentSettingData REF ComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7365d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7365d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7365d-107">*ComponentSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7365d-107">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7365d-108">Matriz de [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) que fazem referência às configurações de componente a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="7365d-108">Array of [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that reference the component settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="7365d-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7365d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7365d-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7365d-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7365d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7365d-111">Return value</span></span>

<span data-ttu-id="7365d-112">Retorna 0 ou 4096 em um êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7365d-112">Returns 0 or 4096 on a success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7365d-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7365d-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="7365d-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-115">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="7365d-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="7365d-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-117">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="7365d-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-118">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="7365d-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7365d-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7365d-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-121">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7365d-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7365d-122">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7365d-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7365d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7365d-123">Requirements</span></span>



| <span data-ttu-id="7365d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7365d-124">Requirement</span></span> | <span data-ttu-id="7365d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7365d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7365d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7365d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7365d-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="7365d-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7365d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7365d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7365d-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7365d-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7365d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="7365d-130">Namespace</span></span><br/>                | <span data-ttu-id="7365d-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7365d-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7365d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7365d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7365d-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7365d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7365d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7365d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7365d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7365d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7365d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7365d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7365d-137">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="7365d-137">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

