---
description: Associa um sistema a um dispositivo lógico que é um componente do sistema.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: Classe CIM_SystemDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757422"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="6c904-103">Classe CIM_SystemDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="6c904-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="6c904-104">Associa um sistema a um dispositivo lógico que é um componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="6c904-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c904-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c904-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6c904-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6c904-106">Members</span></span>

<span data-ttu-id="6c904-107">A classe **CIM \_ SystemDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6c904-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="6c904-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c904-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c904-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c904-109">Properties</span></span>

<span data-ttu-id="6c904-110">A classe **CIM \_ SystemDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6c904-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c904-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6c904-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c904-112">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="6c904-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="6c904-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c904-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c904-114">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6c904-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6c904-115">Uma referência do [**\_ sistema CIM**](cim-system.md) para o sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="6c904-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="6c904-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6c904-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c904-117">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="6c904-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6c904-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c904-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c904-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6c904-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6c904-120">Uma referência de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) para o dispositivo lógico que é um componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="6c904-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c904-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c904-121">Requirements</span></span>



| <span data-ttu-id="6c904-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c904-122">Requirement</span></span> | <span data-ttu-id="6c904-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6c904-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c904-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c904-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c904-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6c904-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6c904-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c904-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c904-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c904-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6c904-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c904-128">Namespace</span></span><br/>                | <span data-ttu-id="6c904-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6c904-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c904-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6c904-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c904-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c904-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c904-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6c904-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c904-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c904-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c904-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c904-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c904-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6c904-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

