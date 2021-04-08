---
description: A \_ classe CIM Statistics representa uma associação que relaciona os elementos do sistema gerenciado aos grupos estatísticos que se aplicam a eles.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: Classe CIM_Statistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920188"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="de68c-103">\_Classe de estatísticas CIM</span><span class="sxs-lookup"><span data-stu-id="de68c-103">CIM\_Statistics class</span></span>

<span data-ttu-id="de68c-104">A classe **CIM \_ Statistics** representa uma associação que relaciona os elementos do sistema gerenciado aos grupos estatísticos que se aplicam a eles.</span><span class="sxs-lookup"><span data-stu-id="de68c-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de68c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="de68c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="de68c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="de68c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="de68c-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="de68c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="de68c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="de68c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de68c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de68c-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="de68c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="de68c-110">Members</span></span>

<span data-ttu-id="de68c-111">A classe de **\_ estatísticas CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de68c-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="de68c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de68c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de68c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de68c-113">Properties</span></span>

<span data-ttu-id="de68c-114">A classe de **\_ estatísticas CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de68c-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de68c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="de68c-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de68c-116">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="de68c-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="de68c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de68c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de68c-118">Referência à classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) para a qual os dados estatísticos ou de métrica são definidos.</span><span class="sxs-lookup"><span data-stu-id="de68c-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="de68c-119">**Estatísticas**</span><span class="sxs-lookup"><span data-stu-id="de68c-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de68c-120">Tipo de dados: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="de68c-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="de68c-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de68c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de68c-122">Referência para o objeto ou informações estatísticas.</span><span class="sxs-lookup"><span data-stu-id="de68c-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de68c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="de68c-123">Remarks</span></span>

<span data-ttu-id="de68c-124">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="de68c-124">WMI does not implement this class.</span></span>

<span data-ttu-id="de68c-125">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="de68c-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="de68c-126">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="de68c-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="de68c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de68c-127">Requirements</span></span>



| <span data-ttu-id="de68c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="de68c-128">Requirement</span></span> | <span data-ttu-id="de68c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="de68c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de68c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de68c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="de68c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de68c-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de68c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de68c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="de68c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de68c-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de68c-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="de68c-134">Namespace</span></span><br/>                | <span data-ttu-id="de68c-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="de68c-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de68c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="de68c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de68c-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de68c-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de68c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="de68c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de68c-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de68c-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




