---
description: Associa um sistema virtual a um instantâneo do sistema virtual.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: Classe CIM_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922148"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="02917-103">\_Classe CIM SnapshotOfVirtualSystem</span><span class="sxs-lookup"><span data-stu-id="02917-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="02917-104">Associa um sistema virtual a um instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="02917-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="02917-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02917-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="02917-106">Membros</span><span class="sxs-lookup"><span data-stu-id="02917-106">Members</span></span>

<span data-ttu-id="02917-107">A classe **CIM \_ SnapshotOfVirtualSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="02917-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="02917-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02917-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02917-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02917-109">Properties</span></span>

<span data-ttu-id="02917-110">A classe **CIM \_ SnapshotOfVirtualSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="02917-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02917-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="02917-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02917-112">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="02917-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="02917-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02917-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02917-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="02917-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="02917-115">Uma referência ao sistema de computador que representa o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="02917-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="02917-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="02917-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02917-117">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="02917-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="02917-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02917-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02917-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="02917-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="02917-120">Uma referência ao objeto de dados de configurações que representa o instantâneo do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="02917-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02917-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02917-121">Requirements</span></span>



| <span data-ttu-id="02917-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="02917-122">Requirement</span></span> | <span data-ttu-id="02917-123">Valor</span><span class="sxs-lookup"><span data-stu-id="02917-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02917-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02917-124">Minimum supported client</span></span><br/> | <span data-ttu-id="02917-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="02917-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="02917-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02917-126">Minimum supported server</span></span><br/> | <span data-ttu-id="02917-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02917-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="02917-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="02917-128">Namespace</span></span><br/>                | <span data-ttu-id="02917-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="02917-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02917-130">MOF</span><span class="sxs-lookup"><span data-stu-id="02917-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02917-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02917-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02917-132">DLL</span><span class="sxs-lookup"><span data-stu-id="02917-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02917-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02917-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02917-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="02917-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02917-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="02917-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

