---
description: A \_ associação CIM PackageInChassis representa a relação na qual um chassi pode conter outros pacotes, como outros chassis e cartões.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: Classe CIM_PackageInChassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457034"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="dee0b-103">\_Classe CIM PackageInChassis</span><span class="sxs-lookup"><span data-stu-id="dee0b-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="dee0b-104">A associação **CIM \_ PackageInChassis** representa a relação na qual um chassi pode conter outros pacotes, como outros chassis e cartões.</span><span class="sxs-lookup"><span data-stu-id="dee0b-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dee0b-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="dee0b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dee0b-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dee0b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dee0b-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="dee0b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dee0b-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="dee0b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee0b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dee0b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="dee0b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="dee0b-110">Members</span></span>

<span data-ttu-id="dee0b-111">A classe **CIM \_ PackageInChassis** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dee0b-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="dee0b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dee0b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dee0b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="dee0b-113">Properties</span></span>

<span data-ttu-id="dee0b-114">A classe **CIM \_ PackageInChassis** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="dee0b-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dee0b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dee0b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee0b-116">Tipo de dados **: \_ chassi CIM**</span><span class="sxs-lookup"><span data-stu-id="dee0b-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="dee0b-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dee0b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee0b-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dee0b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dee0b-119">Um [**\_ chassi CIM**](cim-chassis.md) que descreve o chassi que contém outros pacotes físicos.</span><span class="sxs-lookup"><span data-stu-id="dee0b-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="dee0b-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="dee0b-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee0b-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dee0b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee0b-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dee0b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee0b-123">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="dee0b-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="dee0b-124">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="dee0b-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="dee0b-125">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="dee0b-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="dee0b-126">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="dee0b-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee0b-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dee0b-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee0b-128">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="dee0b-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="dee0b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="dee0b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee0b-130">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="dee0b-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="dee0b-131">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote físico que está contido no chassi.</span><span class="sxs-lookup"><span data-stu-id="dee0b-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dee0b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="dee0b-132">Remarks</span></span>

<span data-ttu-id="dee0b-133">A classe **CIM \_ PackageInChassis** é derivada do [**\_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="dee0b-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="dee0b-134">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="dee0b-134">WMI does not implement this class.</span></span>

<span data-ttu-id="dee0b-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="dee0b-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dee0b-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="dee0b-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee0b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee0b-137">Requirements</span></span>



| <span data-ttu-id="dee0b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee0b-138">Requirement</span></span> | <span data-ttu-id="dee0b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="dee0b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee0b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee0b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="dee0b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dee0b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dee0b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee0b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="dee0b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dee0b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dee0b-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="dee0b-144">Namespace</span></span><br/>                | <span data-ttu-id="dee0b-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dee0b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dee0b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="dee0b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dee0b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dee0b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dee0b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="dee0b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee0b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee0b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee0b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="dee0b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee0b-151">**\_Contêiner CIM**</span><span class="sxs-lookup"><span data-stu-id="dee0b-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

