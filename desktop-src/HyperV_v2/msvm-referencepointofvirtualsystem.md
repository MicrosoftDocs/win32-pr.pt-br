---
description: Associa o Msvm \_ VirtualSystemReferencePoint aos \_ objetos Msvm VirtualSystem correspondentes.
ms.assetid: 5a9cb099-c0ae-4088-a64c-f2720a6cb9c8
title: Classe Msvm_ReferencePointOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystem
- Msvm_ReferencePointOfVirtualSystem.Antecedent
- Msvm_ReferencePointOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debe1931154c5c7a7868e8ee301daf977076b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662287"
---
# <a name="msvm_referencepointofvirtualsystem-class"></a><span data-ttu-id="f3639-103">\_Classe Msvm ReferencePointOfVirtualSystem</span><span class="sxs-lookup"><span data-stu-id="f3639-103">Msvm\_ReferencePointOfVirtualSystem class</span></span>

<span data-ttu-id="f3639-104">Associa o [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) aos objetos [**Msvm \_ VirtualSystem**](msvm-virtualsystemresourcecomponent.md) correspondentes.</span><span class="sxs-lookup"><span data-stu-id="f3639-104">Associates the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) to the corresponding [**Msvm\_VirtualSystem**](msvm-virtualsystemresourcecomponent.md) objects.</span></span>

<span data-ttu-id="f3639-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f3639-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3639-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3639-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystem : CIM_Dependency
{
  Msvm_ComputerSystem              REF Antecedent;
  Msvm_VirtualSystemReferencePoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f3639-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f3639-107">Members</span></span>

<span data-ttu-id="f3639-108">A classe **Msvm \_ ReferencePointOfVirtualSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f3639-108">The **Msvm\_ReferencePointOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="f3639-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3639-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3639-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3639-110">Properties</span></span>

<span data-ttu-id="f3639-111">A classe **Msvm \_ ReferencePointOfVirtualSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f3639-111">The **Msvm\_ReferencePointOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3639-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f3639-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3639-113">Tipo de dados: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f3639-113">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f3639-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3639-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3639-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")</span><span class="sxs-lookup"><span data-stu-id="f3639-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f3639-116">Um [**\_ ComputerSystem Msvm**](msvm-computersystem.md) que representa o objeto independente nessa associação.</span><span class="sxs-lookup"><span data-stu-id="f3639-116">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="f3639-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f3639-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3639-118">Tipo de dados: **Msvm \_ VirtualSystemReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="f3639-118">Data type: **Msvm\_VirtualSystemReferencePoint**</span></span>
</dt> <dt>

<span data-ttu-id="f3639-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3639-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3639-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="f3639-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f3639-121">Um [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa o objeto que é dependente do **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="f3639-121">An [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3639-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3639-122">Requirements</span></span>



| <span data-ttu-id="f3639-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3639-123">Requirement</span></span> | <span data-ttu-id="f3639-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f3639-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3639-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3639-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3639-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f3639-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f3639-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3639-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3639-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3639-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f3639-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3639-129">Namespace</span></span><br/>                | <span data-ttu-id="f3639-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f3639-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f3639-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f3639-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3639-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3639-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f3639-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3639-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3639-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f3639-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3639-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3639-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="f3639-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

