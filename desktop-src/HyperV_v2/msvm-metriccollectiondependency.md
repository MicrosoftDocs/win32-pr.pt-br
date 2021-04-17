---
description: Representa a associação entre duas definições de métrica ou dois valores de métrica.
ms.assetid: 78fb926d-8981-443a-a82d-ebac34d38e13
title: Classe Msvm_MetricCollectionDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricCollectionDependency
- Msvm_MetricCollectionDependency.Antecedent
- Msvm_MetricCollectionDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dc24cf72975f9d4e47e414425ac4cfbfe5d11847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768749"
---
# <a name="msvm_metriccollectiondependency-class"></a><span data-ttu-id="c9026-103">\_Classe Msvm MetricCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="c9026-103">Msvm\_MetricCollectionDependency class</span></span>

<span data-ttu-id="c9026-104">Representa a associação entre duas definições de métrica ou dois valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="c9026-104">Represents the association between two metric definitions or two metric values.</span></span>

<span data-ttu-id="c9026-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c9026-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9026-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9026-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricCollectionDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c9026-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c9026-107">Members</span></span>

<span data-ttu-id="c9026-108">A classe **Msvm \_ MetricCollectionDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9026-108">The **Msvm\_MetricCollectionDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="c9026-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9026-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9026-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9026-110">Properties</span></span>

<span data-ttu-id="c9026-111">A classe **Msvm \_ MetricCollectionDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c9026-111">The **Msvm\_MetricCollectionDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9026-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="c9026-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9026-113">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c9026-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c9026-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9026-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9026-115">Uma referência a uma instância da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa a definição de métrica ou o valor de métrica independente.</span><span class="sxs-lookup"><span data-stu-id="c9026-115">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the independent metric definition or metric value.</span></span> <span data-ttu-id="c9026-116">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="c9026-116">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="c9026-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="c9026-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9026-118">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="c9026-118">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="c9026-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9026-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9026-120">Uma referência a uma instância da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa a definição da métrica ou o valor da métrica que é dependente do **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="c9026-120">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition or metric value that is dependent on the **Antecedent**.</span></span> <span data-ttu-id="c9026-121">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="c9026-121">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9026-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9026-122">Requirements</span></span>



| <span data-ttu-id="c9026-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9026-123">Requirement</span></span> | <span data-ttu-id="c9026-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c9026-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9026-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9026-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c9026-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c9026-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c9026-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9026-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c9026-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c9026-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9026-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9026-129">Namespace</span></span><br/>                | <span data-ttu-id="c9026-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c9026-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c9026-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c9026-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9026-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9026-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9026-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c9026-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9026-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9026-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

