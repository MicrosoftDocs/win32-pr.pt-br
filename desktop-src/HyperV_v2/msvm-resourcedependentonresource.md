---
description: Estabelece que uma \_ instância ResourceAllocationSettingData do CIM que representa uma alocação de recursos depende de outra alocação de recursos.
ms.assetid: 567ee36a-d47b-444d-8d2f-425873f95bef
title: Classe Msvm_ResourceDependentOnResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceDependentOnResource
- Msvm_ResourceDependentOnResource.Antecedent
- Msvm_ResourceDependentOnResource.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 29cf3b607449c6a9145568e3ee858248af3c4248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757836"
---
# <a name="msvm_resourcedependentonresource-class"></a><span data-ttu-id="c0ce5-103">\_Classe Msvm ResourceDependentOnResource</span><span class="sxs-lookup"><span data-stu-id="c0ce5-103">Msvm\_ResourceDependentOnResource class</span></span>

<span data-ttu-id="c0ce5-104">Estabelece que uma instância [**\_ ResourceAllocationSettingData do CIM**](cim-resourceallocationsettingdata.md) que representa uma alocação de recursos depende de outra alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0ce5-104">Establishes that a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance representing a resource allocation depends on another resource allocation.</span></span>

<span data-ttu-id="c0ce5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c0ce5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ce5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0ce5-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceDependentOnResource : CIM_Dependency
{
  CIM_ResourceAllocationSettingData REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c0ce5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c0ce5-107">Members</span></span>

<span data-ttu-id="c0ce5-108">A classe **Msvm \_ ResourceDependentOnResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c0ce5-108">The **Msvm\_ResourceDependentOnResource** class has these types of members:</span></span>

-   [<span data-ttu-id="c0ce5-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c0ce5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0ce5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c0ce5-110">Properties</span></span>

<span data-ttu-id="c0ce5-111">A classe **Msvm \_ ResourceDependentOnResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c0ce5-111">The **Msvm\_ResourceDependentOnResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0ce5-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="c0ce5-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ce5-113">Tipo de dados: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="c0ce5-113">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c0ce5-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c0ce5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0ce5-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")</span><span class="sxs-lookup"><span data-stu-id="c0ce5-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c0ce5-116">Um [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) que representa o recurso independente nessa associação.</span><span class="sxs-lookup"><span data-stu-id="c0ce5-116">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the independent resource in this association.</span></span>

</dd> <dt>

<span data-ttu-id="c0ce5-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="c0ce5-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0ce5-118">Tipo de dados: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="c0ce5-118">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c0ce5-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c0ce5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0ce5-120">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="c0ce5-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c0ce5-121">Um [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) que representa o recurso que depende do antecessor.</span><span class="sxs-lookup"><span data-stu-id="c0ce5-121">A [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that represents the resource that is dependent on the Antecedent.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0ce5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0ce5-122">Requirements</span></span>



| <span data-ttu-id="c0ce5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0ce5-123">Requirement</span></span> | <span data-ttu-id="c0ce5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c0ce5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ce5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0ce5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ce5-126">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c0ce5-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c0ce5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0ce5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ce5-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c0ce5-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c0ce5-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0ce5-129">Namespace</span></span><br/>                | <span data-ttu-id="c0ce5-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c0ce5-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c0ce5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c0ce5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0ce5-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0ce5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ce5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ce5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0ce5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0ce5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0ce5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ce5-136">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="c0ce5-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

