---
description: A \_ associação CIM CardOnCard descreve as relações sobre os cartões que podem ser conectados a placas-mãe/placas, daughtercards de um adaptador ou cartões que dão suporte a módulos especiais semelhantes a cartões.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: Classe CIM_CardOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370450"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="01bba-103">\_Classe CIM CardOnCard</span><span class="sxs-lookup"><span data-stu-id="01bba-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="01bba-104">A associação **CIM \_ CardOnCard** descreve as relações sobre os cartões que podem ser conectados a placas-mãe/placas, daughtercards de um adaptador ou cartões que dão suporte a módulos especiais semelhantes a cartões.</span><span class="sxs-lookup"><span data-stu-id="01bba-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01bba-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="01bba-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01bba-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01bba-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01bba-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="01bba-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01bba-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="01bba-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01bba-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01bba-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="01bba-110">Membros</span><span class="sxs-lookup"><span data-stu-id="01bba-110">Members</span></span>

<span data-ttu-id="01bba-111">A classe **CIM \_ CardOnCard** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01bba-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="01bba-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01bba-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01bba-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01bba-113">Properties</span></span>

<span data-ttu-id="01bba-114">A classe **CIM \_ CardOnCard** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01bba-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01bba-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="01bba-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01bba-116">Tipo de dados **: \_ placa CIM**</span><span class="sxs-lookup"><span data-stu-id="01bba-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="01bba-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01bba-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01bba-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="01bba-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="01bba-119">Um [**\_ cartão CIM**](cim-card.md) que descreve o cartão que hospeda outro cartão.</span><span class="sxs-lookup"><span data-stu-id="01bba-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="01bba-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="01bba-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01bba-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01bba-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01bba-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01bba-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01bba-123">Cadeia de caracteres de forma livre que representa o posicionamento do elemento físico dentro do pacote físico.</span><span class="sxs-lookup"><span data-stu-id="01bba-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="01bba-124">Informações relativas a elementos estacionários no contêiner (por exemplo, "segundo compartimento da unidade a partir da parte superior"), ângulos, altitudes e outros dados podem ser registrados nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="01bba-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="01bba-125">Essa cadeia de caracteres pode complementar ou ser usada no lugar da instanciação do objeto de [**\_ local do CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="01bba-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="01bba-126">Essa propriedade é herdada [**do \_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="01bba-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="01bba-127">**MountOrSlotDescription**</span><span class="sxs-lookup"><span data-stu-id="01bba-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01bba-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01bba-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01bba-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01bba-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01bba-130">Descreve e identifica como o cartão é montado ou conectado ao cartão "outro".</span><span class="sxs-lookup"><span data-stu-id="01bba-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="01bba-131">As informações do slot podem ser incluídas nesse campo e podem ser suficientes para determinadas finalidades de gerenciamento, o que evita a criação de instanciações de objetos conector/slot apenas para modelar a relação de cartões para placas de hospedagem ou outros adaptadores.</span><span class="sxs-lookup"><span data-stu-id="01bba-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="01bba-132">Por outro lado, se as informações de slot e conector estiverem disponíveis, esse campo poderá ser usado para fornecer dados detalhados de montagem ou de inserção de slot.</span><span class="sxs-lookup"><span data-stu-id="01bba-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="01bba-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="01bba-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01bba-134">Tipo de dados **: \_ placa CIM**</span><span class="sxs-lookup"><span data-stu-id="01bba-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="01bba-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01bba-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01bba-136">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="01bba-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="01bba-137">Uma [**\_ placa CIM**](cim-card.md) que descreve o cartão que está conectado ou, de outra forma, montado em outro cartão.</span><span class="sxs-lookup"><span data-stu-id="01bba-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01bba-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="01bba-138">Remarks</span></span>

<span data-ttu-id="01bba-139">A classe **CIM \_ CardOnCard** é derivada do [**\_ contêiner CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="01bba-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="01bba-140">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="01bba-140">WMI does not implement this class.</span></span>

<span data-ttu-id="01bba-141">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="01bba-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01bba-142">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="01bba-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01bba-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01bba-143">Requirements</span></span>



| <span data-ttu-id="01bba-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="01bba-144">Requirement</span></span> | <span data-ttu-id="01bba-145">Valor</span><span class="sxs-lookup"><span data-stu-id="01bba-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01bba-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01bba-146">Minimum supported client</span></span><br/> | <span data-ttu-id="01bba-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01bba-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01bba-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01bba-148">Minimum supported server</span></span><br/> | <span data-ttu-id="01bba-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01bba-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01bba-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="01bba-150">Namespace</span></span><br/>                | <span data-ttu-id="01bba-151">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01bba-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01bba-152">MOF</span><span class="sxs-lookup"><span data-stu-id="01bba-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01bba-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01bba-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01bba-154">DLL</span><span class="sxs-lookup"><span data-stu-id="01bba-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01bba-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01bba-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01bba-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="01bba-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01bba-157">**\_Contêiner CIM**</span><span class="sxs-lookup"><span data-stu-id="01bba-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

