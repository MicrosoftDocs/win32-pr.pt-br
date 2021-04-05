---
description: A \_ classe CIM ConnectorOnPackage representa uma associação que torna explícita a relação de confinamento entre conectores e pacotes. Os pacotes físicos contêm conectores e outros elementos físicos.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: Classe CIM_ConnectorOnPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826496"
---
# <a name="cim_connectoronpackage-class"></a><span data-ttu-id="ab2dc-104">\_Classe CIM ConnectorOnPackage</span><span class="sxs-lookup"><span data-stu-id="ab2dc-104">CIM\_ConnectorOnPackage class</span></span>

<span data-ttu-id="ab2dc-105">A classe **CIM \_ ConnectorOnPackage** representa uma associação que torna explícita a relação de confinamento entre conectores e pacotes.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-105">The **CIM\_ConnectorOnPackage** class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="ab2dc-106">Os pacotes físicos contêm conectores e outros elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-106">Physical packages contain connectors as well as other physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab2dc-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ab2dc-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ab2dc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ab2dc-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ab2dc-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2dc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab2dc-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="ab2dc-112">Membros</span><span class="sxs-lookup"><span data-stu-id="ab2dc-112">Members</span></span>

<span data-ttu-id="ab2dc-113">A classe **CIM \_ ConnectorOnPackage** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab2dc-113">The **CIM\_ConnectorOnPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="ab2dc-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab2dc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab2dc-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab2dc-115">Properties</span></span>

<span data-ttu-id="ab2dc-116">A classe **CIM \_ ConnectorOnPackage** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-116">The **CIM\_ConnectorOnPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab2dc-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab2dc-118">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="ab2dc-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab2dc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab2dc-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ab2dc-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ab2dc-121">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico que tem um conector.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="ab2dc-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab2dc-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab2dc-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab2dc-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ab2dc-125">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="ab2dc-126">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="ab2dc-127">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2dc-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="ab2dc-128">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="ab2dc-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab2dc-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab2dc-130">Tipo de dados: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-130">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="ab2dc-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab2dc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab2dc-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="ab2dc-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ab2dc-133">Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que descreve o conector físico.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-133">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab2dc-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab2dc-134">Remarks</span></span>

<span data-ttu-id="ab2dc-135">A classe **CIM \_ ConnectorOnPackage** é derivada do [**\_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="ab2dc-135">The **CIM\_ConnectorOnPackage** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="ab2dc-136">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-136">WMI does not implement this class.</span></span>

<span data-ttu-id="ab2dc-137">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ab2dc-138">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2dc-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab2dc-139">Requirements</span></span>



| <span data-ttu-id="ab2dc-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab2dc-140">Requirement</span></span> | <span data-ttu-id="ab2dc-141">Valor</span><span class="sxs-lookup"><span data-stu-id="ab2dc-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2dc-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab2dc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2dc-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab2dc-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab2dc-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab2dc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2dc-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab2dc-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab2dc-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab2dc-146">Namespace</span></span><br/>                | <span data-ttu-id="ab2dc-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ab2dc-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab2dc-148">MOF</span><span class="sxs-lookup"><span data-stu-id="ab2dc-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab2dc-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab2dc-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab2dc-150">DLL</span><span class="sxs-lookup"><span data-stu-id="ab2dc-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab2dc-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab2dc-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2dc-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab2dc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2dc-153">**\_Contêiner CIM**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

