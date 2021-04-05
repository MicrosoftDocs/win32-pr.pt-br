---
description: A \_ classe CIM CardInSlot associa uma placa de adaptador ao contêiner no qual ela é inserida.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: Classe CIM_CardInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826509"
---
# <a name="cim_cardinslot-class"></a><span data-ttu-id="29034-103">\_Classe CIM CardInSlot</span><span class="sxs-lookup"><span data-stu-id="29034-103">CIM\_CardInSlot class</span></span>

<span data-ttu-id="29034-104">A classe **CIM \_ CardInSlot** associa uma placa de adaptador ao contêiner no qual ela é inserida.</span><span class="sxs-lookup"><span data-stu-id="29034-104">The **CIM\_CardInSlot** class associates an adapter card with the container into which it is inserted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29034-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="29034-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="29034-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="29034-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="29034-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="29034-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="29034-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="29034-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="29034-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29034-109">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="29034-110">Membros</span><span class="sxs-lookup"><span data-stu-id="29034-110">Members</span></span>

<span data-ttu-id="29034-111">A classe **CIM \_ CardInSlot** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="29034-111">The **CIM\_CardInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="29034-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29034-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29034-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29034-113">Properties</span></span>

<span data-ttu-id="29034-114">A classe **CIM \_ CardInSlot** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29034-114">The **CIM\_CardInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29034-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="29034-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29034-116">Tipo de dados **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="29034-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="29034-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29034-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29034-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="29034-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="29034-119">Um [**\_ slot CIM**](cim-slot.md) que descreve o slot no qual o cartão é inserido.</span><span class="sxs-lookup"><span data-stu-id="29034-119">A [**CIM\_Slot**](cim-slot.md) that describes the slot into which the card is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="29034-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="29034-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29034-121">Tipo de dados **: \_ placa CIM**</span><span class="sxs-lookup"><span data-stu-id="29034-121">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="29034-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29034-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29034-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="29034-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="29034-124">Um [**\_ cartão CIM**](cim-card.md) que descreve o cartão no slot.</span><span class="sxs-lookup"><span data-stu-id="29034-124">A [**CIM\_Card**](cim-card.md) that describes the card in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29034-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="29034-125">Remarks</span></span>

<span data-ttu-id="29034-126">A classe **CIM \_ CardInSlot** é derivada de [**\_ PackageInSlot CIM**](cim-packageinslot.md).</span><span class="sxs-lookup"><span data-stu-id="29034-126">The **CIM\_CardInSlot** class is derived from [**CIM\_PackageInSlot**](cim-packageinslot.md).</span></span>

<span data-ttu-id="29034-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="29034-127">WMI does not implement this class.</span></span>

<span data-ttu-id="29034-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="29034-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="29034-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="29034-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="29034-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29034-130">Requirements</span></span>



| <span data-ttu-id="29034-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="29034-131">Requirement</span></span> | <span data-ttu-id="29034-132">Valor</span><span class="sxs-lookup"><span data-stu-id="29034-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29034-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29034-133">Minimum supported client</span></span><br/> | <span data-ttu-id="29034-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29034-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29034-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29034-135">Minimum supported server</span></span><br/> | <span data-ttu-id="29034-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29034-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29034-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="29034-137">Namespace</span></span><br/>                | <span data-ttu-id="29034-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="29034-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29034-139">MOF</span><span class="sxs-lookup"><span data-stu-id="29034-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29034-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29034-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29034-141">DLL</span><span class="sxs-lookup"><span data-stu-id="29034-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29034-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29034-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29034-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="29034-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29034-144">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="29034-144">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> </dl>

 

