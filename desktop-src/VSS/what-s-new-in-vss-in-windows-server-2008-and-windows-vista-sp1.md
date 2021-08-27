---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novidades no VSS no Windows Server 2008 e Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee109eec31c084dc43fb9e0cc6341f443a16e6aa06ac989a7f328d9bb3011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006116"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Novidades no VSS no Windows Server 2008 e Windows Vista SP1

Windows O Server 2008 e Windows Vista com Service Pack 1 (SP1) introduzem as seguintes alterações ao Serviço de Cópias de Sombra de Volume.

> [!Note]  
> Todas as alterações do Windows Vista se aplicam ao Windows Server 2008 e Windows Vista com SP1. Para obter detalhes sobre essas alterações, consulte [Novidades no VSS no Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Novas interfaces vss](#new-vss-interfaces)
-   [Novas enumerações vss](#new-vss-enumerations)
-   [Novas estruturas vss](#new-vss-structures)
-   [Modificações de enumeração do VSS existentes](#existing-vss-enumeration-modifications)
-   [Modificações de interface do VSS existentes](#existing-vss-interface-modifications)
-   [Novos vss writers](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Novas interfaces vss

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Novas enumerações vss

<dl>

[**\_OPÇÕES DE \_ HARDWARE \_ DO VSS**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**FALHA DE PROTEÇÃO DO VSS \_ \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**NÍVEL DE PROTEÇÃO DO VSS \_ \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Novas estruturas vss

<dl>

[**INFORMAÇÕES DE \_ PROTEÇÃO DE VOLUME \_ DO VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modificações de enumeração do VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Enumeração \_ DE ESQUEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) DE BACKUP
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valor adicionado:
</dt> <dd>

O VSS \_ BS \_ WRITER DÁ SUPORTE \_ A \_ \_ RESTAURAÇÕES PARALELAS

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeração [**\_ ATRIBUTOS DE INSTANTÂNEO DE \_ VOLUME \_ \_ DO VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ \_ POSTNAPSHOT ATRASADO

VSS \_ VOLSNAP \_ ATTR \_ TXF \_ RECOVERY

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modificações de interface do VSS existentes

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interface [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Método adicionado:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Novos vss writers

Windows O Server 2008 e Windows Vista com SP1 apresentam os seguintes autores VSS:

-   IIS Configuration Writer
-   IIS Metabase Writer
-   NPS VSS Writer
-   Serviços de Área de Trabalho Remota vss do gateway (Serviços de Terminal)
-   Serviços de Área de Trabalho Remota vss writer de licenciamento (Serviços de Terminal)

Esses autores estão documentados em [In-Box VSS Writers](in-box-vss-writers.md).

 

 



