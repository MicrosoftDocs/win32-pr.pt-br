---
description: Exporte os dados de configuração a serem passados para o método ExportSnapshot da \_ classe Msvm CollectionSnapshotService.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Classe Msvm_CollectionSnapshotExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753473"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="670db-103">\_Classe Msvm CollectionSnapshotExportSettingData</span><span class="sxs-lookup"><span data-stu-id="670db-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="670db-104">Exporte os dados de configuração a serem passados para o método ExportSnapshot da classe [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="670db-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="670db-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="670db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="670db-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="670db-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="670db-107">Membros</span><span class="sxs-lookup"><span data-stu-id="670db-107">Members</span></span>

<span data-ttu-id="670db-108">A classe **Msvm \_ CollectionSnapshotExportSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="670db-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="670db-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="670db-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="670db-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="670db-110">Properties</span></span>

<span data-ttu-id="670db-111">A classe **Msvm \_ CollectionSnapshotExportSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="670db-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="670db-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="670db-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670db-113">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="670db-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="670db-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="670db-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="670db-115">Indica a intenção de como os conjuntos de backup exportados seriam usados:</span><span class="sxs-lookup"><span data-stu-id="670db-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="670db-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span><span class="sxs-lookup"><span data-stu-id="670db-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="670db-117">Todos os conjuntos de backup exportados completos e diferenciais seriam preservados como estão.</span><span class="sxs-lookup"><span data-stu-id="670db-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="670db-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span><span class="sxs-lookup"><span data-stu-id="670db-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="670db-119">Os conjuntos de backup exportados completos e diferenciais seriam mesclados para sintetizar conjuntos de backup completos.</span><span class="sxs-lookup"><span data-stu-id="670db-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="670db-120">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="670db-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670db-121">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="670db-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="670db-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="670db-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="670db-123">Se **for true**, o armazenamento da VM será copiado quando a VM for exportada.</span><span class="sxs-lookup"><span data-stu-id="670db-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="670db-124">Caso contrário, **false.**</span><span class="sxs-lookup"><span data-stu-id="670db-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="670db-125">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="670db-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="670db-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="670db-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="670db-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="670db-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="670db-128">Base para exportação diferencial.</span><span class="sxs-lookup"><span data-stu-id="670db-128">Base for differential export.</span></span> <span data-ttu-id="670db-129">Este é o caminho para uma instância [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa o ponto de referência, ou o caminho para uma instância do [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) que representa o instantâneo a ser usado como base para a exportação diferencial.</span><span class="sxs-lookup"><span data-stu-id="670db-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="670db-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="670db-130">Requirements</span></span>



| <span data-ttu-id="670db-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="670db-131">Requirement</span></span> | <span data-ttu-id="670db-132">Valor</span><span class="sxs-lookup"><span data-stu-id="670db-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670db-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="670db-133">Minimum supported client</span></span><br/> | <span data-ttu-id="670db-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="670db-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="670db-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="670db-135">Minimum supported server</span></span><br/> | <span data-ttu-id="670db-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="670db-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="670db-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="670db-137">Namespace</span></span><br/>                | <span data-ttu-id="670db-138">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="670db-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="670db-139">MOF</span><span class="sxs-lookup"><span data-stu-id="670db-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="670db-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="670db-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="670db-141">DLL</span><span class="sxs-lookup"><span data-stu-id="670db-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="670db-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="670db-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="670db-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="670db-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="670db-144">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="670db-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




