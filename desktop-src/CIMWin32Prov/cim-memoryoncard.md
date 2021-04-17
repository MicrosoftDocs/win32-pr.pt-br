---
description: A \_ classe CIM MemoryOnCard associa a memória física localizada em placas de hospedagem, placas de adaptador e assim por diante. Essa associação define explicitamente a relação de memória para os cartões.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: Classe CIM_MemoryOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755673"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="bf6ed-104">\_Classe CIM MemoryOnCard</span><span class="sxs-lookup"><span data-stu-id="bf6ed-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="bf6ed-105">A classe **CIM \_ MemoryOnCard** associa a memória física localizada em placas de hospedagem, placas de adaptador e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="bf6ed-106">Essa associação define explicitamente a relação de memória para os cartões.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf6ed-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bf6ed-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bf6ed-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bf6ed-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bf6ed-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf6ed-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf6ed-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="bf6ed-112">Membros</span><span class="sxs-lookup"><span data-stu-id="bf6ed-112">Members</span></span>

<span data-ttu-id="bf6ed-113">A classe **CIM \_ MemoryOnCard** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bf6ed-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="bf6ed-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf6ed-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf6ed-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bf6ed-115">Properties</span></span>

<span data-ttu-id="bf6ed-116">A classe **CIM \_ MemoryOnCard** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf6ed-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf6ed-118">Tipo de dados **: \_ placa CIM**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="bf6ed-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf6ed-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf6ed-120">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="bf6ed-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bf6ed-121">Um [**\_ cartão CIM**](cim-card.md) que descreve o cartão que inclui ou ' contém ' memória.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="bf6ed-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf6ed-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf6ed-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf6ed-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf6ed-125">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="bf6ed-126">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="bf6ed-127">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="bf6ed-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="bf6ed-128">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="bf6ed-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf6ed-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf6ed-130">Tipo de dados: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="bf6ed-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bf6ed-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf6ed-132">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="bf6ed-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="bf6ed-133">Um [**\_ PhysicalMemory CIM**](cim-physicalmemory.md) que descreve a memória física que está localizada no cartão.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf6ed-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf6ed-134">Remarks</span></span>

<span data-ttu-id="bf6ed-135">A classe **CIM \_ MemoryOnCard** é derivada de [**\_ PackagedComponent CIM**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="bf6ed-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="bf6ed-136">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-136">WMI does not implement this class.</span></span>

<span data-ttu-id="bf6ed-137">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bf6ed-138">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bf6ed-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf6ed-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf6ed-139">Requirements</span></span>



| <span data-ttu-id="bf6ed-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf6ed-140">Requirement</span></span> | <span data-ttu-id="bf6ed-141">Valor</span><span class="sxs-lookup"><span data-stu-id="bf6ed-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6ed-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf6ed-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bf6ed-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf6ed-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf6ed-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf6ed-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bf6ed-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf6ed-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf6ed-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf6ed-146">Namespace</span></span><br/>                | <span data-ttu-id="bf6ed-147">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bf6ed-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf6ed-148">MOF</span><span class="sxs-lookup"><span data-stu-id="bf6ed-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf6ed-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ed-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf6ed-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bf6ed-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf6ed-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf6ed-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf6ed-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf6ed-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf6ed-153">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="bf6ed-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

