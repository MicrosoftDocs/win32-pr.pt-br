---
description: Representa uma associação na qual uma \_ instância de RESOURCEALLOCATIONSETTINGDATA CIM é alocada de um pool de recursos.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: Classe CIM_ResourceAllocationFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922255"
---
# <a name="cim_resourceallocationfrompool-class"></a><span data-ttu-id="5a923-103">\_Classe CIM ResourceAllocationFromPool</span><span class="sxs-lookup"><span data-stu-id="5a923-103">CIM\_ResourceAllocationFromPool class</span></span>

<span data-ttu-id="5a923-104">Representa uma associação na qual uma instância de [**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md) é alocada de um pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a923-104">Represents an association in which a [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instance is allocated from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a923-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a923-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5a923-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5a923-106">Members</span></span>

<span data-ttu-id="5a923-107">A classe **CIM \_ ResourceAllocationFromPool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5a923-107">The **CIM\_ResourceAllocationFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="5a923-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a923-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a923-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5a923-109">Properties</span></span>

<span data-ttu-id="5a923-110">A classe **CIM \_ ResourceAllocationFromPool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5a923-110">The **CIM\_ResourceAllocationFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a923-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="5a923-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a923-112">Tipo de dados: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="5a923-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="5a923-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a923-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a923-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="5a923-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="5a923-115">O pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a923-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="5a923-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="5a923-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a923-117">Tipo de dados: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="5a923-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="5a923-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5a923-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a923-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="5a923-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5a923-120">Os dados de alocação de recursos.</span><span class="sxs-lookup"><span data-stu-id="5a923-120">The resource allocation data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a923-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a923-121">Requirements</span></span>



| <span data-ttu-id="5a923-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a923-122">Requirement</span></span> | <span data-ttu-id="5a923-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5a923-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a923-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a923-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5a923-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5a923-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5a923-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a923-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5a923-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a923-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5a923-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a923-128">Namespace</span></span><br/>                | <span data-ttu-id="5a923-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5a923-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5a923-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5a923-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a923-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a923-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a923-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5a923-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a923-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a923-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a923-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a923-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a923-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="5a923-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

