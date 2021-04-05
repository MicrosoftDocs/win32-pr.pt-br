---
description: Modifica as configurações do serviço convidado.
ms.assetid: a308aa59-bd43-4dd5-a690-c435102e8043
title: Método ModifyGuestServiceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bc0af24346c445022ba3f8725ea6102c61dc9c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826861"
---
# <a name="modifyguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="00bb2-103">Método ModifyGuestServiceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="00bb2-103">ModifyGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="00bb2-104">Modifica as configurações do serviço convidado.</span><span class="sxs-lookup"><span data-stu-id="00bb2-104">Modifies guest service settings.</span></span>

<span data-ttu-id="00bb2-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="00bb2-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="00bb2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00bb2-106">Syntax</span></span>


```mof
uint32 ModifyGuestServiceSettings(
  [in]  string              GuestServiceSettings[],
  [out] CIM_SettingData REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="00bb2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00bb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00bb2-108">*GuestServiceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00bb2-108">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00bb2-109">Uma matriz que contém as novas configurações do serviço de convidado.</span><span class="sxs-lookup"><span data-stu-id="00bb2-109">An array that contains the new guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="00bb2-110">*ResultingGuestServiceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="00bb2-110">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00bb2-111">Em caso de sucesso, contiains uma matriz de [**CIM \_ SettingData**](cim-settingdata.md) que faz referência às configurações do serviço de convidado resultante.</span><span class="sxs-lookup"><span data-stu-id="00bb2-111">On success, contiains an array of [**CIM\_SettingData**](cim-settingdata.md) that reference the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="00bb2-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="00bb2-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00bb2-113">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00bb2-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00bb2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00bb2-114">Return value</span></span>

<span data-ttu-id="00bb2-115">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="00bb2-115">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="00bb2-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="00bb2-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="00bb2-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-118">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="00bb2-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="00bb2-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-120">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="00bb2-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-121">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="00bb2-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-122">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="00bb2-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="00bb2-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="00bb2-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="00bb2-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="00bb2-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="00bb2-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="00bb2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00bb2-127">Requirements</span></span>



| <span data-ttu-id="00bb2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="00bb2-128">Requirement</span></span> | <span data-ttu-id="00bb2-129">Valor</span><span class="sxs-lookup"><span data-stu-id="00bb2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00bb2-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00bb2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00bb2-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="00bb2-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="00bb2-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00bb2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00bb2-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="00bb2-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="00bb2-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="00bb2-134">Namespace</span></span><br/>                | <span data-ttu-id="00bb2-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="00bb2-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="00bb2-136">MOF</span><span class="sxs-lookup"><span data-stu-id="00bb2-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00bb2-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00bb2-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00bb2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00bb2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00bb2-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00bb2-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="00bb2-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="00bb2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00bb2-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="00bb2-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

