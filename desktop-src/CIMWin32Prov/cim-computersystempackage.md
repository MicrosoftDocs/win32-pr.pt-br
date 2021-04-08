---
description: A \_ classe CIM ComputerSystemPackage representa uma associação que define explicitamente a relação entre os sistemas de computador unitários e um ou mais pacotes físicos.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920430"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="409ff-103">\_Classe CIM ComputerSystemPackage</span><span class="sxs-lookup"><span data-stu-id="409ff-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="409ff-104">A classe **CIM \_ ComputerSystemPackage** representa uma associação que define explicitamente a relação entre os sistemas de computador unitários e um ou mais pacotes físicos.</span><span class="sxs-lookup"><span data-stu-id="409ff-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="409ff-105">A associação é semelhante à forma como os dispositivos lógicos são concretizados por elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="409ff-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="409ff-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="409ff-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="409ff-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="409ff-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="409ff-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="409ff-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="409ff-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="409ff-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="409ff-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="409ff-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="409ff-111">Membros</span><span class="sxs-lookup"><span data-stu-id="409ff-111">Members</span></span>

<span data-ttu-id="409ff-112">A classe **CIM \_ ComputerSystemPackage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="409ff-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="409ff-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="409ff-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="409ff-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="409ff-114">Properties</span></span>

<span data-ttu-id="409ff-115">A classe **CIM \_ ComputerSystemPackage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="409ff-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="409ff-116">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="409ff-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409ff-117">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="409ff-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="409ff-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="409ff-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="409ff-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="409ff-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="409ff-120">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve os pacotes físicos que percebem um sistema de computador unitário.</span><span class="sxs-lookup"><span data-stu-id="409ff-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="409ff-121">**Depende**</span><span class="sxs-lookup"><span data-stu-id="409ff-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409ff-122">Tipo de dados: **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="409ff-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="409ff-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="409ff-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="409ff-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="409ff-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="409ff-125">Um [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) que descreve o sistema de computador unitário.</span><span class="sxs-lookup"><span data-stu-id="409ff-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="409ff-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="409ff-126">Remarks</span></span>

<span data-ttu-id="409ff-127">A classe **CIM \_ ComputerSystemPackage** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="409ff-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="409ff-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="409ff-128">WMI does not implement this class.</span></span>

<span data-ttu-id="409ff-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="409ff-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="409ff-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="409ff-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="409ff-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="409ff-131">Requirements</span></span>



| <span data-ttu-id="409ff-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="409ff-132">Requirement</span></span> | <span data-ttu-id="409ff-133">Valor</span><span class="sxs-lookup"><span data-stu-id="409ff-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="409ff-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="409ff-134">Minimum supported client</span></span><br/> | <span data-ttu-id="409ff-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="409ff-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="409ff-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="409ff-136">Minimum supported server</span></span><br/> | <span data-ttu-id="409ff-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="409ff-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="409ff-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="409ff-138">Namespace</span></span><br/>                | <span data-ttu-id="409ff-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="409ff-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="409ff-140">MOF</span><span class="sxs-lookup"><span data-stu-id="409ff-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="409ff-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="409ff-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="409ff-142">DLL</span><span class="sxs-lookup"><span data-stu-id="409ff-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="409ff-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="409ff-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="409ff-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="409ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="409ff-145">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="409ff-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

