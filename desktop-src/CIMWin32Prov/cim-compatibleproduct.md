---
description: A \_ classe CIM CompatibleProduct representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro, e assim por diante.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: Classe CIM_CompatibleProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826499"
---
# <a name="cim_compatibleproduct-class"></a><span data-ttu-id="d0187-103">\_Classe CIM CompatibleProduct</span><span class="sxs-lookup"><span data-stu-id="d0187-103">CIM\_CompatibleProduct class</span></span>

<span data-ttu-id="d0187-104">A classe **CIM \_ CompatibleProduct** representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d0187-104">The **CIM\_CompatibleProduct** class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0187-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d0187-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d0187-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d0187-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d0187-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d0187-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d0187-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d0187-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0187-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0187-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="d0187-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d0187-110">Members</span></span>

<span data-ttu-id="d0187-111">A classe **CIM \_ CompatibleProduct** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d0187-111">The **CIM\_CompatibleProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="d0187-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0187-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0187-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0187-113">Properties</span></span>

<span data-ttu-id="d0187-114">A classe **CIM \_ CompatibleProduct** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d0187-114">The **CIM\_CompatibleProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0187-115">**CompatibilityDescription**</span><span class="sxs-lookup"><span data-stu-id="d0187-115">**CompatibilityDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0187-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d0187-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0187-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0187-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0187-118">Cadeia de caracteres de forma livre que define como os dois produtos referenciados são interoperáveis, compatíveis e se há limitações de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="d0187-118">Free-form string that defines how the two referenced products are interoperable, compatible, and whether there are compatibility limitations.</span></span>

</dd> <dt>

<span data-ttu-id="d0187-119">**CompatibleProduct**</span><span class="sxs-lookup"><span data-stu-id="d0187-119">**CompatibleProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0187-120">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="d0187-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="d0187-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0187-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0187-122">Referência ao produto compatível.</span><span class="sxs-lookup"><span data-stu-id="d0187-122">Reference to the compatible product.</span></span>

</dd> <dt>

<span data-ttu-id="d0187-123">**Product**</span><span class="sxs-lookup"><span data-stu-id="d0187-123">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0187-124">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="d0187-124">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="d0187-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0187-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0187-126">Referência ao produto para o qual as ofertas compatíveis são definidas.</span><span class="sxs-lookup"><span data-stu-id="d0187-126">Reference to the product for which compatible offerings are defined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0187-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0187-127">Remarks</span></span>

<span data-ttu-id="d0187-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d0187-128">WMI does not implement this class.</span></span>

<span data-ttu-id="d0187-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d0187-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d0187-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d0187-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0187-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0187-131">Requirements</span></span>



| <span data-ttu-id="d0187-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0187-132">Requirement</span></span> | <span data-ttu-id="d0187-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d0187-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0187-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0187-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d0187-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0187-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0187-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0187-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d0187-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0187-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0187-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0187-138">Namespace</span></span><br/>                | <span data-ttu-id="d0187-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d0187-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0187-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d0187-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0187-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0187-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0187-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d0187-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0187-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0187-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




