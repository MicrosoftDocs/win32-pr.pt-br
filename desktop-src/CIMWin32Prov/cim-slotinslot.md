---
description: A \_ relação de SlotInSlot do CIM representa a capacidade de um adaptador especial estender a estrutura de slot existente para permitir que cartões incompatíveis sejam conectados a um quadro ou placa de hospedagem.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Classe CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749322"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="bfab7-103">\_Classe CIM SlotInSlot</span><span class="sxs-lookup"><span data-stu-id="bfab7-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="bfab7-104">A relação de **\_ SlotInSlot do CIM** representa a capacidade de um adaptador especial estender a estrutura de slot existente para permitir que cartões incompatíveis sejam conectados a um quadro ou placa de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="bfab7-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="bfab7-105">Os slots são tipos especiais de conectores nos quais as placas de adaptador são normalmente inseridas.</span><span class="sxs-lookup"><span data-stu-id="bfab7-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="bfab7-106">O adaptador cria efetivamente um novo slot e pode ser considerado (conceitualmente) como um slot em um slot.</span><span class="sxs-lookup"><span data-stu-id="bfab7-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="bfab7-107">Os cartões que, de outra forma, seriam incompatíveis fisicamente ou eletricamente com os slots existentes seriam compatíveis com a interface do slot fornecido pelo adaptador.</span><span class="sxs-lookup"><span data-stu-id="bfab7-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="bfab7-108">Por exemplo, as placas de rede são muito caras.</span><span class="sxs-lookup"><span data-stu-id="bfab7-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="bfab7-109">À medida que um novo hardware é disponibilizado, as configurações do chassi e do cartão são alteradas.</span><span class="sxs-lookup"><span data-stu-id="bfab7-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="bfab7-110">Para proteger o investimento de seus clientes, os fornecedores de rede fabricarão adaptadores especiais que permitem que os cartões antigos se encaixem em novos chassis ou placas de hospedagem ou novos cartões para se ajustarem em cartões antigos usando um adaptador especial que caiba em um ou mais slots existentes e apresente um novo slot ao qual o cartão pode se ajustar.</span><span class="sxs-lookup"><span data-stu-id="bfab7-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfab7-111">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bfab7-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bfab7-112">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bfab7-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bfab7-113">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bfab7-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bfab7-114">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="bfab7-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfab7-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfab7-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="bfab7-116">Membros</span><span class="sxs-lookup"><span data-stu-id="bfab7-116">Members</span></span>

<span data-ttu-id="bfab7-117">A classe **CIM \_ SlotInSlot** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bfab7-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="bfab7-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bfab7-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfab7-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bfab7-119">Properties</span></span>

<span data-ttu-id="bfab7-120">A classe **CIM \_ SlotInSlot** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bfab7-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfab7-121">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="bfab7-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfab7-122">Tipo de dados **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="bfab7-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="bfab7-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bfab7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfab7-124">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="bfab7-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bfab7-125">Um [**\_ slot CIM**](cim-slot.md) que descreve os slots existentes da placa de hospedagem ou o quadro que está sendo adaptado para acomodar um cartão que, de outra forma, não seria fisicamente e/ou eletricamente compatível com ele.</span><span class="sxs-lookup"><span data-stu-id="bfab7-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="bfab7-126">**Depende**</span><span class="sxs-lookup"><span data-stu-id="bfab7-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfab7-127">Tipo de dados **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="bfab7-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="bfab7-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bfab7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfab7-129">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="bfab7-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bfab7-130">Um [**\_ slot CIM**](cim-slot.md) que descreve o novo slot fornecido pela placa adaptadora.</span><span class="sxs-lookup"><span data-stu-id="bfab7-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfab7-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfab7-131">Remarks</span></span>

<span data-ttu-id="bfab7-132">A classe **CIM \_ SlotInSlot** é derivada de [**CIM \_ conectado**](cim-connectedto.md)a.</span><span class="sxs-lookup"><span data-stu-id="bfab7-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="bfab7-133">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="bfab7-133">WMI does not implement this class.</span></span>

<span data-ttu-id="bfab7-134">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bfab7-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bfab7-135">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bfab7-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfab7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfab7-136">Requirements</span></span>



| <span data-ttu-id="bfab7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfab7-137">Requirement</span></span> | <span data-ttu-id="bfab7-138">Valor</span><span class="sxs-lookup"><span data-stu-id="bfab7-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfab7-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfab7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bfab7-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfab7-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfab7-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfab7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bfab7-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfab7-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfab7-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="bfab7-143">Namespace</span></span><br/>                | <span data-ttu-id="bfab7-144">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bfab7-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bfab7-145">MOF</span><span class="sxs-lookup"><span data-stu-id="bfab7-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfab7-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfab7-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfab7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="bfab7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfab7-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfab7-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfab7-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfab7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfab7-150">**CIM \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="bfab7-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

