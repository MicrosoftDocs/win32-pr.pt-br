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
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>O que há de novo no VSS no Windows Server 2008 e no Windows Vista SP1

O Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1) apresentam as seguintes alterações na Serviço de Cópias de Sombra de Volume.

> [!Note]  
> Todas as alterações do Windows Vista se aplicam ao Windows Server 2008 e ao Windows Vista com SP1. Para obter detalhes sobre essas alterações, consulte [o que há de novo no VSS no Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Novas interfaces VSS](#new-vss-interfaces)
-   [Novas enumerações VSS](#new-vss-enumerations)
-   [Novas estruturas VSS](#new-vss-structures)
-   [Modificações de enumeração do VSS existentes](#existing-vss-enumeration-modifications)
-   [Modificações de interface VSS existentes](#existing-vss-interface-modifications)
-   [Novos gravadores VSS](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Novas interfaces VSS

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Novas enumerações VSS

<dl>

[**\_\_Opções de hardware do VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**\_falha na proteção VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**\_nível de proteção VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Novas estruturas VSS

<dl>

[**\_informações de \_ proteção de volume do VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modificações de enumeração do VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Enumeração de \_ esquema de backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valor adicionado:
</dt> <dd>

o \_ gravador do VSS BS \_ \_ dá suporte a \_ \_ restaurações paralelas

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:
</dt> <dd>

metainstantâneo do VSS \_ VOLSNAP \_ attr \_ atrasado \_

\_recuperação de \_ TxF de attr \_ \_ do VSS VOLSNAP

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modificações de interface VSS existentes

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interface [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Método adicionado:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Novos gravadores VSS

O Windows Server 2008 e o Windows Vista com SP1 apresentam os seguintes gravadores VSS:

-   Gravador de configuração do IIS
-   Gravador de metabase do IIS
-   Gravador VSS do NPS
-   Gravador VSS do gateway de Serviços de Área de Trabalho Remota (serviços de terminal)
-   Gravador VSS de licenciamento do Serviços de Área de Trabalho Remota (serviços de terminal)

Esses gravadores são documentados em [gravadores VSS](in-box-vss-writers.md)integrados.

 

 



