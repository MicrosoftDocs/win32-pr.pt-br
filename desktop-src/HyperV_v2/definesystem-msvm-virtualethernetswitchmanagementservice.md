---
description: Cria um novo comutador virtual.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Método DefineSystem da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829368"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="3eae4-103">Método DefineSystem da \_ classe VirtualEthernetSwitchManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="3eae4-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="3eae4-104">Cria um novo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="3eae4-104">Creates a new virtual switch.</span></span> <span data-ttu-id="3eae4-105">As propriedades que não forem especificadas serão preenchidas com valores padrão.</span><span class="sxs-lookup"><span data-stu-id="3eae4-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eae4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eae4-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3eae4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eae4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eae4-108">*SystemSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eae4-109">Uma instância inserida da classe [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que é usada para definir os atributos do comutador virtual a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3eae4-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="3eae4-110">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="3eae4-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="3eae4-111">*ResourceSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eae4-112">Uma matriz de instâncias inseridas da classe [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que descreve as configurações das portas de comutador a serem criadas no escopo do novo comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="3eae4-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="3eae4-113">Se **NULL** for especificado, o comutador virtual será criado sem recursos (ou seja, sem portas de comutador).</span><span class="sxs-lookup"><span data-stu-id="3eae4-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="3eae4-114">*ReferenceConfiguration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eae4-115">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="3eae4-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3eae4-116">*ResultingSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3eae4-117">Se um comutador virtual for criado com êxito, uma referência a uma instância da classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o comutador virtual recém-definido.</span><span class="sxs-lookup"><span data-stu-id="3eae4-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="3eae4-118">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3eae4-119">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3eae4-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eae4-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3eae4-120">Return value</span></span>

<span data-ttu-id="3eae4-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3eae4-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3eae4-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="3eae4-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-123">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="3eae4-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-124">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="3eae4-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-125">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="3eae4-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-126">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="3eae4-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-127">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3eae4-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-128">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="3eae4-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-129">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3eae4-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3eae4-130">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3eae4-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3eae4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eae4-131">Requirements</span></span>



| <span data-ttu-id="3eae4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eae4-132">Requirement</span></span> | <span data-ttu-id="3eae4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3eae4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eae4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3eae4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3eae4-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3eae4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3eae4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3eae4-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3eae4-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3eae4-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="3eae4-138">Namespace</span></span><br/>                | <span data-ttu-id="3eae4-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3eae4-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3eae4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3eae4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3eae4-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3eae4-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3eae4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3eae4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eae4-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3eae4-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3eae4-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eae4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eae4-145">**Msvm \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="3eae4-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

