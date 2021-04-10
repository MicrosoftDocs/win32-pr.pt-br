---
description: Registra um serviço que fornece objetos relacionados ao pool de recursos globais.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Classe Msvm_ResourcePoolRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091716"
---
# <a name="msvm_resourcepoolregistration-class"></a><span data-ttu-id="4c50b-103">\_Classe Msvm ResourcePoolRegistration</span><span class="sxs-lookup"><span data-stu-id="4c50b-103">Msvm\_ResourcePoolRegistration class</span></span>

<span data-ttu-id="4c50b-104">Registra um serviço que fornece objetos relacionados ao pool de recursos globais.</span><span class="sxs-lookup"><span data-stu-id="4c50b-104">Registers a service that provides global resource pool-related objects.</span></span>

<span data-ttu-id="4c50b-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4c50b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c50b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c50b-106">Syntax</span></span>

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a><span data-ttu-id="4c50b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4c50b-107">Members</span></span>

<span data-ttu-id="4c50b-108">A classe **Msvm \_ ResourcePoolRegistration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4c50b-108">The **Msvm\_ResourcePoolRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4c50b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c50b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c50b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4c50b-110">Properties</span></span>

<span data-ttu-id="4c50b-111">A classe **Msvm \_ ResourcePoolRegistration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4c50b-111">The **Msvm\_ResourcePoolRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c50b-112">**Componente**</span><span class="sxs-lookup"><span data-stu-id="4c50b-112">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c50b-113">Tipo de dados: **[ **Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="4c50b-113">Data type: **[**Msvm\_ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4c50b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c50b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c50b-115">Uma referência a uma instância que descreve o objeto COM que implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="4c50b-115">A reference to an instance that describes the COM object that implements this class.</span></span>

</dd> <dt>

<span data-ttu-id="4c50b-116">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4c50b-116">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c50b-117">Tipo de dados: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span><span class="sxs-lookup"><span data-stu-id="4c50b-117">Data type: **[**Msvm\_ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4c50b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4c50b-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c50b-119">Uma referência a uma instância que descreve um tipo de recurso com suporte pelo serviço.</span><span class="sxs-lookup"><span data-stu-id="4c50b-119">A reference to an instance that describes a resource type supported by the service.</span></span> <span data-ttu-id="4c50b-120">Esta propriedade é herdada de [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4c50b-120">This property is inherited from [**Msvm\_VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c50b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c50b-121">Remarks</span></span>

<span data-ttu-id="4c50b-122">O acesso à classe **Msvm \_ ResourcePoolRegistration** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="4c50b-122">Access to the **Msvm\_ResourcePoolRegistration** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4c50b-123">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4c50b-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c50b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c50b-124">Requirements</span></span>



| <span data-ttu-id="4c50b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c50b-125">Requirement</span></span> | <span data-ttu-id="4c50b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4c50b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c50b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c50b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4c50b-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4c50b-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4c50b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c50b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4c50b-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4c50b-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c50b-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4c50b-131">End of client support</span></span><br/>    | <span data-ttu-id="4c50b-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4c50b-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4c50b-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4c50b-133">End of server support</span></span><br/>    | <span data-ttu-id="4c50b-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4c50b-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4c50b-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c50b-135">Namespace</span></span><br/>                | <span data-ttu-id="4c50b-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4c50b-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4c50b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4c50b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c50b-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c50b-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c50b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4c50b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c50b-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c50b-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4c50b-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c50b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c50b-142">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="4c50b-142">**Msvm\_VirtualizationComponentRegistration**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[<span data-ttu-id="4c50b-143">**Msvm \_ VirtualizationComponentRegistration**</span><span class="sxs-lookup"><span data-stu-id="4c50b-143">**Msvm\_VirtualizationComponentRegistration**</span></span>](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

