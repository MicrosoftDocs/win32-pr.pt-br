---
description: Representa uma coleção de instantâneos do sistema virtual.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Classe Msvm_SnapshotCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091143"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="5fc02-103">\_Classe Msvm snapshotcollection</span><span class="sxs-lookup"><span data-stu-id="5fc02-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="5fc02-104">Representa uma coleção de instantâneos do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5fc02-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="5fc02-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5fc02-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc02-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fc02-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="5fc02-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5fc02-107">Members</span></span>

<span data-ttu-id="5fc02-108">A classe **Msvm \_ snapshotcollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5fc02-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="5fc02-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5fc02-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fc02-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5fc02-110">Properties</span></span>

<span data-ttu-id="5fc02-111">A classe **Msvm \_ snapshotcollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5fc02-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fc02-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="5fc02-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc02-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc02-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc02-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc02-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc02-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5fc02-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5fc02-116">A identificação exclusiva do objeto de coleção.</span><span class="sxs-lookup"><span data-stu-id="5fc02-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="5fc02-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5fc02-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc02-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc02-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc02-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc02-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc02-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="5fc02-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="5fc02-121">Um nome definido pelo usuário para a coleção.</span><span class="sxs-lookup"><span data-stu-id="5fc02-121">An user-defined name for the collection.</span></span> <span data-ttu-id="5fc02-122">Observe que isso não é garantido como exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5fc02-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fc02-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc02-123">Requirements</span></span>



| <span data-ttu-id="5fc02-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc02-124">Requirement</span></span> | <span data-ttu-id="5fc02-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5fc02-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc02-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc02-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc02-127">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5fc02-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5fc02-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc02-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc02-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5fc02-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5fc02-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fc02-130">Namespace</span></span><br/>                | <span data-ttu-id="5fc02-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5fc02-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5fc02-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5fc02-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fc02-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fc02-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fc02-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5fc02-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fc02-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fc02-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fc02-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc02-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc02-137">**\_Coleção CIM**</span><span class="sxs-lookup"><span data-stu-id="5fc02-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

