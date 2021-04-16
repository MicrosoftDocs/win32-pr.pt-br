---
description: Remove as configurações de recurso de uma porta de comutador Ethernet.
ms.assetid: 3d45259e-34e4-417b-a895-4926b0eaaf59
title: Método RemoveFeatureSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 919e2b69e2a0ef215a522c601088cb7aa2976a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757806"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="31b07-103">Método RemoveFeatureSettings da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="31b07-103">RemoveFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="31b07-104">Remove as configurações de recurso de uma porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="31b07-104">Removes feature settings from an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31b07-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_FeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="31b07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31b07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b07-107">*FeatureSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31b07-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31b07-108">Uma matriz de referências a instâncias da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa as configurações de recurso a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="31b07-108">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="31b07-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="31b07-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31b07-110">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="31b07-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b07-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31b07-111">Return value</span></span>

<span data-ttu-id="31b07-112">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="31b07-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="31b07-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="31b07-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="31b07-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-115">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="31b07-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="31b07-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-117">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="31b07-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-118">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="31b07-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="31b07-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-120">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="31b07-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-121">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="31b07-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="31b07-122">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="31b07-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="31b07-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31b07-123">Requirements</span></span>



| <span data-ttu-id="31b07-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b07-124">Requirement</span></span> | <span data-ttu-id="31b07-125">Valor</span><span class="sxs-lookup"><span data-stu-id="31b07-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31b07-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31b07-126">Minimum supported client</span></span><br/> | <span data-ttu-id="31b07-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="31b07-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31b07-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31b07-128">Minimum supported server</span></span><br/> | <span data-ttu-id="31b07-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="31b07-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31b07-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="31b07-130">Namespace</span></span><br/>                | <span data-ttu-id="31b07-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="31b07-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="31b07-132">MOF</span><span class="sxs-lookup"><span data-stu-id="31b07-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31b07-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31b07-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31b07-134">DLL</span><span class="sxs-lookup"><span data-stu-id="31b07-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31b07-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31b07-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="31b07-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="31b07-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b07-137">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="31b07-137">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="31b07-138">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="31b07-138">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="31b07-139">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="31b07-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

