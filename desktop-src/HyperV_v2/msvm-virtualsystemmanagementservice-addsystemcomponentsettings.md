---
description: Adiciona configurações genéricas a uma configuração de sistema virtual.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Método AddSystemComponentSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 56ca8bed752bab52f6a82e18975dd5df72dbe12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757405"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7bfc7-103">Método AddSystemComponentSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="7bfc7-103">AddSystemComponentSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7bfc7-104">Adiciona configurações genéricas a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-104">Adds generic settings to a virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bfc7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bfc7-105">Syntax</span></span>


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7bfc7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bfc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bfc7-107">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7bfc7-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bfc7-108">*ComponentSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7bfc7-108">*ComponentSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bfc7-109">As configurações de componente a serem adicionadas.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-109">The component settings to add.</span></span>

</dd> <dt>

<span data-ttu-id="7bfc7-110">*ResultingComponentSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7bfc7-110">*ResultingComponentSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bfc7-111">Em caso de sucesso, faz referência a um [**\_ SystemComponentSettingData Msvm**](msvm-systemcomponentsettingdata.md) que contém as configurações de componente resultantes.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-111">On success, references a [**Msvm\_SystemComponentSettingData**](msvm-systemcomponentsettingdata.md) that contains the resulting component settings.</span></span>

</dd> <dt>

<span data-ttu-id="7bfc7-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="7bfc7-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bfc7-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7bfc7-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bfc7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7bfc7-114">Return value</span></span>

<span data-ttu-id="7bfc7-115">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-115">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7bfc7-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-123">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7bfc7-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7bfc7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bfc7-125">Requirements</span></span>



| <span data-ttu-id="7bfc7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bfc7-126">Requirement</span></span> | <span data-ttu-id="7bfc7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7bfc7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bfc7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bfc7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7bfc7-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="7bfc7-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7bfc7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bfc7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7bfc7-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7bfc7-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7bfc7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bfc7-132">Namespace</span></span><br/>                | <span data-ttu-id="7bfc7-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7bfc7-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7bfc7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7bfc7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bfc7-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bfc7-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bfc7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7bfc7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bfc7-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7bfc7-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7bfc7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bfc7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bfc7-139">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="7bfc7-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

