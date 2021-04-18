---
description: Representa uma associação na qual os valores de métrica são coletados para um elemento gerenciado.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: Classe CIM_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778597"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="b73ac-103">\_Classe CIM MetricForME</span><span class="sxs-lookup"><span data-stu-id="b73ac-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="b73ac-104">Representa uma associação na qual os valores de métrica são coletados para um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b73ac-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73ac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b73ac-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b73ac-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b73ac-106">Members</span></span>

<span data-ttu-id="b73ac-107">A classe **CIM \_ MetricForME** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b73ac-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="b73ac-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b73ac-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b73ac-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b73ac-109">Properties</span></span>

<span data-ttu-id="b73ac-110">A classe **CIM \_ MetricForME** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b73ac-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b73ac-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b73ac-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b73ac-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="b73ac-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="b73ac-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b73ac-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b73ac-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b73ac-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b73ac-115">O elemento gerenciado na associação.</span><span class="sxs-lookup"><span data-stu-id="b73ac-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="b73ac-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b73ac-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b73ac-117">Tipo de dados: **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="b73ac-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="b73ac-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b73ac-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b73ac-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="b73ac-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b73ac-120">O valor da métrica na associação.</span><span class="sxs-lookup"><span data-stu-id="b73ac-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b73ac-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b73ac-121">Requirements</span></span>



| <span data-ttu-id="b73ac-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73ac-122">Requirement</span></span> | <span data-ttu-id="b73ac-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b73ac-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73ac-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b73ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b73ac-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b73ac-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b73ac-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b73ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b73ac-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b73ac-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b73ac-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="b73ac-128">Namespace</span></span><br/>                | <span data-ttu-id="b73ac-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b73ac-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b73ac-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b73ac-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b73ac-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b73ac-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b73ac-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b73ac-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b73ac-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b73ac-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b73ac-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b73ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73ac-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="b73ac-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

