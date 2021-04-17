---
description: Adiciona configurações de serviço de convidado a uma configuração de sistema virtual.
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Método AddGuestServiceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5bcdfd8c159e92efe633c04e22af5bceb9d003e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501374"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="25543-103">Método AddGuestServiceSettings da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="25543-103">AddGuestServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="25543-104">Adiciona configurações de serviço de convidado a uma configuração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="25543-104">Adds guest service settings to a virtual system configuration.</span></span>

<span data-ttu-id="25543-105">Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="25543-105">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="25543-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25543-106">Syntax</span></span>


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="25543-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25543-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25543-108">*AffectedConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25543-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25543-109">Referência a um [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) que descreve a configuração afetada.</span><span class="sxs-lookup"><span data-stu-id="25543-109">Reference to a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that describes the affected configuration.</span></span>

</dd> <dt>

<span data-ttu-id="25543-110">*GuestServiceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25543-110">*GuestServiceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25543-111">Uma matriz que contém as configurações do serviço de convidado.</span><span class="sxs-lookup"><span data-stu-id="25543-111">An array containing the guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="25543-112">*ResultingGuestServiceSettings* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="25543-112">*ResultingGuestServiceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25543-113">Em caso de sucesso, contém uma referência a um [**CIM \_ SettingData**](cim-settingdata.md) que descreve as configurações do serviço de convidado resultante.</span><span class="sxs-lookup"><span data-stu-id="25543-113">On success, contains a reference to a [**CIM\_SettingData**](cim-settingdata.md) that describes the resulting guest service settings.</span></span>

</dd> <dt>

<span data-ttu-id="25543-114">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="25543-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25543-115">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="25543-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25543-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25543-116">Return value</span></span>

<span data-ttu-id="25543-117">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="25543-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="25543-118">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="25543-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="25543-119">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="25543-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="25543-120">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="25543-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="25543-121">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="25543-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="25543-122">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="25543-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="25543-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="25543-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="25543-124">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="25543-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="25543-125">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="25543-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="25543-126">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="25543-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="25543-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25543-127">Requirements</span></span>



| <span data-ttu-id="25543-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="25543-128">Requirement</span></span> | <span data-ttu-id="25543-129">Valor</span><span class="sxs-lookup"><span data-stu-id="25543-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25543-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25543-130">Minimum supported client</span></span><br/> | <span data-ttu-id="25543-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="25543-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="25543-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25543-132">Minimum supported server</span></span><br/> | <span data-ttu-id="25543-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="25543-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="25543-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="25543-134">Namespace</span></span><br/>                | <span data-ttu-id="25543-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="25543-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="25543-136">MOF</span><span class="sxs-lookup"><span data-stu-id="25543-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25543-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25543-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="25543-138">DLL</span><span class="sxs-lookup"><span data-stu-id="25543-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25543-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="25543-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="25543-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="25543-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25543-141">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="25543-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

