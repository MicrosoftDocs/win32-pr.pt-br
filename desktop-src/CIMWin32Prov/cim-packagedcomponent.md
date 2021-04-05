---
description: A \_ associação CIM PackagedComponent representa uma relação explícita na qual um componente é normalmente contido por um pacote físico, como um chassi ou cartão.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: Classe CIM_PackagedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826204"
---
# <a name="cim_packagedcomponent-class"></a><span data-ttu-id="8ee59-103">\_Classe CIM PackagedComponent</span><span class="sxs-lookup"><span data-stu-id="8ee59-103">CIM\_PackagedComponent class</span></span>

<span data-ttu-id="8ee59-104">A associação **CIM \_ PackagedComponent** representa uma relação explícita na qual um componente é normalmente contido por um pacote físico, como um chassi ou cartão.</span><span class="sxs-lookup"><span data-stu-id="8ee59-104">The **CIM\_PackagedComponent** association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

<span data-ttu-id="8ee59-105">**Observação**  Um componente pode ser removido ou ainda não inserido no, seu pacote de contenção (ou seja, a propriedade booliana **removível** é **true**).</span><span class="sxs-lookup"><span data-stu-id="8ee59-105">**Note**  A component may be removed from, or not yet inserted into, its containing package (that is, the **Removable** Boolean property is **TRUE**).</span></span> <span data-ttu-id="8ee59-106">Portanto, um componente nem sempre pode ser associado a um contêiner.</span><span class="sxs-lookup"><span data-stu-id="8ee59-106">Therefore, a component may not always be associated with a container.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ee59-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8ee59-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8ee59-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8ee59-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8ee59-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8ee59-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8ee59-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8ee59-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee59-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ee59-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="8ee59-112">Membros</span><span class="sxs-lookup"><span data-stu-id="8ee59-112">Members</span></span>

<span data-ttu-id="8ee59-113">A classe **CIM \_ PackagedComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8ee59-113">The **CIM\_PackagedComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8ee59-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ee59-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ee59-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8ee59-115">Properties</span></span>

<span data-ttu-id="8ee59-116">A classe **CIM \_ PackagedComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8ee59-116">The **CIM\_PackagedComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ee59-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8ee59-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ee59-118">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="8ee59-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="8ee59-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ee59-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ee59-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8ee59-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8ee59-121">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico que contém componente (s).</span><span class="sxs-lookup"><span data-stu-id="8ee59-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that contains component(s).</span></span>

</dd> <dt>

<span data-ttu-id="8ee59-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="8ee59-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ee59-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8ee59-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ee59-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ee59-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ee59-125">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="8ee59-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="8ee59-126">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8ee59-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="8ee59-127">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee59-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="8ee59-128">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="8ee59-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ee59-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8ee59-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ee59-130">Tipo de dados: **CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="8ee59-130">Data type: **CIM\_PhysicalComponent**</span></span>
</dt> <dt>

<span data-ttu-id="8ee59-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8ee59-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ee59-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="8ee59-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="8ee59-133">Um [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md) que descreve o componente físico que está contido no pacote.</span><span class="sxs-lookup"><span data-stu-id="8ee59-133">A [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) describing the physical component which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ee59-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ee59-134">Remarks</span></span>

<span data-ttu-id="8ee59-135">A classe **CIM \_ PackagedComponent** é derivada do [**\_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="8ee59-135">The **CIM\_PackagedComponent** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="8ee59-136">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="8ee59-136">WMI does not implement this class.</span></span>

<span data-ttu-id="8ee59-137">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8ee59-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8ee59-138">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8ee59-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee59-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee59-139">Requirements</span></span>



| <span data-ttu-id="8ee59-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee59-140">Requirement</span></span> | <span data-ttu-id="8ee59-141">Valor</span><span class="sxs-lookup"><span data-stu-id="8ee59-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee59-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ee59-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee59-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ee59-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ee59-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ee59-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee59-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ee59-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ee59-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ee59-146">Namespace</span></span><br/>                | <span data-ttu-id="8ee59-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8ee59-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8ee59-148">MOF</span><span class="sxs-lookup"><span data-stu-id="8ee59-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ee59-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ee59-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ee59-150">DLL</span><span class="sxs-lookup"><span data-stu-id="8ee59-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ee59-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee59-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee59-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ee59-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee59-153">**\_Contêiner CIM**</span><span class="sxs-lookup"><span data-stu-id="8ee59-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

