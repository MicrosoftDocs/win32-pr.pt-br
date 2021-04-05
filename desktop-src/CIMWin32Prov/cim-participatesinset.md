---
description: A \_ classe CIM ParticipatesInSet identifica os elementos físicos que devem ser substituídos juntos.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: Classe CIM_ParticipatesInSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826526"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="d528b-103">\_Classe CIM ParticipatesInSet</span><span class="sxs-lookup"><span data-stu-id="d528b-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="d528b-104">A classe **CIM \_ ParticipatesInSet** identifica os elementos físicos que devem ser substituídos juntos.</span><span class="sxs-lookup"><span data-stu-id="d528b-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d528b-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d528b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d528b-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d528b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d528b-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d528b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d528b-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d528b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d528b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d528b-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="d528b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d528b-110">Members</span></span>

<span data-ttu-id="d528b-111">A classe **CIM \_ ParticipatesInSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d528b-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="d528b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d528b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d528b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d528b-113">Properties</span></span>

<span data-ttu-id="d528b-114">A classe **CIM \_ ParticipatesInSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d528b-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d528b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d528b-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d528b-116">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="d528b-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="d528b-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d528b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d528b-118">Referência ao elemento físico que deve ser substituído por outros elementos, como um conjunto.</span><span class="sxs-lookup"><span data-stu-id="d528b-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="d528b-119">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="d528b-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d528b-120">Tipo de dados **: \_ Replacement do CIM**</span><span class="sxs-lookup"><span data-stu-id="d528b-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="d528b-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d528b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d528b-122">Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d528b-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d528b-123">Referência ao conjunto de substituição de elementos.</span><span class="sxs-lookup"><span data-stu-id="d528b-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d528b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d528b-124">Remarks</span></span>

<span data-ttu-id="d528b-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d528b-125">WMI does not implement this class.</span></span>

<span data-ttu-id="d528b-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d528b-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d528b-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d528b-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d528b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d528b-128">Requirements</span></span>



| <span data-ttu-id="d528b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d528b-129">Requirement</span></span> | <span data-ttu-id="d528b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d528b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d528b-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d528b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d528b-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d528b-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d528b-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d528b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d528b-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d528b-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d528b-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d528b-135">Namespace</span></span><br/>                | <span data-ttu-id="d528b-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d528b-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d528b-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d528b-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d528b-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d528b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d528b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d528b-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

