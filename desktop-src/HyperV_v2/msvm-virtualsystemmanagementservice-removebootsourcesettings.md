---
description: Remove as configurações de recursos virtuais de uma configuração de sistema virtual.
ms.assetid: 0deb7719-e605-4ba5-9bb2-037d0cafee24
title: Método RemoveBootSourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2693be33d291ea5a975119a5478af580ef2bb3f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789797"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="69897-103">Método RemoveBootSourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="69897-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="69897-104">Remove as configurações de recursos virtuais de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="69897-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="69897-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como os recursos de efeito colateral do sistema virtual ativo podem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="69897-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="69897-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69897-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="69897-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69897-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69897-108">*BootSourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="69897-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69897-109">Referência a uma matriz de [**CIM \_ SettingData**](cim-settingdata.md) que descreve as configurações de origem de inicialização a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="69897-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="69897-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="69897-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69897-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="69897-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69897-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69897-112">Return value</span></span>

<span data-ttu-id="69897-113">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="69897-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="69897-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="69897-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69897-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="69897-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="69897-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="69897-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="69897-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="69897-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="69897-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="69897-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="69897-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="69897-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="69897-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="69897-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="69897-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="69897-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="69897-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="69897-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="69897-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="69897-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="69897-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69897-124">Requirements</span></span>



| <span data-ttu-id="69897-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="69897-125">Requirement</span></span> | <span data-ttu-id="69897-126">Valor</span><span class="sxs-lookup"><span data-stu-id="69897-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69897-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69897-127">Minimum supported client</span></span><br/> | <span data-ttu-id="69897-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="69897-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="69897-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69897-129">Minimum supported server</span></span><br/> | <span data-ttu-id="69897-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="69897-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="69897-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="69897-131">Namespace</span></span><br/>                | <span data-ttu-id="69897-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="69897-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="69897-133">MOF</span><span class="sxs-lookup"><span data-stu-id="69897-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69897-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69897-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69897-135">DLL</span><span class="sxs-lookup"><span data-stu-id="69897-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69897-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69897-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69897-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="69897-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69897-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="69897-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

