---
description: A \_ classe CIM ComputerSystemIRQ representa uma associação entre um sistema de computador e suas IRQs (linhas de solicitação de interrupção) disponíveis.
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemIRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753994"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="86f81-103">\_Classe CIM ComputerSystemIRQ</span><span class="sxs-lookup"><span data-stu-id="86f81-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="86f81-104">A classe **CIM \_ ComputerSystemIRQ** representa uma associação entre um sistema de computador e suas IRQs (linhas de solicitação de interrupção) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="86f81-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86f81-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="86f81-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="86f81-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="86f81-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="86f81-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="86f81-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="86f81-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="86f81-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f81-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86f81-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="86f81-110">Membros</span><span class="sxs-lookup"><span data-stu-id="86f81-110">Members</span></span>

<span data-ttu-id="86f81-111">A classe **CIM \_ ComputerSystemIRQ** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="86f81-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="86f81-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="86f81-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86f81-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="86f81-113">Properties</span></span>

<span data-ttu-id="86f81-114">A classe **CIM \_ ComputerSystemIRQ** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="86f81-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86f81-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="86f81-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86f81-116">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="86f81-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="86f81-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86f81-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86f81-118">Qualificadores: [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="86f81-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="86f81-119">Um [**\_ sistema**](cim-computersystem.md) de computadores CIM que descreve o computador associado ao IRQ.</span><span class="sxs-lookup"><span data-stu-id="86f81-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="86f81-120">Esta propriedade é herdada do [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="86f81-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="86f81-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="86f81-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86f81-122">Tipo de dados **: \_ IRQ de CIM**</span><span class="sxs-lookup"><span data-stu-id="86f81-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="86f81-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86f81-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86f81-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="86f81-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="86f81-125">Um [**\_ IRQ de CIM**](cim-irq.md) que descreve um IRQ do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="86f81-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86f81-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="86f81-126">Remarks</span></span>

<span data-ttu-id="86f81-127">A classe **CIM \_ ComputerSystemIRQ** é derivada de [**\_ ComputerSystemResource CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="86f81-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="86f81-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="86f81-128">WMI does not implement this class.</span></span>

<span data-ttu-id="86f81-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="86f81-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="86f81-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="86f81-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="86f81-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86f81-131">Requirements</span></span>



| <span data-ttu-id="86f81-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="86f81-132">Requirement</span></span> | <span data-ttu-id="86f81-133">Valor</span><span class="sxs-lookup"><span data-stu-id="86f81-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86f81-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86f81-134">Minimum supported client</span></span><br/> | <span data-ttu-id="86f81-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86f81-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86f81-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86f81-136">Minimum supported server</span></span><br/> | <span data-ttu-id="86f81-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86f81-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86f81-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="86f81-138">Namespace</span></span><br/>                | <span data-ttu-id="86f81-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="86f81-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86f81-140">MOF</span><span class="sxs-lookup"><span data-stu-id="86f81-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86f81-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86f81-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86f81-142">DLL</span><span class="sxs-lookup"><span data-stu-id="86f81-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86f81-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86f81-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f81-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="86f81-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f81-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="86f81-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

