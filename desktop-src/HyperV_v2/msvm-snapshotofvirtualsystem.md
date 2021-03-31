---
description: Associa um sistema virtual a um instantâneo que foi capturado do sistema virtual.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Classe Msvm_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921258"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="b2ee4-103">\_Classe Msvm SnapshotOfVirtualSystem</span><span class="sxs-lookup"><span data-stu-id="b2ee4-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="b2ee4-104">Associa um sistema virtual a um instantâneo que foi capturado do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="b2ee4-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ee4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2ee4-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b2ee4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b2ee4-107">Members</span></span>

<span data-ttu-id="b2ee4-108">A classe **Msvm \_ SnapshotOfVirtualSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b2ee4-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="b2ee4-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2ee4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2ee4-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2ee4-110">Properties</span></span>

<span data-ttu-id="b2ee4-111">A classe **Msvm \_ SnapshotOfVirtualSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2ee4-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2ee4-113">Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b2ee4-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2ee4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2ee4-115">Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="b2ee4-116">Essa propriedade é derivada da [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="b2ee4-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="b2ee4-117">**Depende**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2ee4-118">Tipo de dados: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b2ee4-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2ee4-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2ee4-120">Uma referência a uma instância da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa o instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="b2ee4-121">Essa propriedade é derivada da [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="b2ee4-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2ee4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2ee4-122">Requirements</span></span>



| <span data-ttu-id="b2ee4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ee4-123">Requirement</span></span> | <span data-ttu-id="b2ee4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b2ee4-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ee4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2ee4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b2ee4-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b2ee4-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2ee4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2ee4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b2ee4-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b2ee4-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2ee4-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2ee4-129">Namespace</span></span><br/>                | <span data-ttu-id="b2ee4-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b2ee4-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2ee4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b2ee4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2ee4-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2ee4-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2ee4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b2ee4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2ee4-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2ee4-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2ee4-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2ee4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ee4-136">**\_SNAPSHOTOFVIRTUALSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="b2ee4-137">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

