---
description: Representa uma associação entre um sistema virtual e o instantâneo mais atual do sistema. Essa associação só pode existir se o sistema virtual foi criado usando um instantâneo ou se um instantâneo foi criado a partir do sistema virtual.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: Classe CIM_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 078a7c9f1669a2aa0449dce01022eba0eadcb2c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775740"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="fdc5b-104">\_Classe CIM MostCurrentSnapshotInBranch</span><span class="sxs-lookup"><span data-stu-id="fdc5b-104">CIM\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="fdc5b-105">Representa uma associação entre um sistema virtual e o instantâneo mais atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="fdc5b-105">Represents an association between a virtual system and the most current snapshot of the system.</span></span> <span data-ttu-id="fdc5b-106">Essa associação só pode existir se o sistema virtual foi criado usando um instantâneo ou se um instantâneo foi criado a partir do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fdc5b-106">This association can only exist if the virtual system was create using a snapshot or if a snapshot was created from the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc5b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdc5b-107">Syntax</span></span>

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fdc5b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fdc5b-108">Members</span></span>

<span data-ttu-id="fdc5b-109">A classe **CIM \_ MostCurrentSnapshotInBranch** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fdc5b-109">The **CIM\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="fdc5b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fdc5b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fdc5b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fdc5b-111">Properties</span></span>

<span data-ttu-id="fdc5b-112">A classe **CIM \_ MostCurrentSnapshotInBranch** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fdc5b-112">The **CIM\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fdc5b-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="fdc5b-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdc5b-114">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="fdc5b-114">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="fdc5b-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdc5b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdc5b-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="fdc5b-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fdc5b-117">Uma referência à instância do [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fdc5b-117">A reference to the instance of [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="fdc5b-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="fdc5b-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fdc5b-119">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="fdc5b-119">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="fdc5b-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fdc5b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fdc5b-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="fdc5b-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fdc5b-122">Uma referência à instância de [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa o instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="fdc5b-122">A reference to the instance of [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that represents the virtual system snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fdc5b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdc5b-123">Requirements</span></span>



| <span data-ttu-id="fdc5b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdc5b-124">Requirement</span></span> | <span data-ttu-id="fdc5b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fdc5b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc5b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc5b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc5b-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fdc5b-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fdc5b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdc5b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc5b-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdc5b-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fdc5b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fdc5b-130">Namespace</span></span><br/>                | <span data-ttu-id="fdc5b-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fdc5b-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fdc5b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="fdc5b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdc5b-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fdc5b-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdc5b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc5b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdc5b-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fdc5b-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fdc5b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fdc5b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc5b-137">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="fdc5b-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

