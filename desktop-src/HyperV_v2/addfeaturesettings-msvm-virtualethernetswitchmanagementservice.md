---
description: Adiciona configurações de recurso à configuração de uma porta de comutador Ethernet.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Método AddFeatureSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921788"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="dcc3a-103">Método AddFeatureSettings da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="dcc3a-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="dcc3a-104">Adiciona configurações de recurso à configuração de uma porta de comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="dcc3a-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcc3a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dcc3a-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="dcc3a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dcc3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcc3a-107">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcc3a-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc3a-108">Uma referência a uma classe derivada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que representa a porta do comutador Ethernet afetada ou a configuração do comutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="dcc3a-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dcc3a-109">*FeatureSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dcc3a-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc3a-110">Uma matriz de cadeias de caracteres que contém uma instância incorporada de uma classe derivada da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) , que descreve as configurações de recurso a serem adicionadas à configuração da porta do comutador.</span><span class="sxs-lookup"><span data-stu-id="dcc3a-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dcc3a-111">*ResultingFeatureSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dcc3a-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc3a-112">Uma matriz de referências a instâncias da classe [**Msvm \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa as configurações de recurso adicionadas.</span><span class="sxs-lookup"><span data-stu-id="dcc3a-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="dcc3a-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="dcc3a-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcc3a-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dcc3a-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcc3a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dcc3a-115">Return value</span></span>

<span data-ttu-id="dcc3a-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dcc3a-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dcc3a-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="dcc3a-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="dcc3a-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dcc3a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcc3a-126">Requirements</span></span>



| <span data-ttu-id="dcc3a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcc3a-127">Requirement</span></span> | <span data-ttu-id="dcc3a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dcc3a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcc3a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcc3a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dcc3a-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dcc3a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dcc3a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dcc3a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dcc3a-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dcc3a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcc3a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcc3a-133">Namespace</span></span><br/>                | <span data-ttu-id="dcc3a-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="dcc3a-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dcc3a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="dcc3a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcc3a-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcc3a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcc3a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="dcc3a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcc3a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dcc3a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dcc3a-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcc3a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcc3a-140">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dcc3a-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="dcc3a-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dcc3a-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="dcc3a-142">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="dcc3a-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

