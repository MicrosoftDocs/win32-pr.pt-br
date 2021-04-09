---
description: A \_ classe de contêiner CIM representa uma associação entre um elemento físico contido e um que o contém. Um objeto recipiente deve ser um pacote físico.
ms.assetid: 9b119163-3c56-44e2-ba66-d8add3c375fa
ms.tgt_platform: multiple
title: Classe CIM_Container
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Container
- CIM_Container.PartComponent
- CIM_Container.GroupComponent
- CIM_Container.LocationWithinContainer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70aca54c80a954deed88d1ec740f0057753bf5e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920428"
---
# <a name="cim_container-class"></a><span data-ttu-id="0cb5d-104">\_Classe de contêiner CIM</span><span class="sxs-lookup"><span data-stu-id="0cb5d-104">CIM\_Container class</span></span>

<span data-ttu-id="0cb5d-105">A classe de **\_ contêiner CIM** representa uma associação entre um elemento físico contido e um que o contém.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-105">The **CIM\_Container** class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="0cb5d-106">Um objeto recipiente deve ser um pacote físico.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-106">A containing object must be a physical package.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0cb5d-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0cb5d-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0cb5d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0cb5d-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0cb5d-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb5d-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cb5d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Container : CIM_Component
{
  CIM_PhysicalElement REF PartComponent;
  CIM_PhysicalPackage REF GroupComponent;
  string                  LocationWithinContainer;
};
```

## <a name="members"></a><span data-ttu-id="0cb5d-112">Membros</span><span class="sxs-lookup"><span data-stu-id="0cb5d-112">Members</span></span>

<span data-ttu-id="0cb5d-113">A classe de **\_ contêiner CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0cb5d-113">The **CIM\_Container** class has these types of members:</span></span>

-   [<span data-ttu-id="0cb5d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0cb5d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cb5d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0cb5d-115">Properties</span></span>

<span data-ttu-id="0cb5d-116">A classe de **\_ contêiner CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-116">The **CIM\_Container** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cb5d-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb5d-118">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="0cb5d-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb5d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb5d-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0cb5d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0cb5d-121">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que representa o pacote físico que contém outros elementos físicos, incluindo outros pacotes.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that represents the physical package that contains other physical elements, including other packages.</span></span>

</dd> <dt>

<span data-ttu-id="0cb5d-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb5d-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cb5d-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb5d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0cb5d-125">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="0cb5d-126">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="0cb5d-127">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb5d-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="0cb5d-128">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-128">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cb5d-129">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-129">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="0cb5d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0cb5d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cb5d-131">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="0cb5d-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0cb5d-132">Um [**\_ físicoelement do CIM**](cim-physicalelement.md) que descreve o elemento físico que está contido no pacote.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-132">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0cb5d-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb5d-133">Remarks</span></span>

<span data-ttu-id="0cb5d-134">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-134">WMI does not implement this class.</span></span> <span data-ttu-id="0cb5d-135">Para obter mais informações sobre classes derivadas **do \_ contêiner CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0cb5d-135">For more information about classes derived from **CIM\_Container**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0cb5d-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0cb5d-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0cb5d-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb5d-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb5d-138">Requirements</span></span>



| <span data-ttu-id="0cb5d-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb5d-139">Requirement</span></span> | <span data-ttu-id="0cb5d-140">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb5d-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb5d-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb5d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb5d-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cb5d-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0cb5d-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb5d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb5d-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cb5d-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0cb5d-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cb5d-145">Namespace</span></span><br/>                | <span data-ttu-id="0cb5d-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0cb5d-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0cb5d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="0cb5d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cb5d-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cb5d-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cb5d-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0cb5d-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cb5d-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb5d-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cb5d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb5d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb5d-152">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="0cb5d-152">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

