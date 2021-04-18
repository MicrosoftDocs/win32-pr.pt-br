---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: O que há de novo no VSS no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788825"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="537b4-103">O que há de novo no VSS no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="537b4-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="537b4-104">O Windows Vista apresenta as seguintes alterações na Serviço de Cópias de Sombra de Volume.</span><span class="sxs-lookup"><span data-stu-id="537b4-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="537b4-105">Observe que todas as alterações do Windows Vista também se aplicam ao Windows Server 2008 e ao Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="537b4-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="537b4-106">Novas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="537b4-106">New VSS Interfaces</span></span>

[<span data-ttu-id="537b4-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="537b4-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="537b4-108">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="537b4-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="537b4-109">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="537b4-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="537b4-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="537b4-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="537b4-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="537b4-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="537b4-112">Novas classes VSS</span><span class="sxs-lookup"><span data-stu-id="537b4-112">New VSS Classes</span></span>

[<span data-ttu-id="537b4-113">**CVssWriterEx**</span><span class="sxs-lookup"><span data-stu-id="537b4-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="537b4-114">Novas enumerações VSS</span><span class="sxs-lookup"><span data-stu-id="537b4-114">New VSS Enumerations</span></span>

[<span data-ttu-id="537b4-115">**\_tipo de avanço VSS \_**</span><span class="sxs-lookup"><span data-stu-id="537b4-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="537b4-116">Modificações de enumeração do VSS existentes</span><span class="sxs-lookup"><span data-stu-id="537b4-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="537b4-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Enumeração de \_ esquema de backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="537b4-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="537b4-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:</span><span class="sxs-lookup"><span data-stu-id="537b4-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="537b4-119">\_ \_ restauração AUTORITATIVA do VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="537b4-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="537b4-120">\_estado do \_ \_ sistema independente \_ do VSS BS</span><span class="sxs-lookup"><span data-stu-id="537b4-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="537b4-121">\_ \_ renomear restauração do VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="537b4-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="537b4-122">restauração do VSS \_ BS \_ avanço \_</span><span class="sxs-lookup"><span data-stu-id="537b4-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="537b4-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ Enumeração de \_ sinalizadores de componente**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="537b4-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="537b4-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:</span><span class="sxs-lookup"><span data-stu-id="537b4-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="537b4-125">VSS \_ CF \_ não \_ estado do sistema \_</span><span class="sxs-lookup"><span data-stu-id="537b4-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="537b4-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="537b4-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="537b4-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:</span><span class="sxs-lookup"><span data-stu-id="537b4-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="537b4-128">desattr do VSS \_ VOLSNAP \_ \_ sem \_ AutoRecuperação</span><span class="sxs-lookup"><span data-stu-id="537b4-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="537b4-129">ATTR de VOLSNAP do VSS \_ \_ \_ não \_ transacionada</span><span class="sxs-lookup"><span data-stu-id="537b4-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="537b4-130">Rastreamento e log de eventos do VSS</span><span class="sxs-lookup"><span data-stu-id="537b4-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="537b4-131">O arquivo de rastreamento do VSS agora pode estar localizado em qualquer volume local.</span><span class="sxs-lookup"><span data-stu-id="537b4-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="537b4-132">Nas versões do Windows anteriores ao Windows Vista, o arquivo de rastreamento do VSS não pôde ser localizado em um volume que estava no conjunto de cópias de sombra.</span><span class="sxs-lookup"><span data-stu-id="537b4-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="537b4-133">Muitas entradas de log de eventos foram refeitas para torná-las mais claras.</span><span class="sxs-lookup"><span data-stu-id="537b4-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="537b4-134">Todas as entradas do log de eventos do VSS agora contêm informações de contexto.</span><span class="sxs-lookup"><span data-stu-id="537b4-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="537b4-135">Relatório de erros do VSS</span><span class="sxs-lookup"><span data-stu-id="537b4-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="537b4-136">As descrições de todos os códigos de erro do VSS agora podem ser recuperadas chamando a função [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem \_ de formato do \_ sinalizador HMODULE especificado no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="537b4-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="537b4-137">As mensagens de código de erro do VSS estão contidas em vsstrace.dll.</span><span class="sxs-lookup"><span data-stu-id="537b4-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="537b4-138">Um identificador para esse módulo deve ser especificado no parâmetro *lpSource* .</span><span class="sxs-lookup"><span data-stu-id="537b4-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="537b4-139">Excluindo arquivos de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="537b4-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="537b4-140">Os aplicativos ou serviços podem usar a chave do registro FilesNotToSnapshot para especificar os arquivos a serem excluídos das cópias de sombra recém-criadas.</span><span class="sxs-lookup"><span data-stu-id="537b4-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="537b4-141">Para obter mais informações, consulte [excluindo arquivos de cópias de sombra](excluding-files-from-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="537b4-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="537b4-142">Compatibilidade de aplicativos de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="537b4-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="537b4-143">Os desenvolvedores de aplicativos de backup e restauração precisam estar cientes de determinados recursos novos no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="537b4-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="537b4-144">Para obter uma lista de verificação de compatibilidade de aplicativos, consulte [compatibilidade de aplicativos para backup e restauração](application-compatibility-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="537b4-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
