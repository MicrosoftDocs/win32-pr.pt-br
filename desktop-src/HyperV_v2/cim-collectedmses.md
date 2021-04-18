---
description: Representa uma associação genérica entre uma coleção de elementos do sistema gerenciado e os membros da coleção.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Classe CIM_CollectedMSEs (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780984"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="0faaa-103">Classe CIM_CollectedMSEs (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0faaa-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="0faaa-104">Representa uma associação genérica entre uma coleção de elementos do sistema gerenciado e os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="0faaa-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0faaa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0faaa-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="0faaa-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0faaa-106">Members</span></span>

<span data-ttu-id="0faaa-107">A classe **CIM \_ CollectedMSEs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0faaa-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="0faaa-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0faaa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0faaa-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0faaa-109">Properties</span></span>

<span data-ttu-id="0faaa-110">A classe **CIM \_ CollectedMSEs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0faaa-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0faaa-111">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="0faaa-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0faaa-112">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="0faaa-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="0faaa-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0faaa-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0faaa-114">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("coleção")</span><span class="sxs-lookup"><span data-stu-id="0faaa-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="0faaa-115">A coleção.</span><span class="sxs-lookup"><span data-stu-id="0faaa-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="0faaa-116">**Membro**</span><span class="sxs-lookup"><span data-stu-id="0faaa-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0faaa-117">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="0faaa-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="0faaa-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0faaa-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0faaa-119">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("membro")</span><span class="sxs-lookup"><span data-stu-id="0faaa-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="0faaa-120">Os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="0faaa-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0faaa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0faaa-121">Requirements</span></span>



| <span data-ttu-id="0faaa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0faaa-122">Requirement</span></span> | <span data-ttu-id="0faaa-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0faaa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0faaa-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0faaa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0faaa-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0faaa-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0faaa-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0faaa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0faaa-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0faaa-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0faaa-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0faaa-128">Namespace</span></span><br/>                | <span data-ttu-id="0faaa-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0faaa-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0faaa-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0faaa-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0faaa-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0faaa-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0faaa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0faaa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0faaa-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0faaa-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0faaa-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0faaa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0faaa-135">**\_MEMBEROFCOLLECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="0faaa-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

