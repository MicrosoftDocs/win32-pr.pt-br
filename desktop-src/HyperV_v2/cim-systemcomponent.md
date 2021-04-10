---
description: Representa uma associação entre um sistema e um dos elementos que o compõem.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: Classe CIM_SystemComponent (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827889"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="83f38-103">Classe CIM_SystemComponent (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="83f38-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="83f38-104">Representa uma associação entre um sistema e um dos elementos que o compõem.</span><span class="sxs-lookup"><span data-stu-id="83f38-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="83f38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83f38-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="83f38-106">Membros</span><span class="sxs-lookup"><span data-stu-id="83f38-106">Members</span></span>

<span data-ttu-id="83f38-107">A classe **CIM \_ Systemcomponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="83f38-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="83f38-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83f38-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="83f38-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="83f38-109">Properties</span></span>

<span data-ttu-id="83f38-110">A classe **CIM \_ Systemcomponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="83f38-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="83f38-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="83f38-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83f38-112">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="83f38-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="83f38-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83f38-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83f38-114">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="83f38-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="83f38-115">O [**\_ sistema CIM**](cim-system.md) que contém o **PartComponent**.</span><span class="sxs-lookup"><span data-stu-id="83f38-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="83f38-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="83f38-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="83f38-117">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="83f38-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="83f38-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="83f38-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="83f38-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="83f38-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="83f38-120">O [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) filho que é um componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="83f38-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83f38-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83f38-121">Requirements</span></span>



| <span data-ttu-id="83f38-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="83f38-122">Requirement</span></span> | <span data-ttu-id="83f38-123">Valor</span><span class="sxs-lookup"><span data-stu-id="83f38-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f38-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83f38-124">Minimum supported client</span></span><br/> | <span data-ttu-id="83f38-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="83f38-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="83f38-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83f38-126">Minimum supported server</span></span><br/> | <span data-ttu-id="83f38-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83f38-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="83f38-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="83f38-128">Namespace</span></span><br/>                | <span data-ttu-id="83f38-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="83f38-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="83f38-130">MOF</span><span class="sxs-lookup"><span data-stu-id="83f38-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83f38-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83f38-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="83f38-132">DLL</span><span class="sxs-lookup"><span data-stu-id="83f38-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83f38-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="83f38-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="83f38-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="83f38-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83f38-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="83f38-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

