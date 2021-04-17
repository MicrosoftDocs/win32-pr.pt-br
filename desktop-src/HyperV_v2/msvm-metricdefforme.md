---
description: Define a associação entre um Msvm \_ BaseMetricDefinition e um CIM \_ managedelement para definir métricas para o último. A definição de métricas recebe o contexto do Managedelement, que é o motivo pelo qual a definição depende do elemento.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Classe Msvm_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755100"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="16e61-104">\_Classe Msvm MetricDefForME</span><span class="sxs-lookup"><span data-stu-id="16e61-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="16e61-105">Define a associação entre um [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) e um [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) para definir métricas para o último.</span><span class="sxs-lookup"><span data-stu-id="16e61-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="16e61-106">A definição de métricas recebe o contexto do Managedelement, que é o motivo pelo qual a definição depende do elemento.</span><span class="sxs-lookup"><span data-stu-id="16e61-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="16e61-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="16e61-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="16e61-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16e61-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="16e61-109">Membros</span><span class="sxs-lookup"><span data-stu-id="16e61-109">Members</span></span>

<span data-ttu-id="16e61-110">A classe **Msvm \_ MetricDefForME** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16e61-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="16e61-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16e61-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16e61-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16e61-112">Properties</span></span>

<span data-ttu-id="16e61-113">A classe **Msvm \_ MetricDefForME** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16e61-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16e61-114">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="16e61-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e61-115">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="16e61-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="16e61-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16e61-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16e61-117">Uma referência a uma instância da classe [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa o elemento gerenciado que pode ter métricas do tipo definido por **dependente** aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="16e61-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="16e61-118">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="16e61-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="16e61-119">**Depende**</span><span class="sxs-lookup"><span data-stu-id="16e61-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e61-120">Tipo de dados: **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="16e61-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="16e61-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16e61-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16e61-122">Uma referência a uma instância da classe [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa a definição de métrica que o **Antecedent** pode ter aplicado a ela.</span><span class="sxs-lookup"><span data-stu-id="16e61-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="16e61-123">Essa propriedade é herdada [**da \_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="16e61-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="16e61-124">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="16e61-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16e61-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16e61-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16e61-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16e61-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16e61-127">Indica se a métrica definida pelo **dependente** está sendo coletada para o **Antecedent**.</span><span class="sxs-lookup"><span data-stu-id="16e61-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="16e61-128">Esse será um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="16e61-128">This will be one of the following values.</span></span>



| <span data-ttu-id="16e61-129">Valor</span><span class="sxs-lookup"><span data-stu-id="16e61-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="16e61-130">Significado</span><span class="sxs-lookup"><span data-stu-id="16e61-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="16e61-131"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="16e61-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="16e61-132">A métrica está sendo coletada.</span><span class="sxs-lookup"><span data-stu-id="16e61-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="16e61-133"><dt>**Desabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="16e61-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="16e61-134">A métrica não está sendo coletada.</span><span class="sxs-lookup"><span data-stu-id="16e61-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="16e61-135"><dt>**Reservado**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="16e61-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="16e61-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="16e61-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="16e61-137">A métrica está sendo coletada para alguns, mas não para todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="16e61-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16e61-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16e61-138">Requirements</span></span>



| <span data-ttu-id="16e61-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="16e61-139">Requirement</span></span> | <span data-ttu-id="16e61-140">Valor</span><span class="sxs-lookup"><span data-stu-id="16e61-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16e61-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16e61-141">Minimum supported client</span></span><br/> | <span data-ttu-id="16e61-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="16e61-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="16e61-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16e61-143">Minimum supported server</span></span><br/> | <span data-ttu-id="16e61-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="16e61-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16e61-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="16e61-145">Namespace</span></span><br/>                | <span data-ttu-id="16e61-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="16e61-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="16e61-147">MOF</span><span class="sxs-lookup"><span data-stu-id="16e61-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16e61-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16e61-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16e61-149">DLL</span><span class="sxs-lookup"><span data-stu-id="16e61-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16e61-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16e61-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

