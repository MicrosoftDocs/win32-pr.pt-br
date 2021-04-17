---
description: Remove as configurações de serviço de convidado de uma configuração de sistema virtual.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Método RemoveGuestServiceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782349"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="3c67c-103">Método RemoveGuestServiceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="3c67c-103">RemoveGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="3c67c-104">Remove as configurações de serviço de convidado de uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="3c67c-104">Removes guest service settings from a virtual system configuration.</span></span>

<span data-ttu-id="3c67c-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="3c67c-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c67c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c67c-106">Syntax</span></span>


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3c67c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c67c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c67c-108">*GuestServiceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c67c-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c67c-109">Referência a uma matriz de [**CIM \_ SettingData**](cim-settingdata.md) que descreve a configuração do serviço de convidado a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3c67c-109">Reference to an array of [**CIM\_SettingData**](cim-settingdata.md) that describe the guest service setting to remove.</span></span>

</dd> <dt>

<span data-ttu-id="3c67c-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3c67c-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c67c-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c67c-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c67c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c67c-112">Return value</span></span>

<span data-ttu-id="3c67c-113">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3c67c-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3c67c-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3c67c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3c67c-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="3c67c-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="3c67c-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="3c67c-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="3c67c-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3c67c-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3c67c-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-122">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3c67c-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3c67c-123">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3c67c-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3c67c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c67c-124">Requirements</span></span>



| <span data-ttu-id="3c67c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c67c-125">Requirement</span></span> | <span data-ttu-id="3c67c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3c67c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c67c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c67c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3c67c-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3c67c-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3c67c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c67c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3c67c-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c67c-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3c67c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c67c-131">Namespace</span></span><br/>                | <span data-ttu-id="3c67c-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3c67c-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c67c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3c67c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c67c-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c67c-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c67c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3c67c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c67c-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c67c-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c67c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c67c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c67c-138">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="3c67c-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

