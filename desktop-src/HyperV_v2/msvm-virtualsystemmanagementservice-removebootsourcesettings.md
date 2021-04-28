---
description: Método RemoveBootSourceSettings da classe Msvm_VirtualSystemManagementService-remove as configurações de recurso virtual de uma configuração de sistema virtual.
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
ms.openlocfilehash: 5407e56b761dd545d20b89e0a28742f9c542b15a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109394"
---
# <a name="removebootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="02e15-103">Método RemoveBootSourceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="02e15-103">RemoveBootSourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="02e15-104">Remove as configurações de recursos virtuais de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="02e15-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="02e15-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como os recursos de efeito colateral do sistema virtual ativo podem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="02e15-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e15-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02e15-106">Syntax</span></span>


```mof
uint32 RemoveBootSourceSettings(
  [in]  CIM_SettingData REF BootSourceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="02e15-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02e15-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e15-108">*BootSourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02e15-108">*BootSourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e15-109">Referência a uma matriz de [**CIM \_ SettingData**](cim-settingdata.md) que descreve as configurações de origem de inicialização a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="02e15-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the boot source settings to remove.</span></span>

</dd> <dt>

<span data-ttu-id="02e15-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="02e15-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02e15-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="02e15-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e15-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="02e15-112">Return value</span></span>

<span data-ttu-id="02e15-113">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="02e15-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="02e15-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="02e15-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="02e15-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="02e15-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="02e15-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="02e15-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="02e15-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="02e15-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="02e15-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="02e15-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="02e15-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="02e15-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="02e15-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02e15-124">Requirements</span></span>



| <span data-ttu-id="02e15-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e15-125">Requirement</span></span> | <span data-ttu-id="02e15-126">Valor</span><span class="sxs-lookup"><span data-stu-id="02e15-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e15-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02e15-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02e15-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="02e15-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="02e15-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02e15-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02e15-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="02e15-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="02e15-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="02e15-131">Namespace</span></span><br/>                | <span data-ttu-id="02e15-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="02e15-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02e15-133">MOF</span><span class="sxs-lookup"><span data-stu-id="02e15-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02e15-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02e15-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02e15-135">DLL</span><span class="sxs-lookup"><span data-stu-id="02e15-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e15-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02e15-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02e15-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="02e15-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e15-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="02e15-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

