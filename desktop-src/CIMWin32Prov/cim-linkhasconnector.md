---
description: A \_ classe CIM LinkHasConnector associa cabos e links usados como conectores físicos, que conectam os elementos físicos. Essa associação define explicitamente a relação de conectores para \_ PHYSICALLINK CIM.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: Classe CIM_LinkHasConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826449"
---
# <a name="cim_linkhasconnector-class"></a><span data-ttu-id="efb00-104">\_Classe CIM LinkHasConnector</span><span class="sxs-lookup"><span data-stu-id="efb00-104">CIM\_LinkHasConnector class</span></span>

<span data-ttu-id="efb00-105">A classe **CIM \_ LinkHasConnector** associa cabos e links usados como conectores físicos, que conectam os elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="efb00-105">The **CIM\_LinkHasConnector** class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="efb00-106">Essa associação define explicitamente a relação de conectores [**para \_ PhysicalLink CIM**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="efb00-106">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efb00-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="efb00-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="efb00-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="efb00-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="efb00-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="efb00-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="efb00-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="efb00-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb00-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efb00-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="efb00-112">Membros</span><span class="sxs-lookup"><span data-stu-id="efb00-112">Members</span></span>

<span data-ttu-id="efb00-113">A classe **CIM \_ LinkHasConnector** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="efb00-113">The **CIM\_LinkHasConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="efb00-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efb00-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efb00-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efb00-115">Properties</span></span>

<span data-ttu-id="efb00-116">A classe **CIM \_ LinkHasConnector** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="efb00-116">The **CIM\_LinkHasConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efb00-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="efb00-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb00-118">Tipo de dados: **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="efb00-118">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="efb00-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efb00-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efb00-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="efb00-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="efb00-121">Um [**\_ PhysicalLink CIM**](cim-physicallink.md) que descreve o link físico que tem um conector.</span><span class="sxs-lookup"><span data-stu-id="efb00-121">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="efb00-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="efb00-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efb00-123">Tipo de dados: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="efb00-123">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="efb00-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="efb00-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efb00-125">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="efb00-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="efb00-126">Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que descreve o conector físico.</span><span class="sxs-lookup"><span data-stu-id="efb00-126">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efb00-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="efb00-127">Remarks</span></span>

<span data-ttu-id="efb00-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="efb00-128">WMI does not implement this class.</span></span>

<span data-ttu-id="efb00-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="efb00-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="efb00-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="efb00-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb00-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb00-131">Requirements</span></span>



| <span data-ttu-id="efb00-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="efb00-132">Requirement</span></span> | <span data-ttu-id="efb00-133">Valor</span><span class="sxs-lookup"><span data-stu-id="efb00-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efb00-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efb00-134">Minimum supported client</span></span><br/> | <span data-ttu-id="efb00-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efb00-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="efb00-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="efb00-136">Minimum supported server</span></span><br/> | <span data-ttu-id="efb00-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efb00-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="efb00-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="efb00-138">Namespace</span></span><br/>                | <span data-ttu-id="efb00-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="efb00-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="efb00-140">MOF</span><span class="sxs-lookup"><span data-stu-id="efb00-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efb00-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efb00-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="efb00-142">DLL</span><span class="sxs-lookup"><span data-stu-id="efb00-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efb00-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efb00-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efb00-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="efb00-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb00-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="efb00-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

