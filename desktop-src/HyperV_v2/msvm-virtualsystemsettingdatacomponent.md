---
description: Uma associação genérica usada para estabelecer parte de relações entre uma instância do CIM \_ VirtualSystemSettingData e uma ou mais instâncias do CIM \_ ResourceAllocationSettingData.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Classe Msvm_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780972"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="95073-103">\_Classe Msvm VirtualSystemSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="95073-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="95073-104">Uma associação genérica usada para estabelecer a "parte de" relações entre uma instância do [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) e uma ou mais instâncias do [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="95073-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="95073-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="95073-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="95073-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95073-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="95073-107">Membros</span><span class="sxs-lookup"><span data-stu-id="95073-107">Members</span></span>

<span data-ttu-id="95073-108">A classe **Msvm \_ VirtualSystemSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="95073-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="95073-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95073-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95073-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="95073-110">Properties</span></span>

<span data-ttu-id="95073-111">A classe **Msvm \_ VirtualSystemSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="95073-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95073-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="95073-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95073-113">Tipo de dados: **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="95073-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="95073-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95073-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95073-115">Qualificadores: **override**, **min** (1), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="95073-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="95073-116">O elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="95073-116">The parent element in the association.</span></span> <span data-ttu-id="95073-117">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="95073-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="95073-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="95073-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95073-119">Tipo de dados: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="95073-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="95073-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="95073-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95073-121">O elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="95073-121">The child element in the association.</span></span> <span data-ttu-id="95073-122">Essa propriedade é herdada do [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="95073-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95073-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="95073-123">Remarks</span></span>

<span data-ttu-id="95073-124">O acesso à classe **Msvm \_ VirtualSystemSettingDataComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="95073-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="95073-125">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="95073-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="95073-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95073-126">Requirements</span></span>



| <span data-ttu-id="95073-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="95073-127">Requirement</span></span> | <span data-ttu-id="95073-128">Valor</span><span class="sxs-lookup"><span data-stu-id="95073-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95073-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95073-129">Minimum supported client</span></span><br/> | <span data-ttu-id="95073-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95073-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="95073-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95073-131">Minimum supported server</span></span><br/> | <span data-ttu-id="95073-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="95073-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95073-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="95073-133">Namespace</span></span><br/>                | <span data-ttu-id="95073-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="95073-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="95073-135">MOF</span><span class="sxs-lookup"><span data-stu-id="95073-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95073-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95073-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95073-137">DLL</span><span class="sxs-lookup"><span data-stu-id="95073-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95073-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95073-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95073-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="95073-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95073-140">**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="95073-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="95073-141">[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95073-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="95073-142">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="95073-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

