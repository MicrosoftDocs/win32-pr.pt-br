---
description: A \_ classe CIM ProductSupport representa uma associação entre produto e acesso de suporte que transmite como o suporte é obtido para o produto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Classe CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753989"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="eeb26-103">\_Classe CIM ProductSupport</span><span class="sxs-lookup"><span data-stu-id="eeb26-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="eeb26-104">A classe **CIM \_ ProductSupport** representa uma associação entre produto e acesso de suporte que transmite como o suporte é obtido para o produto.</span><span class="sxs-lookup"><span data-stu-id="eeb26-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="eeb26-105">Vários tipos de suporte estão disponíveis para um produto; o mesmo objeto de suporte pode fornecer assistência para vários produtos.</span><span class="sxs-lookup"><span data-stu-id="eeb26-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eeb26-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="eeb26-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eeb26-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eeb26-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eeb26-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eeb26-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="eeb26-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="eeb26-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb26-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eeb26-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="eeb26-111">Membros</span><span class="sxs-lookup"><span data-stu-id="eeb26-111">Members</span></span>

<span data-ttu-id="eeb26-112">A classe **CIM \_ ProductSupport** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eeb26-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="eeb26-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eeb26-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eeb26-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eeb26-114">Properties</span></span>

<span data-ttu-id="eeb26-115">A classe **CIM \_ ProductSupport** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eeb26-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eeb26-116">**Product**</span><span class="sxs-lookup"><span data-stu-id="eeb26-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb26-117">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="eeb26-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="eeb26-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eeb26-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb26-119">Referência ao produto.</span><span class="sxs-lookup"><span data-stu-id="eeb26-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="eeb26-120">**Suporte**</span><span class="sxs-lookup"><span data-stu-id="eeb26-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb26-121">Tipo de dados: **CIM \_ SupportAccess**</span><span class="sxs-lookup"><span data-stu-id="eeb26-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="eeb26-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eeb26-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb26-123">Referência ao suporte do produto.</span><span class="sxs-lookup"><span data-stu-id="eeb26-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeb26-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="eeb26-124">Remarks</span></span>

<span data-ttu-id="eeb26-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="eeb26-125">WMI does not implement this class.</span></span>

<span data-ttu-id="eeb26-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="eeb26-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eeb26-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="eeb26-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb26-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeb26-128">Requirements</span></span>



| <span data-ttu-id="eeb26-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeb26-129">Requirement</span></span> | <span data-ttu-id="eeb26-130">Valor</span><span class="sxs-lookup"><span data-stu-id="eeb26-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb26-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeb26-131">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb26-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eeb26-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eeb26-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeb26-133">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb26-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eeb26-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eeb26-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="eeb26-135">Namespace</span></span><br/>                | <span data-ttu-id="eeb26-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eeb26-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eeb26-137">MOF</span><span class="sxs-lookup"><span data-stu-id="eeb26-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeb26-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eeb26-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeb26-139">DLL</span><span class="sxs-lookup"><span data-stu-id="eeb26-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeb26-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeb26-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




