---
description: Adiciona fontes de inicialização a uma configuração de sistema virtual quando aplicada a um &\# 0034; state&\# 0034; configuração do sistema virtual.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Método AddBootSourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e20a1184e11113ba25ac060ec19dab5d2391b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089998"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f4606-103">Método AddBootSourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="f4606-103">AddBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f4606-104">Adiciona fontes de inicialização a uma configuração de sistema virtual quando aplicada a uma configuração de sistema virtual "State".</span><span class="sxs-lookup"><span data-stu-id="f4606-104">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4606-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4606-105">Syntax</span></span>


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f4606-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4606-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4606-107">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4606-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4606-108">Um [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) que contém a configuração afetada.</span><span class="sxs-lookup"><span data-stu-id="f4606-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f4606-109">*BootSourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4606-109">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4606-110">Uma matriz que contém as configurações de origem da inicialização.</span><span class="sxs-lookup"><span data-stu-id="f4606-110">An array containing the boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="f4606-111">*ResultingBootSourceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f4606-111">*ResultingBootSourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4606-112">Em caso de sucesso, retorna um [**CIM \_ SettingData**](cim-settingdata.md) com as configurações de origem de inicialização resultantes.</span><span class="sxs-lookup"><span data-stu-id="f4606-112">On success, returns a [**CIM\_SettingData**](cim-settingdata.md) with the resulting boot source settings.</span></span>

</dd> <dt>

<span data-ttu-id="f4606-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f4606-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4606-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f4606-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4606-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4606-115">Return value</span></span>

<span data-ttu-id="f4606-116">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f4606-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f4606-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f4606-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-118">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="f4606-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-119">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="f4606-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-120">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="f4606-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-121">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="f4606-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="f4606-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f4606-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-124">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f4606-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f4606-125">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f4606-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f4606-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4606-126">Requirements</span></span>



| <span data-ttu-id="f4606-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4606-127">Requirement</span></span> | <span data-ttu-id="f4606-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f4606-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4606-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4606-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f4606-130">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f4606-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f4606-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4606-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f4606-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f4606-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f4606-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4606-133">Namespace</span></span><br/>                | <span data-ttu-id="f4606-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f4606-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f4606-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f4606-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4606-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4606-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4606-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f4606-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4606-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4606-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4606-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4606-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4606-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f4606-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

