---
description: A \_ classe CIM StatisticalInformation é uma classe raiz para a coleção arbitrária de dados estatísticos ou métricas aplicáveis a um ou mais elementos do sistema gerenciados.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: Classe CIM_StatisticalInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826659"
---
# <a name="cim_statisticalinformation-class"></a><span data-ttu-id="d05ed-103">\_Classe CIM StatisticalInformation</span><span class="sxs-lookup"><span data-stu-id="d05ed-103">CIM\_StatisticalInformation class</span></span>

<span data-ttu-id="d05ed-104">A classe **CIM \_ StatisticalInformation** é uma classe raiz para a coleção arbitrária de dados estatísticos ou métricas aplicáveis a um ou mais elementos do sistema gerenciados.</span><span class="sxs-lookup"><span data-stu-id="d05ed-104">The **CIM\_StatisticalInformation** class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d05ed-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d05ed-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d05ed-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d05ed-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d05ed-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d05ed-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d05ed-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d05ed-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d05ed-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d05ed-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="d05ed-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d05ed-110">Members</span></span>

<span data-ttu-id="d05ed-111">A classe **CIM \_ StatisticalInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d05ed-111">The **CIM\_StatisticalInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="d05ed-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d05ed-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d05ed-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d05ed-113">Properties</span></span>

<span data-ttu-id="d05ed-114">A classe **CIM \_ StatisticalInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d05ed-114">The **CIM\_StatisticalInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d05ed-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d05ed-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05ed-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d05ed-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05ed-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d05ed-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d05ed-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d05ed-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d05ed-119">Breve descrição textual para a estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="d05ed-119">Short textual description for the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="d05ed-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d05ed-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05ed-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d05ed-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05ed-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d05ed-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d05ed-123">Descrição textual da estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="d05ed-123">Textual description of the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="d05ed-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d05ed-124">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d05ed-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d05ed-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d05ed-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d05ed-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d05ed-127">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="d05ed-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d05ed-128">Rótulo pelo qual a estatística ou métrica é conhecida.</span><span class="sxs-lookup"><span data-stu-id="d05ed-128">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="d05ed-129">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="d05ed-129">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d05ed-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d05ed-130">Remarks</span></span>

<span data-ttu-id="d05ed-131">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d05ed-131">WMI does not implement this class.</span></span> <span data-ttu-id="d05ed-132">Para classes WMI derivadas do **CIM \_ StatisticalInformation**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d05ed-132">For WMI classes derived from **CIM\_StatisticalInformation**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d05ed-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d05ed-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d05ed-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d05ed-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05ed-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d05ed-135">Requirements</span></span>



| <span data-ttu-id="d05ed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d05ed-136">Requirement</span></span> | <span data-ttu-id="d05ed-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d05ed-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d05ed-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d05ed-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d05ed-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d05ed-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d05ed-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d05ed-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d05ed-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d05ed-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d05ed-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="d05ed-142">Namespace</span></span><br/>                | <span data-ttu-id="d05ed-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d05ed-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d05ed-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d05ed-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d05ed-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d05ed-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d05ed-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d05ed-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d05ed-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d05ed-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

