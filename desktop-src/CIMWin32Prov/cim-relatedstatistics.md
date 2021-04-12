---
description: A \_ associação CIM RelatedStatistics representa hierarquias e dependências de classes StatisticalInformation do CIM relacionadas \_ .
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: Classe CIM_RelatedStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500816"
---
# <a name="cim_relatedstatistics-class"></a><span data-ttu-id="12071-103">\_Classe CIM RelatedStatistics</span><span class="sxs-lookup"><span data-stu-id="12071-103">CIM\_RelatedStatistics class</span></span>

<span data-ttu-id="12071-104">A associação **CIM \_ RelatedStatistics** representa hierarquias e dependências de classes [**\_ StatisticalInformation do CIM**](cim-statisticalinformation.md) relacionadas.</span><span class="sxs-lookup"><span data-stu-id="12071-104">The **CIM\_RelatedStatistics** association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12071-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="12071-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="12071-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="12071-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="12071-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="12071-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="12071-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="12071-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12071-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12071-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="12071-110">Membros</span><span class="sxs-lookup"><span data-stu-id="12071-110">Members</span></span>

<span data-ttu-id="12071-111">A classe **CIM \_ RelatedStatistics** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="12071-111">The **CIM\_RelatedStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="12071-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12071-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12071-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="12071-113">Properties</span></span>

<span data-ttu-id="12071-114">A classe **CIM \_ RelatedStatistics** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="12071-114">The **CIM\_RelatedStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12071-115">**RelatedStats**</span><span class="sxs-lookup"><span data-stu-id="12071-115">**RelatedStats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12071-116">Tipo de dados: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="12071-116">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="12071-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12071-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12071-118">Referência às estatísticas ou métricas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="12071-118">Reference to the related statistics or metrics.</span></span>

</dd> <dt>

<span data-ttu-id="12071-119">**Estatísticas**</span><span class="sxs-lookup"><span data-stu-id="12071-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12071-120">Tipo de dados: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="12071-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="12071-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="12071-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12071-122">Referência para o objeto ou informações de estatística.</span><span class="sxs-lookup"><span data-stu-id="12071-122">Reference to the statistic information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12071-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="12071-123">Remarks</span></span>

<span data-ttu-id="12071-124">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="12071-124">WMI does not implement this class.</span></span>

<span data-ttu-id="12071-125">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="12071-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="12071-126">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="12071-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="12071-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12071-127">Requirements</span></span>



| <span data-ttu-id="12071-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="12071-128">Requirement</span></span> | <span data-ttu-id="12071-129">Valor</span><span class="sxs-lookup"><span data-stu-id="12071-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12071-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12071-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12071-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12071-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12071-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12071-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12071-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12071-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12071-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="12071-134">Namespace</span></span><br/>                | <span data-ttu-id="12071-135">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12071-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12071-136">MOF</span><span class="sxs-lookup"><span data-stu-id="12071-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12071-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12071-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12071-138">DLL</span><span class="sxs-lookup"><span data-stu-id="12071-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12071-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12071-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




