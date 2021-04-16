---
description: Associa um dispositivo lógico ao sistema pai.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Classe Msvm_SystemDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747798"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="89e72-103">\_Classe Msvm SystemDevice</span><span class="sxs-lookup"><span data-stu-id="89e72-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="89e72-104">Os dispositivos lógicos podem ser agregados por um sistema.</span><span class="sxs-lookup"><span data-stu-id="89e72-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="89e72-105">Essa relação se torna explícita pela Associação de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="89e72-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="89e72-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="89e72-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e72-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89e72-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="89e72-108">Membros</span><span class="sxs-lookup"><span data-stu-id="89e72-108">Members</span></span>

<span data-ttu-id="89e72-109">A classe **Msvm \_ SystemDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="89e72-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="89e72-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89e72-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89e72-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="89e72-111">Properties</span></span>

<span data-ttu-id="89e72-112">A classe **Msvm \_ SystemDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="89e72-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89e72-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="89e72-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e72-114">Tipo de dados: **[ **\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="89e72-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="89e72-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89e72-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89e72-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="89e72-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="89e72-117">O sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="89e72-117">The parent system in the association.</span></span> <span data-ttu-id="89e72-118">Esta propriedade é herdada [**do \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="89e72-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="89e72-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="89e72-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89e72-120">Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="89e72-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="89e72-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="89e72-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89e72-122">O dispositivo lógico que é um elemento de um sistema.</span><span class="sxs-lookup"><span data-stu-id="89e72-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="89e72-123">Esta propriedade é herdada [**do \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="89e72-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89e72-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="89e72-124">Remarks</span></span>

<span data-ttu-id="89e72-125">O acesso à classe **Msvm \_ SystemDevice** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="89e72-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="89e72-126">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="89e72-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="89e72-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89e72-127">Requirements</span></span>



| <span data-ttu-id="89e72-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e72-128">Requirement</span></span> | <span data-ttu-id="89e72-129">Valor</span><span class="sxs-lookup"><span data-stu-id="89e72-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89e72-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e72-130">Minimum supported client</span></span><br/> | <span data-ttu-id="89e72-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="89e72-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="89e72-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89e72-132">Minimum supported server</span></span><br/> | <span data-ttu-id="89e72-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="89e72-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89e72-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="89e72-134">Namespace</span></span><br/>                | <span data-ttu-id="89e72-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="89e72-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="89e72-136">MOF</span><span class="sxs-lookup"><span data-stu-id="89e72-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89e72-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89e72-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="89e72-138">DLL</span><span class="sxs-lookup"><span data-stu-id="89e72-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e72-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="89e72-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="89e72-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="89e72-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e72-141">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="89e72-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="89e72-142">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="89e72-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="89e72-143">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="89e72-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

