---
description: A \_ classe CIM FRUIncludesProduct indica que uma FRU (unidade substituível de campo) pode ser composta por outros produtos.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: Classe CIM_FRUIncludesProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172487"
---
# <a name="cim_fruincludesproduct-class"></a><span data-ttu-id="fa635-103">\_Classe CIM FRUIncludesProduct</span><span class="sxs-lookup"><span data-stu-id="fa635-103">CIM\_FRUIncludesProduct class</span></span>

<span data-ttu-id="fa635-104">A classe **CIM \_ FRUIncludesProduct** indica que uma FRU (unidade substituível de campo) pode ser composta por outros produtos.</span><span class="sxs-lookup"><span data-stu-id="fa635-104">The **CIM\_FRUIncludesProduct** class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa635-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="fa635-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa635-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fa635-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa635-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fa635-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fa635-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="fa635-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa635-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa635-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="fa635-110">Membros</span><span class="sxs-lookup"><span data-stu-id="fa635-110">Members</span></span>

<span data-ttu-id="fa635-111">A classe **CIM \_ FRUIncludesProduct** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fa635-111">The **CIM\_FRUIncludesProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="fa635-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa635-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa635-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fa635-113">Properties</span></span>

<span data-ttu-id="fa635-114">A classe **CIM \_ FRUIncludesProduct** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fa635-114">The **CIM\_FRUIncludesProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa635-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="fa635-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa635-116">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="fa635-116">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="fa635-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa635-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa635-118">Referência ao produto que faz parte da FRU.</span><span class="sxs-lookup"><span data-stu-id="fa635-118">Reference to the product that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="fa635-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="fa635-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa635-120">Tipo de dados **: \_ FRU do CIM**</span><span class="sxs-lookup"><span data-stu-id="fa635-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="fa635-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fa635-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa635-122">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="fa635-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fa635-123">Referência à FRU.</span><span class="sxs-lookup"><span data-stu-id="fa635-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa635-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa635-124">Remarks</span></span>

<span data-ttu-id="fa635-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="fa635-125">WMI does not implement this class.</span></span>

<span data-ttu-id="fa635-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="fa635-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa635-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="fa635-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa635-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa635-128">Requirements</span></span>



| <span data-ttu-id="fa635-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa635-129">Requirement</span></span> | <span data-ttu-id="fa635-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fa635-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa635-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa635-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fa635-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa635-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa635-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa635-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fa635-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa635-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa635-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa635-135">Namespace</span></span><br/>                | <span data-ttu-id="fa635-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fa635-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa635-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fa635-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa635-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa635-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa635-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fa635-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa635-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa635-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

