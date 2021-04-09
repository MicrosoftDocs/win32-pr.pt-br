---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: O que há de novo no VSS no Windows Server 2008 e no Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090435"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="696fc-103">O que há de novo no VSS no Windows Server 2008 e no Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="696fc-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="696fc-104">O Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1) apresentam as seguintes alterações na Serviço de Cópias de Sombra de Volume.</span><span class="sxs-lookup"><span data-stu-id="696fc-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="696fc-105">Todas as alterações do Windows Vista se aplicam ao Windows Server 2008 e ao Windows Vista com SP1.</span><span class="sxs-lookup"><span data-stu-id="696fc-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="696fc-106">Para obter detalhes sobre essas alterações, consulte [o que há de novo no VSS no Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="696fc-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="696fc-107">Novas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="696fc-108">Novas enumerações VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="696fc-109">Novas estruturas VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="696fc-110">Modificações de enumeração do VSS existentes</span><span class="sxs-lookup"><span data-stu-id="696fc-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="696fc-111">Modificações de interface VSS existentes</span><span class="sxs-lookup"><span data-stu-id="696fc-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="696fc-112">Novos gravadores VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="696fc-113">Novas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="696fc-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="696fc-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="696fc-115">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="696fc-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="696fc-116">Novas enumerações VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="696fc-117">**\_\_Opções de hardware do VSS \_**</span><span class="sxs-lookup"><span data-stu-id="696fc-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="696fc-118">**\_falha na proteção VSS \_**</span><span class="sxs-lookup"><span data-stu-id="696fc-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="696fc-119">**\_nível de proteção VSS \_**</span><span class="sxs-lookup"><span data-stu-id="696fc-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="696fc-120">Novas estruturas VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="696fc-121">**\_informações de \_ proteção de volume do VSS \_**</span><span class="sxs-lookup"><span data-stu-id="696fc-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="696fc-122">Modificações de enumeração do VSS existentes</span><span class="sxs-lookup"><span data-stu-id="696fc-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="696fc-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Enumeração de \_ esquema de backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="696fc-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="696fc-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valor adicionado:</span><span class="sxs-lookup"><span data-stu-id="696fc-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="696fc-125">o \_ gravador do VSS BS \_ \_ dá suporte a \_ \_ restaurações paralelas</span><span class="sxs-lookup"><span data-stu-id="696fc-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="696fc-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="696fc-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="696fc-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:</span><span class="sxs-lookup"><span data-stu-id="696fc-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="696fc-128">metainstantâneo do VSS \_ VOLSNAP \_ attr \_ atrasado \_</span><span class="sxs-lookup"><span data-stu-id="696fc-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="696fc-129">\_recuperação de \_ TxF de attr \_ \_ do VSS VOLSNAP</span><span class="sxs-lookup"><span data-stu-id="696fc-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="696fc-130">Modificações de interface VSS existentes</span><span class="sxs-lookup"><span data-stu-id="696fc-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="696fc-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interface [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)</span><span class="sxs-lookup"><span data-stu-id="696fc-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="696fc-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Método adicionado:</span><span class="sxs-lookup"><span data-stu-id="696fc-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="696fc-133">**BreakSnapshotSetEx**</span><span class="sxs-lookup"><span data-stu-id="696fc-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="696fc-134">Novos gravadores VSS</span><span class="sxs-lookup"><span data-stu-id="696fc-134">New VSS Writers</span></span>

<span data-ttu-id="696fc-135">O Windows Server 2008 e o Windows Vista com SP1 apresentam os seguintes gravadores VSS:</span><span class="sxs-lookup"><span data-stu-id="696fc-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="696fc-136">Gravador de configuração do IIS</span><span class="sxs-lookup"><span data-stu-id="696fc-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="696fc-137">Gravador de metabase do IIS</span><span class="sxs-lookup"><span data-stu-id="696fc-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="696fc-138">Gravador VSS do NPS</span><span class="sxs-lookup"><span data-stu-id="696fc-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="696fc-139">Gravador VSS do gateway de Serviços de Área de Trabalho Remota (serviços de terminal)</span><span class="sxs-lookup"><span data-stu-id="696fc-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="696fc-140">Gravador VSS de licenciamento do Serviços de Área de Trabalho Remota (serviços de terminal)</span><span class="sxs-lookup"><span data-stu-id="696fc-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="696fc-141">Esses gravadores são documentados em [gravadores VSS](in-box-vss-writers.md)integrados.</span><span class="sxs-lookup"><span data-stu-id="696fc-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



