---
description: A \_ associação CIM ChassisInRack representa o &\# 0034; que contém&\# 0034; relação entre um rack e um chassi que ele contém.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: Classe CIM_ChassisInRack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089353"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="0b51e-103">\_Classe CIM ChassisInRack</span><span class="sxs-lookup"><span data-stu-id="0b51e-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="0b51e-104">A associação de **\_ ChassisInRack do CIM** representa a relação de "contenção" entre um rack e um chassi que ele contém.</span><span class="sxs-lookup"><span data-stu-id="0b51e-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b51e-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0b51e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b51e-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b51e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b51e-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0b51e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0b51e-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0b51e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b51e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b51e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="0b51e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0b51e-110">Members</span></span>

<span data-ttu-id="0b51e-111">A classe **CIM \_ ChassisInRack** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b51e-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="0b51e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b51e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b51e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b51e-113">Properties</span></span>

<span data-ttu-id="0b51e-114">A classe **CIM \_ ChassisInRack** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b51e-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b51e-115">**Inferior**</span><span class="sxs-lookup"><span data-stu-id="0b51e-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b51e-116">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b51e-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b51e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-118">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="0b51e-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="0b51e-119">Inteiro que indica o "U" mais baixo ou inferior no qual o chassi está montado.</span><span class="sxs-lookup"><span data-stu-id="0b51e-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="0b51e-120">Um "U" é uma unidade de medida padrão para a altura de um rack, ou componente montável em rack, e é igual a 1,75 polegadas ou 4,445 centímetros.</span><span class="sxs-lookup"><span data-stu-id="0b51e-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="0b51e-121">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0b51e-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b51e-122">Tipo de dados **: \_ rack CIM**</span><span class="sxs-lookup"><span data-stu-id="0b51e-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b51e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0b51e-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0b51e-125">Um [**\_ rack CIM**](cim-rack.md) que descreve o rack que contém o chassi.</span><span class="sxs-lookup"><span data-stu-id="0b51e-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="0b51e-126">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="0b51e-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b51e-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b51e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b51e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b51e-129">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="0b51e-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="0b51e-130">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="0b51e-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="0b51e-131">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="0b51e-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="0b51e-132">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="0b51e-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b51e-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0b51e-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b51e-134">Tipo de dados **: \_ chassi CIM**</span><span class="sxs-lookup"><span data-stu-id="0b51e-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b51e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b51e-136">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="0b51e-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0b51e-137">Um [**\_ chassi CIM**](cim-chassis.md) que descreve o chassi que está montado no rack.</span><span class="sxs-lookup"><span data-stu-id="0b51e-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b51e-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b51e-138">Remarks</span></span>

<span data-ttu-id="0b51e-139">A classe **CIM \_ ChassisInRack** é derivada do [**\_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="0b51e-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="0b51e-140">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0b51e-140">WMI does not implement this class.</span></span>

<span data-ttu-id="0b51e-141">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b51e-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b51e-142">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0b51e-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b51e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b51e-143">Requirements</span></span>



| <span data-ttu-id="0b51e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b51e-144">Requirement</span></span> | <span data-ttu-id="0b51e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="0b51e-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b51e-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b51e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0b51e-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b51e-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b51e-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b51e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0b51e-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b51e-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b51e-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b51e-150">Namespace</span></span><br/>                | <span data-ttu-id="0b51e-151">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0b51e-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b51e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="0b51e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b51e-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b51e-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b51e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="0b51e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b51e-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b51e-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b51e-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b51e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b51e-157">**\_Contêiner CIM**</span><span class="sxs-lookup"><span data-stu-id="0b51e-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

