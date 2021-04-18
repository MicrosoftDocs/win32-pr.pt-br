---
description: O CIM \_ percebe que a classe representa a associação que define o mapeamento entre um dispositivo lógico e o componente físico que implementa o dispositivo.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: Classe CIM_Realizes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756441"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="0b016-103">O CIM \_ percebe a classe</span><span class="sxs-lookup"><span data-stu-id="0b016-103">CIM\_Realizes class</span></span>

<span data-ttu-id="0b016-104">O **CIM \_ percebe** que a classe representa a associação que define o mapeamento entre um dispositivo lógico e o componente físico que implementa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b016-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b016-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0b016-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b016-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b016-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b016-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b016-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0b016-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0b016-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b016-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b016-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0b016-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0b016-110">Members</span></span>

<span data-ttu-id="0b016-111">A classe de **\_ concretizações do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b016-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="0b016-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b016-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b016-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b016-113">Properties</span></span>

<span data-ttu-id="0b016-114">A classe de **\_ concretizações do CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b016-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b016-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="0b016-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b016-116">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="0b016-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="0b016-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b016-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b016-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0b016-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0b016-119">Um [**\_ físicoelement do CIM**](cim-physicalelement.md) que descreve o componente físico que implementa o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0b016-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="0b016-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="0b016-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b016-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="0b016-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="0b016-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b016-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b016-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="0b016-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0b016-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0b016-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b016-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b016-125">Remarks</span></span>

<span data-ttu-id="0b016-126">O **CIM \_ percebe** que a classe é derivada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0b016-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0b016-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0b016-127">WMI does not implement this class.</span></span>

<span data-ttu-id="0b016-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b016-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b016-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0b016-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b016-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b016-130">Requirements</span></span>



| <span data-ttu-id="0b016-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b016-131">Requirement</span></span> | <span data-ttu-id="0b016-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0b016-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b016-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b016-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0b016-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b016-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b016-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b016-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0b016-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b016-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b016-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b016-137">Namespace</span></span><br/>                | <span data-ttu-id="0b016-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0b016-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b016-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0b016-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b016-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b016-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b016-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0b016-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b016-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b016-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b016-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b016-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b016-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="0b016-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

