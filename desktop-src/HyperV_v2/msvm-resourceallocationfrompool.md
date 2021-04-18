---
description: Associa uma instância de uma alocação de recursos ao pool de recursos do qual ele está alocado.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Classe Msvm_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785449"
---
# <a name="msvm_resourceallocationfrompool-class"></a><span data-ttu-id="9d863-103">\_Classe Msvm ResourceAllocationFromPool</span><span class="sxs-lookup"><span data-stu-id="9d863-103">Msvm\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="9d863-104">Associa uma instância de uma alocação de recursos ao pool de recursos do qual ele está alocado.</span><span class="sxs-lookup"><span data-stu-id="9d863-104">Associates an instance of a resource allocation with the resource pool from which it is allocated.</span></span>

<span data-ttu-id="9d863-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9d863-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d863-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d863-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9d863-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9d863-107">Members</span></span>

<span data-ttu-id="9d863-108">A classe **Msvm \_ ResourceAllocationFromPool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9d863-108">The **Msvm\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="9d863-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d863-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d863-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d863-110">Properties</span></span>

<span data-ttu-id="9d863-111">A classe **Msvm \_ ResourceAllocationFromPool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9d863-111">The **Msvm\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d863-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="9d863-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d863-113">Tipo de dados: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9d863-113">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="9d863-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d863-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d863-115">Qualificadores: **substituir**, **máximo** (1)</span><span class="sxs-lookup"><span data-stu-id="9d863-115">Qualifiers: **Override**, **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="9d863-116">O pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d863-116">The resource pool.</span></span> <span data-ttu-id="9d863-117">Essa propriedade é herdada do [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d863-117">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d863-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="9d863-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d863-119">Tipo de dados: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="9d863-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="9d863-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d863-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d863-121">A alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="9d863-121">The resource allocation.</span></span> <span data-ttu-id="9d863-122">Essa propriedade é herdada do [**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d863-122">This property is inherited from [**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d863-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d863-123">Remarks</span></span>

<span data-ttu-id="9d863-124">O acesso à classe **Msvm \_ ResourceAllocationFromPool** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="9d863-124">Access to the **Msvm\_ResourceAllocationFromPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9d863-125">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9d863-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d863-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d863-126">Requirements</span></span>



| <span data-ttu-id="9d863-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d863-127">Requirement</span></span> | <span data-ttu-id="9d863-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9d863-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d863-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d863-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9d863-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d863-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d863-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d863-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9d863-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d863-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d863-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d863-133">Namespace</span></span><br/>                | <span data-ttu-id="9d863-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9d863-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d863-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9d863-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d863-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d863-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d863-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9d863-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d863-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d863-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d863-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d863-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d863-140">**\_RESOURCEALLOCATIONFROMPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="9d863-140">**CIM\_ResourceAllocationFromPool**</span></span>](cim-resourceallocationfrompool.md)
</dt> <dt>

<span data-ttu-id="9d863-141">[**\_RESOURCEALLOCATIONFROMPOOL CIM**](/previous-versions//cc150673(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9d863-141">[**CIM\_ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9d863-142">**Msvm \_ ResourceAllocationFromPool (v1)**</span><span class="sxs-lookup"><span data-stu-id="9d863-142">**Msvm\_ResourceAllocationFromPool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[<span data-ttu-id="9d863-143">Classes de gerenciamento de recursos</span><span class="sxs-lookup"><span data-stu-id="9d863-143">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

