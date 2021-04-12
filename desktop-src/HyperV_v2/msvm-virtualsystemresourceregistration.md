---
description: Registra um serviço que fornece objetos relacionados a recursos específicos da máquina virtual.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Classe Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501367"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a><span data-ttu-id="fa739-103">\_Classe Msvm VirtualSystemResourceRegistration</span><span class="sxs-lookup"><span data-stu-id="fa739-103">Msvm\_VirtualSystemResourceRegistration class</span></span>

<span data-ttu-id="fa739-104">Registra um serviço que fornece objetos relacionados a recursos específicos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fa739-104">Registers a service that provides virtual machine-specific resource-related objects.</span></span>

<span data-ttu-id="fa739-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fa739-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa739-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa739-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a><span data-ttu-id="fa739-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fa739-107">Members</span></span>

<span data-ttu-id="fa739-108">A classe **Msvm \_ VirtualSystemResourceRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fa739-108">The **Msvm\_VirtualSystemResourceRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="fa739-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa739-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa739-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa739-110">Properties</span></span>

<span data-ttu-id="fa739-111">A classe **Msvm \_ VirtualSystemResourceRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa739-111">The **Msvm\_VirtualSystemResourceRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa739-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="fa739-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa739-113">Tipo de dados: **[ **Msvm \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="fa739-113">Data type: **[**Msvm\_VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa739-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa739-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa739-115">Uma referência a uma instância que descreve o objeto COM que implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="fa739-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="fa739-116">**IsRootDevice**</span><span class="sxs-lookup"><span data-stu-id="fa739-116">**IsRootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa739-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fa739-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa739-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa739-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa739-119">**True** se esse registro indicar se o tipo de recurso especificado é o dispositivo raiz (ou menos) para este serviço; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa739-119">**True** if this registration indicates whether the specified resource type is the root (or parent-less) device for this service; otherwise, **False**.</span></span> <span data-ttu-id="fa739-120">Somente um registro pode existir quando **IsRootDevice** é definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="fa739-120">Only one registration can exist when **IsRootDevice** is set to **True**.</span></span> <span data-ttu-id="fa739-121">Caso contrário, esse registro representa um mapeamento para um subdispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa739-121">Otherwise, this registration represents a mapping to a sub-device.</span></span> <span data-ttu-id="fa739-122">Essa propriedade é sempre definida como **false**.</span><span class="sxs-lookup"><span data-stu-id="fa739-122">This property is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="fa739-123">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fa739-123">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa739-124">Tipo de dados: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="fa739-124">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fa739-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa739-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa739-126">Uma referência a uma instância que descreve um tipo de recurso com suporte pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="fa739-126">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="fa739-127">Esta propriedade é herdada de [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="fa739-127">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa739-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa739-128">Remarks</span></span>

<span data-ttu-id="fa739-129">O acesso à classe **Msvm \_ VirtualSystemResourceRegistration** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="fa739-129">Access to the **Msvm\_VirtualSystemResourceRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fa739-130">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fa739-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa739-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa739-131">Requirements</span></span>



| <span data-ttu-id="fa739-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa739-132">Requirement</span></span> | <span data-ttu-id="fa739-133">Valor</span><span class="sxs-lookup"><span data-stu-id="fa739-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa739-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa739-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fa739-135">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fa739-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fa739-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa739-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fa739-137">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fa739-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa739-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fa739-138">End of client support</span></span><br/>    | <span data-ttu-id="fa739-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fa739-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fa739-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fa739-140">End of server support</span></span><br/>    | <span data-ttu-id="fa739-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fa739-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fa739-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa739-142">Namespace</span></span><br/>                | <span data-ttu-id="fa739-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fa739-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fa739-144">MOF</span><span class="sxs-lookup"><span data-stu-id="fa739-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa739-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa739-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa739-146">DLL</span><span class="sxs-lookup"><span data-stu-id="fa739-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa739-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa739-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa739-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa739-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa739-149">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="fa739-149">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="fa739-150">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="fa739-150">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

