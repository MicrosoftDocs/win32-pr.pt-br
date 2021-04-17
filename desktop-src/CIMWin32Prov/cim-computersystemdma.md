---
description: A \_ classe CIM ComputerSystemDMA representa uma associação entre um sistema de computador e seus canais de DMA (acesso direto à memória) disponíveis.
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemDMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754396"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="b6c76-103">\_Classe CIM ComputerSystemDMA</span><span class="sxs-lookup"><span data-stu-id="b6c76-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="b6c76-104">A classe **CIM \_ ComputerSystemDMA** representa uma associação entre um sistema de computador e seus canais de DMA (acesso direto à memória) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b6c76-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6c76-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b6c76-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b6c76-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b6c76-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b6c76-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b6c76-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b6c76-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b6c76-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c76-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6c76-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="b6c76-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b6c76-110">Members</span></span>

<span data-ttu-id="b6c76-111">A classe **CIM \_ ComputerSystemDMA** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b6c76-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="b6c76-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6c76-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6c76-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6c76-113">Properties</span></span>

<span data-ttu-id="b6c76-114">A classe **CIM \_ ComputerSystemDMA** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6c76-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6c76-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b6c76-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c76-116">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="b6c76-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="b6c76-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6c76-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c76-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="b6c76-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b6c76-119">Um [**\_ sistema**](cim-computersystem.md) de computador CIM que descreve o computador associado ao DMA.</span><span class="sxs-lookup"><span data-stu-id="b6c76-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="b6c76-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b6c76-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c76-121">Tipo de dados **: \_ DMA do CIM**</span><span class="sxs-lookup"><span data-stu-id="b6c76-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="b6c76-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6c76-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c76-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**fraca**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b6c76-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b6c76-124">Um [**\_ DMA do CIM**](cim-dma.md) que descreve um canal DMA do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="b6c76-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6c76-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c76-125">Remarks</span></span>

<span data-ttu-id="b6c76-126">A classe **CIM \_ ComputerSystemDMA** é derivada de [**\_ ComputerSystemResource CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="b6c76-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="b6c76-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b6c76-127">WMI does not implement this class.</span></span>

<span data-ttu-id="b6c76-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b6c76-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b6c76-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b6c76-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c76-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c76-130">Requirements</span></span>



| <span data-ttu-id="b6c76-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c76-131">Requirement</span></span> | <span data-ttu-id="b6c76-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b6c76-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c76-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c76-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c76-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6c76-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6c76-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c76-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c76-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6c76-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6c76-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6c76-137">Namespace</span></span><br/>                | <span data-ttu-id="b6c76-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b6c76-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6c76-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b6c76-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6c76-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6c76-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6c76-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c76-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c76-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6c76-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c76-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6c76-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c76-144">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="b6c76-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

