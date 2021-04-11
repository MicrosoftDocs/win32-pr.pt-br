---
description: Adiciona configurações de recurso Ethernet à configuração de uma conexão Ethernet de máquina virtual.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Método AddFeatureSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296761"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d5afe-103">Método AddFeatureSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="d5afe-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d5afe-104">Adiciona configurações de recurso Ethernet à configuração de uma conexão Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d5afe-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5afe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5afe-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d5afe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5afe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5afe-107">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5afe-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5afe-108">Referência a uma instância da classe [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que representa a conexão Ethernet afetada.</span><span class="sxs-lookup"><span data-stu-id="d5afe-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="d5afe-109">*FeatureSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5afe-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5afe-110">Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) que descreve as configurações de recurso a serem adicionadas à configuração de conexão.</span><span class="sxs-lookup"><span data-stu-id="d5afe-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d5afe-111">*ResultingFeatureSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5afe-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5afe-112">Uma matriz de referências a instâncias da classe [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa as configurações de recurso adicionadas.</span><span class="sxs-lookup"><span data-stu-id="d5afe-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="d5afe-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d5afe-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5afe-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d5afe-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5afe-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5afe-115">Return value</span></span>

<span data-ttu-id="d5afe-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d5afe-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d5afe-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d5afe-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="d5afe-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="d5afe-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="d5afe-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="d5afe-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d5afe-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d5afe-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d5afe-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d5afe-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d5afe-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d5afe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5afe-126">Requirements</span></span>



| <span data-ttu-id="d5afe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5afe-127">Requirement</span></span> | <span data-ttu-id="d5afe-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d5afe-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5afe-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5afe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d5afe-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d5afe-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d5afe-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5afe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d5afe-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d5afe-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5afe-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5afe-133">Namespace</span></span><br/>                | <span data-ttu-id="d5afe-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d5afe-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d5afe-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d5afe-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5afe-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5afe-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5afe-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d5afe-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5afe-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5afe-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d5afe-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5afe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5afe-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d5afe-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

