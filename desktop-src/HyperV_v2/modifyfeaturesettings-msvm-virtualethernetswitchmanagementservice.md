---
description: Modifica as configurações de recurso de uma porta de comutador Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Método ModifyFeatureSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782359"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="c415b-103">Método ModifyFeatureSettings da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="c415b-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="c415b-104">Modifica as configurações de recurso de uma porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c415b-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c415b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c415b-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c415b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c415b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c415b-107">*FeatureSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c415b-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c415b-108">Uma matriz de cadeias de caracteres que contém uma instância incorporada de uma classe derivada da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) , que descreve as configurações de recurso de porta do comutador a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="c415b-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="c415b-109">*ResultingFeatureSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c415b-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c415b-110">Uma matriz de referências a instâncias da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa as configurações de recurso modificadas.</span><span class="sxs-lookup"><span data-stu-id="c415b-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="c415b-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c415b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c415b-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c415b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c415b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c415b-113">Return value</span></span>

<span data-ttu-id="c415b-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c415b-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c415b-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="c415b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="c415b-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-117">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="c415b-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="c415b-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-119">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="c415b-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-120">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="c415b-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-121">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="c415b-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c415b-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c415b-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c415b-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c415b-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c415b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c415b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c415b-126">Requirements</span></span>



| <span data-ttu-id="c415b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c415b-127">Requirement</span></span> | <span data-ttu-id="c415b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c415b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c415b-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c415b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c415b-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c415b-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c415b-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c415b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c415b-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c415b-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c415b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c415b-133">Namespace</span></span><br/>                | <span data-ttu-id="c415b-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c415b-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c415b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c415b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c415b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c415b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c415b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c415b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c415b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c415b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c415b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c415b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c415b-140">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="c415b-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="c415b-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="c415b-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="c415b-142">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="c415b-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

