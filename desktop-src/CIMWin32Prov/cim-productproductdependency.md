---
description: A \_ classe CIM ProductProductDependency representa uma associação entre dois produtos, que indica que um deve ser instalado ou ausente para que o outro funcione. Isso é conceitualmente equivalente à associação de \_ ServiceServiceDependency do CIM.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: Classe CIM_ProductProductDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010137"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="8c9d6-104">\_Classe CIM ProductProductDependency</span><span class="sxs-lookup"><span data-stu-id="8c9d6-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="8c9d6-105">A classe **CIM \_ ProductProductDependency** representa uma associação entre dois produtos, que indica que um deve ser instalado ou ausente para que o outro funcione.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="8c9d6-106">Isso é conceitualmente equivalente à associação [**de \_ ServiceServiceDependency do CIM**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="8c9d6-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c9d6-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c9d6-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c9d6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c9d6-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8c9d6-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c9d6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c9d6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="8c9d6-112">Membros</span><span class="sxs-lookup"><span data-stu-id="8c9d6-112">Members</span></span>

<span data-ttu-id="8c9d6-113">A classe **CIM \_ ProductProductDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8c9d6-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="8c9d6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8c9d6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c9d6-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8c9d6-115">Properties</span></span>

<span data-ttu-id="8c9d6-116">A classe **CIM \_ ProductProductDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c9d6-117">**DependentProduct**</span><span class="sxs-lookup"><span data-stu-id="8c9d6-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9d6-118">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="8c9d6-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="8c9d6-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8c9d6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c9d6-120">Referência ao produto que é dependente de outro produto.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="8c9d6-121">**RequiredProduct**</span><span class="sxs-lookup"><span data-stu-id="8c9d6-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9d6-122">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="8c9d6-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="8c9d6-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8c9d6-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c9d6-124">Referência ao produto necessário.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="8c9d6-125">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="8c9d6-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c9d6-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8c9d6-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8c9d6-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8c9d6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c9d6-128">Natureza da dependência do produto.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8c9d6-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="8c9d6-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8c9d6-130">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8c9d6-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="8c9d6-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8c9d6-132">Outros.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="8c9d6-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>O **produto deve ser instalado** (2)</span><span class="sxs-lookup"><span data-stu-id="8c9d6-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8c9d6-134">O produto deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="8c9d6-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>O **produto não deve ser instalado** (3)</span><span class="sxs-lookup"><span data-stu-id="8c9d6-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8c9d6-136">O produto não deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c9d6-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c9d6-137">Remarks</span></span>

<span data-ttu-id="8c9d6-138">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-138">WMI does not implement this class.</span></span>

<span data-ttu-id="8c9d6-139">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c9d6-140">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="8c9d6-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c9d6-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c9d6-141">Requirements</span></span>



| <span data-ttu-id="8c9d6-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c9d6-142">Requirement</span></span> | <span data-ttu-id="8c9d6-143">Valor</span><span class="sxs-lookup"><span data-stu-id="8c9d6-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9d6-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c9d6-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8c9d6-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c9d6-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c9d6-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c9d6-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8c9d6-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c9d6-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c9d6-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c9d6-148">Namespace</span></span><br/>                | <span data-ttu-id="8c9d6-149">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8c9d6-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c9d6-150">MOF</span><span class="sxs-lookup"><span data-stu-id="8c9d6-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c9d6-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c9d6-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c9d6-152">DLL</span><span class="sxs-lookup"><span data-stu-id="8c9d6-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c9d6-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c9d6-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




