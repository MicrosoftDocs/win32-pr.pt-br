---
description: Essa associação vincula um elemento gerenciado aos valores de métrica que estão sendo mantidos para ele.
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Classe Msvm_MetricForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 554f77390737b336b8660d09f737049be193b448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759239"
---
# <a name="msvm_metricforme-class"></a><span data-ttu-id="5c2b6-103">\_Classe Msvm MetricForME</span><span class="sxs-lookup"><span data-stu-id="5c2b6-103">Msvm\_MetricForME class</span></span>

<span data-ttu-id="5c2b6-104">Essa associação vincula um elemento gerenciado aos valores de métrica que estão sendo mantidos para ele.</span><span class="sxs-lookup"><span data-stu-id="5c2b6-104">This association links a managed element to the metric values being maintained for it.</span></span>

<span data-ttu-id="5c2b6-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5c2b6-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2b6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c2b6-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5c2b6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5c2b6-107">Members</span></span>

<span data-ttu-id="5c2b6-108">A classe **Msvm \_ MetricForME** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5c2b6-108">The **Msvm\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="5c2b6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c2b6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c2b6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c2b6-110">Properties</span></span>

<span data-ttu-id="5c2b6-111">A classe **Msvm \_ MetricForME** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5c2b6-111">The **Msvm\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c2b6-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="5c2b6-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c2b6-113">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="5c2b6-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="5c2b6-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c2b6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c2b6-115">Uma referência a uma instância da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa o elemento gerenciado que tem métricas definidas por **dependente** mantidas para ela.</span><span class="sxs-lookup"><span data-stu-id="5c2b6-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that has metrics defined by **Dependent** maintained for it.</span></span> <span data-ttu-id="5c2b6-116">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="5c2b6-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="5c2b6-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="5c2b6-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c2b6-118">Tipo de dados: \* \* \* \* CIM \_ BaseMetricValue \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5c2b6-118">Data type: \*\*\*\*CIM\_BaseMetricValue\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="5c2b6-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5c2b6-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c2b6-120">Uma referência a uma instância da classe **CIM \_ BaseMetricValue** que representa a métrica que o **antecessor** coletou para ela.</span><span class="sxs-lookup"><span data-stu-id="5c2b6-120">A reference to an instance of the **CIM\_BaseMetricValue** class that represents the metric that the **Antecedent** has collected for it.</span></span> <span data-ttu-id="5c2b6-121">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="5c2b6-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c2b6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c2b6-122">Requirements</span></span>



| <span data-ttu-id="5c2b6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c2b6-123">Requirement</span></span> | <span data-ttu-id="5c2b6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5c2b6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2b6-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c2b6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2b6-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5c2b6-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c2b6-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c2b6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2b6-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5c2b6-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c2b6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c2b6-129">Namespace</span></span><br/>                | <span data-ttu-id="5c2b6-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5c2b6-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5c2b6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5c2b6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c2b6-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c2b6-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c2b6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5c2b6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c2b6-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c2b6-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

