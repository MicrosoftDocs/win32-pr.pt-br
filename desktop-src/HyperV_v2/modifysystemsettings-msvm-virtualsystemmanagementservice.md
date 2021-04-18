---
description: Modifica as configurações da máquina virtual.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Método ModifySystemSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766899"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="14db7-103">Método ModifySystemSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="14db7-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="14db7-104">Modifica as configurações da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="14db7-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="14db7-105">Quando aplicado às configurações do sistema de uma configuração de máquina virtual "atual", como um efeito colateral, a instância da máquina virtual pode ser modificada.</span><span class="sxs-lookup"><span data-stu-id="14db7-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="14db7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14db7-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="14db7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14db7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14db7-108">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14db7-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14db7-109">Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que contém os aspectos modificados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="14db7-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="14db7-110">A propriedade **InstanceId** identifica a configuração da máquina virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="14db7-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="14db7-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="14db7-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14db7-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="14db7-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14db7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14db7-113">Return value</span></span>

<span data-ttu-id="14db7-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="14db7-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="14db7-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="14db7-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-116">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="14db7-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-117">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="14db7-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-118">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="14db7-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-119">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="14db7-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-120">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="14db7-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-121">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="14db7-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="14db7-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="14db7-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="14db7-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="14db7-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="14db7-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="14db7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14db7-126">Requirements</span></span>



| <span data-ttu-id="14db7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="14db7-127">Requirement</span></span> | <span data-ttu-id="14db7-128">Valor</span><span class="sxs-lookup"><span data-stu-id="14db7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14db7-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14db7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="14db7-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="14db7-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="14db7-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14db7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="14db7-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="14db7-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14db7-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="14db7-133">Namespace</span></span><br/>                | <span data-ttu-id="14db7-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="14db7-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="14db7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="14db7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14db7-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14db7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="14db7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14db7-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14db7-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14db7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="14db7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14db7-140">**ModifyVirtualSystem (v1)**</span><span class="sxs-lookup"><span data-stu-id="14db7-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="14db7-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="14db7-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

