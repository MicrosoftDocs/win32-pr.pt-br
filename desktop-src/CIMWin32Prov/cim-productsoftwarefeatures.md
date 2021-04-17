---
description: A \_ associação CIM ProductSoftwareFeatures identifica os recursos de software para um produto específico.
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: Classe CIM_ProductSoftwareFeatures
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755209"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="f81f4-103">\_Classe CIM ProductSoftwareFeatures</span><span class="sxs-lookup"><span data-stu-id="f81f4-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="f81f4-104">A associação **CIM \_ ProductSoftwareFeatures** identifica os recursos de software para um produto específico.</span><span class="sxs-lookup"><span data-stu-id="f81f4-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f81f4-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f81f4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f81f4-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f81f4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f81f4-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f81f4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f81f4-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f81f4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81f4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f81f4-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="f81f4-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f81f4-110">Members</span></span>

<span data-ttu-id="f81f4-111">A classe **CIM \_ ProductSoftwareFeatures** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f81f4-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="f81f4-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f81f4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f81f4-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f81f4-113">Properties</span></span>

<span data-ttu-id="f81f4-114">A classe **CIM \_ ProductSoftwareFeatures** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f81f4-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f81f4-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="f81f4-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f81f4-116">Tipo de dados: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="f81f4-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="f81f4-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f81f4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f81f4-118">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f81f4-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f81f4-119">Referência ao componente.</span><span class="sxs-lookup"><span data-stu-id="f81f4-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="f81f4-120">**Product**</span><span class="sxs-lookup"><span data-stu-id="f81f4-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f81f4-121">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="f81f4-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="f81f4-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f81f4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f81f4-123">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f81f4-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f81f4-124">Referência ao produto.</span><span class="sxs-lookup"><span data-stu-id="f81f4-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f81f4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f81f4-125">Remarks</span></span>

<span data-ttu-id="f81f4-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f81f4-126">WMI does not implement this class.</span></span> <span data-ttu-id="f81f4-127">Para classes WMI derivadas do **CIM \_ ProductSoftwareFeatures**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f81f4-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f81f4-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f81f4-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f81f4-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f81f4-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81f4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f81f4-130">Requirements</span></span>



| <span data-ttu-id="f81f4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f81f4-131">Requirement</span></span> | <span data-ttu-id="f81f4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f81f4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f81f4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f81f4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f81f4-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f81f4-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f81f4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f81f4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f81f4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f81f4-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f81f4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f81f4-137">Namespace</span></span><br/>                | <span data-ttu-id="f81f4-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f81f4-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f81f4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f81f4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f81f4-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f81f4-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f81f4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f81f4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f81f4-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f81f4-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

