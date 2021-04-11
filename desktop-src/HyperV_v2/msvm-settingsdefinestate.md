---
description: Associa uma máquina virtual e seus dispositivos a instâncias do CIM \_ SettingData que representam as configurações atuais que se aplicam a esses objetos.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Classe Msvm_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170252"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="15147-103">\_Classe Msvm SettingsDefineState</span><span class="sxs-lookup"><span data-stu-id="15147-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="15147-104">Associa uma máquina virtual e seus dispositivos a instâncias do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que representam as configurações atuais que se aplicam a esses objetos.</span><span class="sxs-lookup"><span data-stu-id="15147-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="15147-105">Mais especificamente, ele associa o [**Msvm \_ ComputerSystem**](msvm-computersystem.md) a instâncias [**de Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)e associa \**Msvm \_ \** _ derivados de [_ *CIM \_ LogicalDevice* \*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) com \**Msvm \_ \** _ derivados de [_ *CIM \_ ResourceAllocationSettingData*. \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)</span><span class="sxs-lookup"><span data-stu-id="15147-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="15147-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="15147-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15147-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15147-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="15147-108">Membros</span><span class="sxs-lookup"><span data-stu-id="15147-108">Members</span></span>

<span data-ttu-id="15147-109">A classe **Msvm \_ SettingsDefineState** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="15147-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="15147-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15147-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15147-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15147-111">Properties</span></span>

<span data-ttu-id="15147-112">A classe **Msvm \_ SettingsDefineState** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="15147-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15147-113">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="15147-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15147-114">Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="15147-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="15147-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15147-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15147-116">Uma referência à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="15147-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="15147-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="15147-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15147-118">Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="15147-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="15147-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15147-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15147-120">Uma referência às configurações ativas no momento para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="15147-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15147-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="15147-121">Remarks</span></span>

<span data-ttu-id="15147-122">O acesso à classe **Msvm \_ SettingsDefineState** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="15147-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="15147-123">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="15147-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="15147-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15147-124">Requirements</span></span>



| <span data-ttu-id="15147-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="15147-125">Requirement</span></span> | <span data-ttu-id="15147-126">Valor</span><span class="sxs-lookup"><span data-stu-id="15147-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15147-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15147-127">Minimum supported client</span></span><br/> | <span data-ttu-id="15147-128">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15147-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="15147-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15147-129">Minimum supported server</span></span><br/> | <span data-ttu-id="15147-130">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="15147-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15147-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="15147-131">Namespace</span></span><br/>                | <span data-ttu-id="15147-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="15147-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15147-133">MOF</span><span class="sxs-lookup"><span data-stu-id="15147-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15147-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15147-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15147-135">DLL</span><span class="sxs-lookup"><span data-stu-id="15147-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15147-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15147-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15147-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="15147-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15147-138">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="15147-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="15147-139">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="15147-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="15147-140">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="15147-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

