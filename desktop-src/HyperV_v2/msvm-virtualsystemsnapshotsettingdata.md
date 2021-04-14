---
description: Fornece informações adicionais a serem usadas com o método createsnapshot da classe Msvm \_ VirtualSystemSnapshotService.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Classe Msvm_VirtualSystemSnapshotSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370600"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="94105-103">\_Classe Msvm VirtualSystemSnapshotSettingData</span><span class="sxs-lookup"><span data-stu-id="94105-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="94105-104">Fornece informações adicionais a serem usadas com o método [**createsnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) da classe [**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="94105-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="94105-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="94105-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94105-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94105-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="94105-107">Membros</span><span class="sxs-lookup"><span data-stu-id="94105-107">Members</span></span>

<span data-ttu-id="94105-108">A classe **Msvm \_ VirtualSystemSnapshotSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94105-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="94105-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94105-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94105-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="94105-110">Properties</span></span>

<span data-ttu-id="94105-111">A classe **Msvm \_ VirtualSystemSnapshotSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="94105-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94105-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="94105-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94105-113">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="94105-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="94105-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94105-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94105-115">O nível de consistência do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="94105-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94105-116">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="94105-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="94105-117">**Consistente** com o aplicativo (1)</span><span class="sxs-lookup"><span data-stu-id="94105-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="94105-118">**Falha consistente** (2)</span><span class="sxs-lookup"><span data-stu-id="94105-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94105-119">**GuestBackupType**</span><span class="sxs-lookup"><span data-stu-id="94105-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94105-120">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="94105-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="94105-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94105-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94105-122">Tipo de backup a ser usado dentro do convidado.</span><span class="sxs-lookup"><span data-stu-id="94105-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="94105-123">Propriedade adicionada no Windows 10, versão 1703</span><span class="sxs-lookup"><span data-stu-id="94105-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="94105-124">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="94105-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="94105-125">**Completo** (1)</span><span class="sxs-lookup"><span data-stu-id="94105-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="94105-126">**Cópia** (2)</span><span class="sxs-lookup"><span data-stu-id="94105-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94105-127">**IgnoreNonSnapshottableDisks**</span><span class="sxs-lookup"><span data-stu-id="94105-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94105-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="94105-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="94105-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94105-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94105-130">Especifica se discos não-instantâneos, como discos de passagem e discos de Fibre Channel, devem ser ignorados durante a criação do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="94105-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94105-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94105-131">Requirements</span></span>



| <span data-ttu-id="94105-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="94105-132">Requirement</span></span> | <span data-ttu-id="94105-133">Valor</span><span class="sxs-lookup"><span data-stu-id="94105-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94105-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94105-134">Minimum supported client</span></span><br/> | <span data-ttu-id="94105-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="94105-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="94105-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94105-136">Minimum supported server</span></span><br/> | <span data-ttu-id="94105-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="94105-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="94105-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="94105-138">Namespace</span></span><br/>                | <span data-ttu-id="94105-139">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="94105-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="94105-140">MOF</span><span class="sxs-lookup"><span data-stu-id="94105-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94105-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94105-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94105-142">DLL</span><span class="sxs-lookup"><span data-stu-id="94105-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94105-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94105-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94105-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="94105-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94105-145">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="94105-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




