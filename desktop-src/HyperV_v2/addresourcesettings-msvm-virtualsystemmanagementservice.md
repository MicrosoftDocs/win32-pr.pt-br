---
description: Adiciona recursos a uma configuração de máquina virtual.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Método AddResourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828442"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="05da2-103">Método AddResourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="05da2-103">AddResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="05da2-104">Adiciona recursos a uma configuração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="05da2-104">Adds resources to a virtual machine configuration.</span></span> <span data-ttu-id="05da2-105">Quando aplicado a uma configuração de máquina virtual de "estado", como um efeito colateral, os recursos são adicionados à máquina virtual ativa.</span><span class="sxs-lookup"><span data-stu-id="05da2-105">When applied to a "state" virtual machine configuration, as a side effect, resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="05da2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05da2-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="05da2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05da2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05da2-108">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05da2-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05da2-109">Uma referência a um objeto [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa a configuração de máquina virtual afetada.</span><span class="sxs-lookup"><span data-stu-id="05da2-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual machine configuration.</span></span>

</dd> <dt>

<span data-ttu-id="05da2-110">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="05da2-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05da2-111">Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que descreve os aspectos virtuais de um recurso virtual a ser adicionado à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="05da2-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="05da2-112">*ResultingResourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="05da2-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05da2-113">Uma matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa aspectos virtuais dos recursos virtuais adicionados.</span><span class="sxs-lookup"><span data-stu-id="05da2-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="05da2-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="05da2-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05da2-115">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="05da2-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05da2-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05da2-116">Return value</span></span>

<span data-ttu-id="05da2-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="05da2-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="05da2-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="05da2-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-119">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="05da2-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-120">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="05da2-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-121">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="05da2-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-122">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="05da2-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="05da2-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="05da2-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="05da2-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="05da2-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="05da2-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="05da2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05da2-127">Requirements</span></span>



| <span data-ttu-id="05da2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="05da2-128">Requirement</span></span> | <span data-ttu-id="05da2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="05da2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05da2-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05da2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="05da2-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="05da2-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="05da2-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05da2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="05da2-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="05da2-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05da2-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="05da2-134">Namespace</span></span><br/>                | <span data-ttu-id="05da2-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="05da2-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="05da2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="05da2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05da2-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05da2-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05da2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="05da2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05da2-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05da2-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05da2-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="05da2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05da2-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="05da2-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

