---
description: Representa uma associação de objetos de valor de métrica com suas definições de métricas.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Classe Msvm_MetricInstance
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759403"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="331ce-103">\_Classe Msvm MetricInstance</span><span class="sxs-lookup"><span data-stu-id="331ce-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="331ce-104">Representa uma associação de objetos de valor de métrica com suas definições de métricas.</span><span class="sxs-lookup"><span data-stu-id="331ce-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="331ce-105">Essa associação vincula uma instância de [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) ao seu [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="331ce-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="331ce-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="331ce-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="331ce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="331ce-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="331ce-108">Membros</span><span class="sxs-lookup"><span data-stu-id="331ce-108">Members</span></span>

<span data-ttu-id="331ce-109">A classe **Msvm \_ MetricInstance** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="331ce-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="331ce-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="331ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="331ce-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="331ce-111">Properties</span></span>

<span data-ttu-id="331ce-112">A classe **Msvm \_ MetricInstance** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="331ce-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="331ce-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="331ce-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="331ce-114">Tipo de dados: \* \* \* \* CIM \_ managedelement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="331ce-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="331ce-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="331ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="331ce-116">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="331ce-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="331ce-117">Uma referência a uma instância da classe [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que representa as definições de métricas.</span><span class="sxs-lookup"><span data-stu-id="331ce-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="331ce-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="331ce-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="331ce-119">Tipo de dados: \* \* \* \* CIM \_ managedelement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="331ce-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="331ce-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="331ce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="331ce-121">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="331ce-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="331ce-122">Uma referência a uma instância da classe [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) que representa as métricas que dependem do **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="331ce-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="331ce-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="331ce-123">Requirements</span></span>



| <span data-ttu-id="331ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="331ce-124">Requirement</span></span> | <span data-ttu-id="331ce-125">Valor</span><span class="sxs-lookup"><span data-stu-id="331ce-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331ce-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="331ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="331ce-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="331ce-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="331ce-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="331ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="331ce-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="331ce-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="331ce-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="331ce-130">Namespace</span></span><br/>                | <span data-ttu-id="331ce-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="331ce-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="331ce-132">MOF</span><span class="sxs-lookup"><span data-stu-id="331ce-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="331ce-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="331ce-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="331ce-134">DLL</span><span class="sxs-lookup"><span data-stu-id="331ce-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="331ce-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="331ce-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




