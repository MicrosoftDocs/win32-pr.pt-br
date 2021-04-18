---
description: Associa uma instância de um recurso alocado com o pool de recursos do qual ele foi alocado.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Classe Msvm_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4d798c31fbcd8429007c53f3b156fc7c5922e7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810350"
---
# <a name="msvm_elementallocatedfrompool-class"></a><span data-ttu-id="b318a-103">\_Classe Msvm ElementAllocatedFromPool</span><span class="sxs-lookup"><span data-stu-id="b318a-103">Msvm\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="b318a-104">Associa uma instância de um recurso alocado com o pool de recursos do qual ele foi alocado.</span><span class="sxs-lookup"><span data-stu-id="b318a-104">Associates an instance of an allocated resource with the resource pool from which it was allocated.</span></span>

<span data-ttu-id="b318a-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b318a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b318a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b318a-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b318a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b318a-107">Members</span></span>

<span data-ttu-id="b318a-108">A classe **Msvm \_ ElementAllocatedFromPool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b318a-108">The **Msvm\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="b318a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b318a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b318a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b318a-110">Properties</span></span>

<span data-ttu-id="b318a-111">A classe **Msvm \_ ElementAllocatedFromPool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b318a-111">The **Msvm\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b318a-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b318a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b318a-113">Tipo de dados: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b318a-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="b318a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b318a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b318a-115">Qualificadores: **substituir**, **máximo** (1)</span><span class="sxs-lookup"><span data-stu-id="b318a-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b318a-116">O pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="b318a-116">The resource pool.</span></span> <span data-ttu-id="b318a-117">Essa propriedade é herdada do [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b318a-117">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b318a-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b318a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b318a-119">Tipo de dados: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span><span class="sxs-lookup"><span data-stu-id="b318a-119">Data type: **[**CIM\_LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**</span></span>
</dt> <dt>

<span data-ttu-id="b318a-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b318a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b318a-121">O recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="b318a-121">The allocated resource.</span></span> <span data-ttu-id="b318a-122">Essa propriedade é herdada do [**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b318a-122">This property is inherited from [**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b318a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b318a-123">Remarks</span></span>

<span data-ttu-id="b318a-124">O acesso à classe **Msvm \_ ElementAllocatedFromPool** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b318a-124">Access to the **Msvm\_ElementAllocatedFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b318a-125">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b318a-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b318a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b318a-126">Requirements</span></span>



| <span data-ttu-id="b318a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b318a-127">Requirement</span></span> | <span data-ttu-id="b318a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b318a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b318a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b318a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b318a-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b318a-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b318a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b318a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b318a-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b318a-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b318a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b318a-133">Namespace</span></span><br/>                | <span data-ttu-id="b318a-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b318a-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b318a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b318a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b318a-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b318a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b318a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b318a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b318a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b318a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b318a-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b318a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b318a-140">**\_ELEMENTALLOCATEDFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="b318a-140">**CIM\_ElementAllocatedFromPool**</span></span>](cim-elementallocatedfrompool.md)
</dt> <dt>

<span data-ttu-id="b318a-141">[**\_ELEMENTALLOCATEDFROMPOOL CIM**](/previous-versions//cc150668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b318a-141">[**CIM\_ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b318a-142">**Msvm \_ ElementAllocatedFromPool (v1)**</span><span class="sxs-lookup"><span data-stu-id="b318a-142">**Msvm\_ElementAllocatedFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[<span data-ttu-id="b318a-143">Classes de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="b318a-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

