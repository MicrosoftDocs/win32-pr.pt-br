---
description: Remove as configurações de recurso de uma conexão Ethernet de máquina virtual.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Método RemoveFeatureSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757541"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="8c830-103">Método RemoveFeatureSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="8c830-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8c830-104">Remove as configurações de recurso de uma conexão Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c830-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c830-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c830-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8c830-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c830-107">*FeatureSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c830-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c830-108">Uma matriz de cadeias de caracteres que contém uma instância inserida de uma classe derivada da classe [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , que define as configurações de recurso a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="8c830-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="8c830-109">A propriedade **InstanceId** de cada uma dessas instâncias identifica as configurações de recurso a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="8c830-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="8c830-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8c830-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c830-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8c830-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c830-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c830-112">Return value</span></span>

<span data-ttu-id="8c830-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c830-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8c830-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8c830-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="8c830-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="8c830-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="8c830-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="8c830-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="8c830-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8c830-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="8c830-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="8c830-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8c830-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="8c830-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8c830-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c830-124">Requirements</span></span>



| <span data-ttu-id="8c830-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c830-125">Requirement</span></span> | <span data-ttu-id="8c830-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8c830-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c830-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c830-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c830-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8c830-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8c830-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c830-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c830-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8c830-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c830-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c830-131">Namespace</span></span><br/>                | <span data-ttu-id="8c830-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8c830-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8c830-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8c830-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c830-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c830-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c830-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8c830-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c830-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8c830-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8c830-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c830-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c830-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="8c830-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

