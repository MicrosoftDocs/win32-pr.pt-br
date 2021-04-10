---
description: Modifica as configurações de recurso atuais de uma conexão Ethernet de máquina virtual.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Método ModifyFeatureSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296862"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="b33b4-103">Método ModifyFeatureSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="b33b4-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b33b4-104">Modifica as configurações de recurso atuais de uma conexão Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b33b4-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b33b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b33b4-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b33b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b33b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33b4-107">*FeatureSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b33b4-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b33b4-108">Uma matriz de cadeias de caracteres que contém uma instância incorporada de uma classe derivada da classe [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , que descreve as modificações nas configurações de recurso atuais de uma conexão Ethernet existente.</span><span class="sxs-lookup"><span data-stu-id="b33b4-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="b33b4-109">A propriedade **InstanceId** de cada uma dessas instâncias identifica as configurações de recurso a serem modificadas.</span><span class="sxs-lookup"><span data-stu-id="b33b4-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="b33b4-110">*ResultingFeatureSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b33b4-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b33b4-111">Uma matriz de referências a instâncias da classe [**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa as configurações de recurso modificadas.</span><span class="sxs-lookup"><span data-stu-id="b33b4-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="b33b4-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b33b4-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b33b4-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b33b4-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33b4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b33b4-114">Return value</span></span>

<span data-ttu-id="b33b4-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b33b4-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b33b4-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b33b4-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="b33b4-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="b33b4-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="b33b4-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="b33b4-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="b33b4-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-122">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="b33b4-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b33b4-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b33b4-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b33b4-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b33b4-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b33b4-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b33b4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33b4-127">Requirements</span></span>



| <span data-ttu-id="b33b4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33b4-128">Requirement</span></span> | <span data-ttu-id="b33b4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b33b4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33b4-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33b4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b33b4-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b33b4-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b33b4-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b33b4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b33b4-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b33b4-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b33b4-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b33b4-134">Namespace</span></span><br/>                | <span data-ttu-id="b33b4-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b33b4-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b33b4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b33b4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b33b4-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b33b4-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b33b4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b33b4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b33b4-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b33b4-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b33b4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b33b4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33b4-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="b33b4-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

