---
description: Associa uma instância de um recurso alocado com o nó NUMA físico do qual ele foi alocado.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Classe Msvm_ElementAllocatedFromNumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829033"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a><span data-ttu-id="35970-103">\_Classe Msvm ElementAllocatedFromNumaNode</span><span class="sxs-lookup"><span data-stu-id="35970-103">Msvm\_ElementAllocatedFromNumaNode class</span></span>

<span data-ttu-id="35970-104">Associa uma instância de um recurso alocado com o nó NUMA físico do qual ele foi alocado.</span><span class="sxs-lookup"><span data-stu-id="35970-104">Associates an instance of an allocated resource with the physical NUMA node from which it was allocated.</span></span>

<span data-ttu-id="35970-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="35970-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35970-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35970-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="35970-107">Membros</span><span class="sxs-lookup"><span data-stu-id="35970-107">Members</span></span>

<span data-ttu-id="35970-108">A classe **Msvm \_ ElementAllocatedFromNumaNode** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="35970-108">The **Msvm\_ElementAllocatedFromNumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="35970-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35970-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35970-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="35970-110">Properties</span></span>

<span data-ttu-id="35970-111">A classe **Msvm \_ ElementAllocatedFromNumaNode** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="35970-111">The **Msvm\_ElementAllocatedFromNumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35970-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="35970-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35970-113">Tipo de dados: **[ **Msvm \_ NumaNode**](msvm-numanode.md)**</span><span class="sxs-lookup"><span data-stu-id="35970-113">Data type: **[**Msvm\_NumaNode**](msvm-numanode.md)**</span></span>
</dt> <dt>

<span data-ttu-id="35970-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35970-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35970-115">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="35970-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="35970-116">O nó físico NUMA.</span><span class="sxs-lookup"><span data-stu-id="35970-116">The physical NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="35970-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="35970-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35970-118">Tipo de dados: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="35970-118">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="35970-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="35970-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35970-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="35970-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="35970-121">O recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="35970-121">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35970-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35970-122">Requirements</span></span>



| <span data-ttu-id="35970-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="35970-123">Requirement</span></span> | <span data-ttu-id="35970-124">Valor</span><span class="sxs-lookup"><span data-stu-id="35970-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35970-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35970-125">Minimum supported client</span></span><br/> | <span data-ttu-id="35970-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="35970-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="35970-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35970-127">Minimum supported server</span></span><br/> | <span data-ttu-id="35970-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="35970-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35970-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="35970-129">Namespace</span></span><br/>                | <span data-ttu-id="35970-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="35970-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35970-131">MOF</span><span class="sxs-lookup"><span data-stu-id="35970-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35970-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35970-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35970-133">DLL</span><span class="sxs-lookup"><span data-stu-id="35970-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35970-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35970-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

