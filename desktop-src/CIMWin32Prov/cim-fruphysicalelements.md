---
description: A \_ classe CIM FRUPhysicalElements representa os elementos físicos que compõem uma unidade de substituição de campo (FRU).
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: Classe CIM_FRUPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920385"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="08123-103">\_Classe CIM FRUPhysicalElements</span><span class="sxs-lookup"><span data-stu-id="08123-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="08123-104">A classe **CIM \_ FRUPhysicalElements** representa os elementos físicos que compõem uma unidade de substituição de campo (FRU).</span><span class="sxs-lookup"><span data-stu-id="08123-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08123-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="08123-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08123-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="08123-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08123-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="08123-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08123-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="08123-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08123-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08123-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="08123-110">Membros</span><span class="sxs-lookup"><span data-stu-id="08123-110">Members</span></span>

<span data-ttu-id="08123-111">A classe **CIM \_ FRUPhysicalElements** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08123-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="08123-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08123-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08123-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08123-113">Properties</span></span>

<span data-ttu-id="08123-114">A classe **CIM \_ FRUPhysicalElements** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08123-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08123-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="08123-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08123-116">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="08123-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="08123-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08123-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08123-118">Referência a um elemento físico que faz parte da FRU.</span><span class="sxs-lookup"><span data-stu-id="08123-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="08123-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="08123-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08123-120">Tipo de dados **: \_ FRU do CIM**</span><span class="sxs-lookup"><span data-stu-id="08123-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="08123-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="08123-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08123-122">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="08123-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="08123-123">Referência à FRU.</span><span class="sxs-lookup"><span data-stu-id="08123-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08123-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="08123-124">Remarks</span></span>

<span data-ttu-id="08123-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="08123-125">WMI does not implement this class.</span></span>

<span data-ttu-id="08123-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="08123-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08123-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="08123-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08123-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08123-128">Requirements</span></span>



| <span data-ttu-id="08123-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="08123-129">Requirement</span></span> | <span data-ttu-id="08123-130">Valor</span><span class="sxs-lookup"><span data-stu-id="08123-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08123-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08123-131">Minimum supported client</span></span><br/> | <span data-ttu-id="08123-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08123-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08123-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08123-133">Minimum supported server</span></span><br/> | <span data-ttu-id="08123-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08123-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08123-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="08123-135">Namespace</span></span><br/>                | <span data-ttu-id="08123-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="08123-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08123-137">MOF</span><span class="sxs-lookup"><span data-stu-id="08123-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08123-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08123-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08123-139">DLL</span><span class="sxs-lookup"><span data-stu-id="08123-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08123-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08123-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

