---
description: Modifica as configurações do comutador virtual.
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Método ModifySystemSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775733"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="501b7-103">Método ModifySystemSettings da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="501b7-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="501b7-104">Modifica as configurações do comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="501b7-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="501b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="501b7-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="501b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="501b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="501b7-107">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="501b7-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="501b7-108">Uma instância inserida da classe [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que contém os aspectos modificados do comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="501b7-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="501b7-109">A propriedade **InstanceId** identifica a configuração do comutador virtual a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="501b7-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="501b7-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="501b7-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="501b7-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="501b7-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="501b7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="501b7-112">Return value</span></span>

<span data-ttu-id="501b7-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="501b7-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="501b7-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="501b7-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-115">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="501b7-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-116">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="501b7-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-117">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="501b7-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-118">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="501b7-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-119">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="501b7-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-120">**Parâmetros incompatíveis** (6)</span><span class="sxs-lookup"><span data-stu-id="501b7-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="501b7-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-122">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="501b7-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-123">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="501b7-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="501b7-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="501b7-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="501b7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="501b7-125">Requirements</span></span>



| <span data-ttu-id="501b7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="501b7-126">Requirement</span></span> | <span data-ttu-id="501b7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="501b7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="501b7-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="501b7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="501b7-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="501b7-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="501b7-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="501b7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="501b7-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="501b7-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="501b7-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="501b7-132">Namespace</span></span><br/>                | <span data-ttu-id="501b7-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="501b7-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="501b7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="501b7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="501b7-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="501b7-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="501b7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="501b7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="501b7-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="501b7-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="501b7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="501b7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501b7-139">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="501b7-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

