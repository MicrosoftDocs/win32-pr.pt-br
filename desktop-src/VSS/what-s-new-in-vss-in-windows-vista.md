---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: o que há de novo no VSS no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9e0780b092b2bed0235ba62377da9a4f7f0b53bded9e3f7feb5d412f5ab982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751138"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>o que há de novo no VSS no Windows Vista

Windows O Vista apresenta as seguintes alterações na Serviço de Cópias de Sombra de Volume.

observe que todas as alterações do Windows vista também se aplicam ao Windows Server 2008 e ao Windows Vista com Service Pack 1 (SP1).

## <a name="new-vss-interfaces"></a>Novas interfaces VSS

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Novas classes VSS

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Novas enumerações VSS

[**\_tipo de avanço VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Modificações de enumeração do VSS existentes

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Enumeração de \_ esquema de backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:
</dt> <dd>

\_ \_ restauração AUTORITATIVA do VSS BS \_

\_estado do \_ \_ sistema independente \_ do VSS BS

\_ \_ renomear restauração do VSS BS \_

restauração do VSS \_ BS \_ avanço \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ Enumeração de \_ sinalizadores de componente**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:
</dt> <dd>

VSS \_ CF \_ não \_ estado do sistema \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores adicionados:
</dt> <dd>

desattr do VSS \_ VOLSNAP \_ \_ sem \_ AutoRecuperação

ATTR de VOLSNAP do VSS \_ \_ \_ não \_ transacionada

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Rastreamento e log de eventos do VSS

-   O arquivo de rastreamento do VSS agora pode estar localizado em qualquer volume local. nas versões do Windows anteriores ao Windows Vista, o arquivo de rastreamento do VSS não pôde ser localizado em um volume que estava no conjunto de cópias de sombra.
-   Muitas entradas de log de eventos foram refeitas para torná-las mais claras.
-   Todas as entradas do log de eventos do VSS agora contêm informações de contexto.

## <a name="vss-error-reporting"></a>Relatório de erros do VSS

-   As descrições de todos os códigos de erro do VSS agora podem ser recuperadas chamando a função [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem \_ de formato do \_ sinalizador HMODULE especificado no parâmetro *dwFlags* .
-   As mensagens de código de erro do VSS estão contidas em vsstrace.dll. Um identificador para esse módulo deve ser especificado no parâmetro *lpSource* .

## <a name="excluding-files-from-shadow-copies"></a>Excluindo arquivos de cópias de sombra

Os aplicativos ou serviços podem usar a chave do registro FilesNotToSnapshot para especificar os arquivos a serem excluídos das cópias de sombra recém-criadas. Para obter mais informações, consulte [excluindo arquivos de cópias de sombra](excluding-files-from-shadow-copies.md).

## <a name="backup-and-restore-application-compatibility"></a>Compatibilidade de aplicativos de backup e restauração

os desenvolvedores de aplicativos de backup e restauração precisam estar cientes de determinados recursos novos no Windows Vista e no Windows Server 2008. Para obter uma lista de verificação de compatibilidade de aplicativos, consulte [compatibilidade de aplicativos para backup e restauração](application-compatibility-for-backup-and-restore.md).

 

 
