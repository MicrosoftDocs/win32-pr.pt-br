---
description: Associa o Msvm \_ ReferencePointCollection aos \_ objetos Msvm VirtualSystemCollection correspondentes.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Classe Msvm_ReferencePointOfVirtualSystemCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747799"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a><span data-ttu-id="795e4-103">\_Classe Msvm ReferencePointOfVirtualSystemCollection</span><span class="sxs-lookup"><span data-stu-id="795e4-103">Msvm\_ReferencePointOfVirtualSystemCollection class</span></span>

<span data-ttu-id="795e4-104">Associa o [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) aos objetos [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) correspondentes.</span><span class="sxs-lookup"><span data-stu-id="795e4-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="795e4-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="795e4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="795e4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="795e4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="795e4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="795e4-107">Members</span></span>

<span data-ttu-id="795e4-108">A classe **Msvm \_ ReferencePointOfVirtualSystemCollection** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="795e4-108">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="795e4-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="795e4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="795e4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="795e4-110">Properties</span></span>

<span data-ttu-id="795e4-111">A classe **Msvm \_ ReferencePointOfVirtualSystemCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="795e4-111">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="795e4-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="795e4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-113">Tipo de dados: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="795e4-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="795e4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")</span><span class="sxs-lookup"><span data-stu-id="795e4-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-116">Um [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) que representa o objeto independente nessa associação.</span><span class="sxs-lookup"><span data-stu-id="795e4-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="795e4-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="795e4-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="795e4-118">Tipo de dados **: \_ coleção CIM**</span><span class="sxs-lookup"><span data-stu-id="795e4-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="795e4-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="795e4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="795e4-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="795e4-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="795e4-121">Uma [**\_ coleção CIM**](cim-collection.md) que representa o objeto que é dependente do **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="795e4-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="795e4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="795e4-122">Requirements</span></span>



| <span data-ttu-id="795e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="795e4-123">Requirement</span></span> | <span data-ttu-id="795e4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="795e4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="795e4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="795e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="795e4-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="795e4-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="795e4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="795e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="795e4-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="795e4-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="795e4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="795e4-129">Namespace</span></span><br/>                | <span data-ttu-id="795e4-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="795e4-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="795e4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="795e4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="795e4-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="795e4-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="795e4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="795e4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="795e4-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="795e4-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="795e4-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="795e4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795e4-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="795e4-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

