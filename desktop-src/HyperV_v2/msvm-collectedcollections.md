---
description: Msvm_CollectedCollections classe – associa os \_ VirtualSystemCollection Msvm aos \_ objetos Msvm ComputerSystem contidos.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Classe Msvm_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112124"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="735c2-103">\_Classe Msvm CollectedCollections</span><span class="sxs-lookup"><span data-stu-id="735c2-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="735c2-104">Associa o [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) aos objetos [**Msvm \_ ComputerSystem**](msvm-computersystem.md) contidos.</span><span class="sxs-lookup"><span data-stu-id="735c2-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="735c2-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="735c2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="735c2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="735c2-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="735c2-107">Membros</span><span class="sxs-lookup"><span data-stu-id="735c2-107">Members</span></span>

<span data-ttu-id="735c2-108">A classe **Msvm \_ CollectedCollections** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="735c2-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="735c2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="735c2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="735c2-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="735c2-110">Properties</span></span>

<span data-ttu-id="735c2-111">A classe **Msvm \_ CollectedCollections** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="735c2-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="735c2-112">**Coleção**</span><span class="sxs-lookup"><span data-stu-id="735c2-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="735c2-113">Tipo de dados: **Msvm \_ managementcollection**</span><span class="sxs-lookup"><span data-stu-id="735c2-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="735c2-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="735c2-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="735c2-115">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("coleção")</span><span class="sxs-lookup"><span data-stu-id="735c2-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="735c2-116">Um objeto de agrupamento [**Msvm \_ managementcollection**](msvm-managementcollection.md) ou ' recipiente ' que representa a coleção.</span><span class="sxs-lookup"><span data-stu-id="735c2-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="735c2-117">**Membro**</span><span class="sxs-lookup"><span data-stu-id="735c2-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="735c2-118">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="735c2-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="735c2-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="735c2-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="735c2-120">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("membro")</span><span class="sxs-lookup"><span data-stu-id="735c2-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="735c2-121">Um [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) que contém os membros da coleção.</span><span class="sxs-lookup"><span data-stu-id="735c2-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="735c2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="735c2-122">Requirements</span></span>



| <span data-ttu-id="735c2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="735c2-123">Requirement</span></span> | <span data-ttu-id="735c2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="735c2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="735c2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="735c2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="735c2-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="735c2-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="735c2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="735c2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="735c2-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="735c2-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="735c2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="735c2-129">Namespace</span></span><br/>                | <span data-ttu-id="735c2-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="735c2-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="735c2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="735c2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="735c2-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="735c2-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="735c2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="735c2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="735c2-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="735c2-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="735c2-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="735c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735c2-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="735c2-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

