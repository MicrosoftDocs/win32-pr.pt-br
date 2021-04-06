---
description: Representa uma relação na qual um elemento gerenciado é um membro e é agregado por uma coleção.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: Classe CIM_MemberOfCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011311"
---
# <a name="cim_memberofcollection-class"></a><span data-ttu-id="6309a-103">\_Classe CIM MemberOfCollection</span><span class="sxs-lookup"><span data-stu-id="6309a-103">CIM\_MemberOfCollection class</span></span>

<span data-ttu-id="6309a-104">Representa uma relação na qual um elemento gerenciado é um membro e é agregado por uma coleção.</span><span class="sxs-lookup"><span data-stu-id="6309a-104">Represents a relationship in which a managed element is a member of and is aggregated by a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6309a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6309a-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="6309a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6309a-106">Members</span></span>

<span data-ttu-id="6309a-107">A classe **CIM \_ MemberOfCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6309a-107">The **CIM\_MemberOfCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="6309a-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6309a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6309a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6309a-109">Properties</span></span>

<span data-ttu-id="6309a-110">A classe **CIM \_ MemberOfCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6309a-110">The **CIM\_MemberOfCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6309a-111">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="6309a-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6309a-112">Tipo de dados **: \_ coleção CIM**</span><span class="sxs-lookup"><span data-stu-id="6309a-112">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="6309a-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6309a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6309a-114">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6309a-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6309a-115">A coleção que agrega os membros.</span><span class="sxs-lookup"><span data-stu-id="6309a-115">The collection that aggregates members.</span></span>

</dd> <dt>

<span data-ttu-id="6309a-116">**Membro**</span><span class="sxs-lookup"><span data-stu-id="6309a-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6309a-117">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="6309a-117">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="6309a-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6309a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6309a-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6309a-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6309a-120">O membro da coleção.</span><span class="sxs-lookup"><span data-stu-id="6309a-120">The member of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6309a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6309a-121">Requirements</span></span>



| <span data-ttu-id="6309a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6309a-122">Requirement</span></span> | <span data-ttu-id="6309a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6309a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6309a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6309a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6309a-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6309a-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6309a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6309a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6309a-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6309a-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6309a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="6309a-128">Namespace</span></span><br/>                | <span data-ttu-id="6309a-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6309a-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6309a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="6309a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6309a-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6309a-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6309a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6309a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6309a-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6309a-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

