---
description: Representa uma associação genérica entre um elemento gerenciado pai e um elemento gerenciado filho em que o filho representa um componente ou parte do pai.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Classe CIM_Component (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761722"
---
# <a name="cim_component-class-hyper-v-management"></a><span data-ttu-id="d1e02-103">Classe CIM_Component (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d1e02-103">CIM_Component class (Hyper-V management)</span></span>

<span data-ttu-id="d1e02-104">Representa uma associação genérica entre um elemento gerenciado pai e um elemento gerenciado filho em que o filho representa um componente ou parte do pai.</span><span class="sxs-lookup"><span data-stu-id="d1e02-104">Represents a generic association between a parent managed element and a child managed element where the child represents a component or part of the parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1e02-105">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d1e02-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d1e02-106">Members</span></span>

<span data-ttu-id="d1e02-107">A classe de **\_ componente CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1e02-107">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="d1e02-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1e02-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1e02-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1e02-109">Properties</span></span>

<span data-ttu-id="d1e02-110">A classe de **\_ componente CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1e02-110">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1e02-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d1e02-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e02-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="d1e02-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d1e02-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1e02-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e02-114">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1e02-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1e02-115">O elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="d1e02-115">The parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d1e02-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d1e02-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e02-117">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="d1e02-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d1e02-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1e02-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e02-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1e02-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1e02-120">O elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="d1e02-120">The child element in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1e02-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1e02-121">Requirements</span></span>



| <span data-ttu-id="d1e02-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e02-122">Requirement</span></span> | <span data-ttu-id="d1e02-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d1e02-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e02-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1e02-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e02-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d1e02-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d1e02-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1e02-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e02-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1e02-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d1e02-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1e02-128">Namespace</span></span><br/>                | <span data-ttu-id="d1e02-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d1e02-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d1e02-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d1e02-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1e02-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1e02-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1e02-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e02-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e02-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1e02-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

