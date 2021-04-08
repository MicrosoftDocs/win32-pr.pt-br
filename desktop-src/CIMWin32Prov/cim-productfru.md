---
description: A \_ classe CIM ProductFRU representa uma associação entre o produto e uma unidade de substituição de campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: Classe CIM_ProductFRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089040"
---
# <a name="cim_productfru-class"></a><span data-ttu-id="459e1-103">\_Classe CIM ProductFRU</span><span class="sxs-lookup"><span data-stu-id="459e1-103">CIM\_ProductFRU class</span></span>

<span data-ttu-id="459e1-104">A classe **CIM \_ ProductFRU** representa uma associação entre o produto e uma unidade de substituição de campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.</span><span class="sxs-lookup"><span data-stu-id="459e1-104">The **CIM\_ProductFRU** class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="459e1-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="459e1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="459e1-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="459e1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="459e1-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="459e1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="459e1-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="459e1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="459e1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="459e1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="459e1-110">Membros</span><span class="sxs-lookup"><span data-stu-id="459e1-110">Members</span></span>

<span data-ttu-id="459e1-111">A classe **CIM \_ ProductFRU** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="459e1-111">The **CIM\_ProductFRU** class has these types of members:</span></span>

-   [<span data-ttu-id="459e1-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="459e1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="459e1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="459e1-113">Properties</span></span>

<span data-ttu-id="459e1-114">A classe **CIM \_ ProductFRU** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="459e1-114">The **CIM\_ProductFRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="459e1-115">**FRU**</span><span class="sxs-lookup"><span data-stu-id="459e1-115">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459e1-116">Tipo de dados **: \_ FRU do CIM**</span><span class="sxs-lookup"><span data-stu-id="459e1-116">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="459e1-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="459e1-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="459e1-118">Referência à FRU.</span><span class="sxs-lookup"><span data-stu-id="459e1-118">Reference to the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="459e1-119">**Product**</span><span class="sxs-lookup"><span data-stu-id="459e1-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="459e1-120">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="459e1-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="459e1-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="459e1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="459e1-122">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="459e1-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="459e1-123">Referência ao produto ao qual a FRU é aplicada.</span><span class="sxs-lookup"><span data-stu-id="459e1-123">Reference to the product to which the FRU is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="459e1-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="459e1-124">Remarks</span></span>

<span data-ttu-id="459e1-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="459e1-125">WMI does not implement this class.</span></span>

<span data-ttu-id="459e1-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="459e1-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="459e1-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="459e1-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="459e1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="459e1-128">Requirements</span></span>



| <span data-ttu-id="459e1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="459e1-129">Requirement</span></span> | <span data-ttu-id="459e1-130">Valor</span><span class="sxs-lookup"><span data-stu-id="459e1-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="459e1-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="459e1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="459e1-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="459e1-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="459e1-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="459e1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="459e1-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="459e1-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="459e1-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="459e1-135">Namespace</span></span><br/>                | <span data-ttu-id="459e1-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="459e1-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="459e1-137">MOF</span><span class="sxs-lookup"><span data-stu-id="459e1-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="459e1-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="459e1-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="459e1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="459e1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="459e1-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="459e1-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

