---
description: A \_ classe CIM PhysicalElementLocation associa um elemento físico a um \_ objeto de local CIM para fins de inventário ou substituição.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElementLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089488"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="33f89-103">\_Classe CIM PhysicalElementLocation</span><span class="sxs-lookup"><span data-stu-id="33f89-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="33f89-104">A classe **CIM \_ PhysicalElementLocation** associa um elemento físico a um objeto de [**\_ local CIM**](cim-location.md) para fins de inventário ou substituição.</span><span class="sxs-lookup"><span data-stu-id="33f89-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33f89-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="33f89-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="33f89-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="33f89-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="33f89-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="33f89-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="33f89-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="33f89-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f89-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33f89-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="33f89-110">Membros</span><span class="sxs-lookup"><span data-stu-id="33f89-110">Members</span></span>

<span data-ttu-id="33f89-111">A classe **CIM \_ PhysicalElementLocation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="33f89-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="33f89-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33f89-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33f89-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="33f89-113">Properties</span></span>

<span data-ttu-id="33f89-114">A classe **CIM \_ PhysicalElementLocation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="33f89-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33f89-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="33f89-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f89-116">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="33f89-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="33f89-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33f89-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33f89-118">Referência ao elemento físico cujo local está especificado.</span><span class="sxs-lookup"><span data-stu-id="33f89-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="33f89-119">**PhysicalLocation**</span><span class="sxs-lookup"><span data-stu-id="33f89-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f89-120">Tipo de dados **: \_ local do CIM**</span><span class="sxs-lookup"><span data-stu-id="33f89-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="33f89-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="33f89-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33f89-122">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="33f89-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="33f89-123">Referência ao local do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="33f89-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33f89-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="33f89-124">Remarks</span></span>

<span data-ttu-id="33f89-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="33f89-125">WMI does not implement this class.</span></span>

<span data-ttu-id="33f89-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="33f89-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="33f89-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="33f89-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="33f89-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33f89-128">Requirements</span></span>



| <span data-ttu-id="33f89-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="33f89-129">Requirement</span></span> | <span data-ttu-id="33f89-130">Valor</span><span class="sxs-lookup"><span data-stu-id="33f89-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33f89-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33f89-131">Minimum supported client</span></span><br/> | <span data-ttu-id="33f89-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33f89-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33f89-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33f89-133">Minimum supported server</span></span><br/> | <span data-ttu-id="33f89-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33f89-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33f89-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="33f89-135">Namespace</span></span><br/>                | <span data-ttu-id="33f89-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="33f89-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33f89-137">MOF</span><span class="sxs-lookup"><span data-stu-id="33f89-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33f89-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33f89-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33f89-139">DLL</span><span class="sxs-lookup"><span data-stu-id="33f89-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33f89-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33f89-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

