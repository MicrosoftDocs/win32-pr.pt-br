---
description: Representa uma associação genérica usada para estabelecer as partes de uma relação entre elementos gerenciados.
ms.assetid: 9785ea8b-fb76-4ffe-8649-aa2fe1b01d5f
title: Classe CIM_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteComponent
- CIM_ConcreteComponent.GroupComponent
- CIM_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77ee0f33f540bfd215ec10a24c3c574976189d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828721"
---
# <a name="cim_concretecomponent-class"></a><span data-ttu-id="24217-103">\_Classe CIM ConcreteComponent</span><span class="sxs-lookup"><span data-stu-id="24217-103">CIM\_ConcreteComponent class</span></span>

<span data-ttu-id="24217-104">Representa uma associação genérica usada para estabelecer as partes de uma relação entre elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="24217-104">Represents a generic association used to establish the parts of a relationship between managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="24217-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24217-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteComponent : CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="24217-106">Membros</span><span class="sxs-lookup"><span data-stu-id="24217-106">Members</span></span>

<span data-ttu-id="24217-107">A classe **CIM \_ ConcreteComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="24217-107">The **CIM\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="24217-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="24217-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24217-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="24217-109">Properties</span></span>

<span data-ttu-id="24217-110">A classe **CIM \_ ConcreteComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="24217-110">The **CIM\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24217-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="24217-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24217-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="24217-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="24217-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24217-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24217-114">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="24217-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="24217-115">O elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="24217-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="24217-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="24217-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24217-117">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="24217-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="24217-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="24217-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24217-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="24217-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="24217-120">O elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="24217-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24217-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24217-121">Requirements</span></span>



| <span data-ttu-id="24217-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="24217-122">Requirement</span></span> | <span data-ttu-id="24217-123">Valor</span><span class="sxs-lookup"><span data-stu-id="24217-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24217-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24217-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24217-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="24217-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="24217-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24217-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24217-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24217-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="24217-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="24217-128">Namespace</span></span><br/>                | <span data-ttu-id="24217-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="24217-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24217-130">MOF</span><span class="sxs-lookup"><span data-stu-id="24217-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24217-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24217-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24217-132">DLL</span><span class="sxs-lookup"><span data-stu-id="24217-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24217-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24217-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24217-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="24217-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24217-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="24217-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

