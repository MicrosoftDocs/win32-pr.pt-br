---
description: Associa o Msvm \_ snapshotcollection aos objetos VirtualSystemCollection do Msvm correspondentes \_ .
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Classe Msvm_SnapshotOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827610"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="ee270-103">\_Classe Msvm SnapshotOfVirtualSystemCollection</span><span class="sxs-lookup"><span data-stu-id="ee270-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="ee270-104">Associa o [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) aos objetos [**\_ VirtualSystemCollection do Msvm**](msvm-virtualsystemcollection.md) correspondentes.</span><span class="sxs-lookup"><span data-stu-id="ee270-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="ee270-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ee270-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee270-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee270-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ee270-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ee270-107">Members</span></span>

<span data-ttu-id="ee270-108">A classe **Msvm \_ SnapshotOfVirtualSystemCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ee270-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="ee270-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ee270-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee270-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ee270-110">Properties</span></span>

<span data-ttu-id="ee270-111">A classe **Msvm \_ SnapshotOfVirtualSystemCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ee270-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ee270-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="ee270-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee270-113">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="ee270-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="ee270-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ee270-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee270-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")</span><span class="sxs-lookup"><span data-stu-id="ee270-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ee270-116">Um [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) que representa o objeto independente nessa associação.</span><span class="sxs-lookup"><span data-stu-id="ee270-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="ee270-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="ee270-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ee270-118">Tipo de dados **: \_ coleção CIM**</span><span class="sxs-lookup"><span data-stu-id="ee270-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="ee270-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ee270-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ee270-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="ee270-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ee270-121">Uma [**\_ coleção CIM**](cim-collection.md) que representa o objeto que é dependente do **Antecedent.**</span><span class="sxs-lookup"><span data-stu-id="ee270-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee270-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee270-122">Requirements</span></span>



| <span data-ttu-id="ee270-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee270-123">Requirement</span></span> | <span data-ttu-id="ee270-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ee270-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee270-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee270-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ee270-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ee270-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ee270-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee270-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ee270-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ee270-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ee270-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee270-129">Namespace</span></span><br/>                | <span data-ttu-id="ee270-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="ee270-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ee270-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ee270-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee270-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee270-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee270-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ee270-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee270-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ee270-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ee270-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee270-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee270-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="ee270-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

