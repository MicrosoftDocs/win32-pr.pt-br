---
description: O Documento de Componentes de Backup é mantido por instâncias da interface IVssBackupComponents.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Conteúdo do documento componentes de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c844f2e9e106817c8201822d000c2f6cb94c0fa272bb5b165d98e4cc48b1c21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248336"
---
# <a name="backup-components-document-contents"></a>Conteúdo do documento componentes de backup

O Documento de Componentes de Backup é mantido por instâncias da interface [**IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) Essa interface também contém vários métodos para controlar operações de backup, manipular cópias de sombra e consultar o estado do sistema. No entanto, nem todas as informações do documento estão diretamente acessíveis por meio dessa interface.

O Documento de Componentes de Backup consiste em vários conjuntos de dados:

-   Informações sobre quais componentes foram incluídos explicitamente em uma operação de backup ou restauração
-   Uma representação das informações do componente armazenado e do autor
-   Informações de estado sobre a operação de backup/recuperação

Embora as informações do componente estão disponíveis para o solicitante e o autor, somente o autor tem acesso às informações de estado.

## <a name="component-inclusion-information"></a>Informações de inclusão de componente

O Documento de Componentes de Backup contém uma lista desses componentes explicitamente incluídos no backup e na restauração pelo solicitante. A lista contém o seguinte:

-   Componentes [*selecionáveis explicitamente incluídos.*](vssgloss-s.md)

    A inclusão desses arquivos em operações de backup é indicada por [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e em operações de restauração por [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Não selecionado para subcomponentes de backup sem um selecionável para o ancestral do componente de backup.

    Todos esses componentes deverão ser incluídos se algum componente do autor for incluído na operação. A inclusão desses arquivos em operações de backup é indicada por [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e em operações de restauração por [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Componentes adicionados implicitamente ao backup ( [](vssgloss-s.md) [*subcomponentes*](vssgloss-s.md)) que são selecionáveis para restauração e são adicionados explicitamente à restauração.

    Esses componentes podem ser selecionáveis ou não selecionáveis, mas têm um ancestral selecionável que foi usado para selecioná-los implicitamente para backup. Eles são adicionados ao Documento de Componentes de Backup por [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

As identidades dos componentes incluídos implicitamente na restauração não são armazenadas no Documento de Componentes de Backup.

O VSS tem acesso a informações sobre inclusão de componentes: os autores sem componentes explicitamente incluídos em uma restauração ou backup não recebem nenhum evento VSS após a geração dos eventos [*PrepareForBackup*](vssgloss-p.md) ou [*PreRestore.*](vssgloss-p.md)

Os autores não podem consultar diretamente essas informações. Essa não é uma limitação significativa porque, por design, os autores vss individuais não devem exigir informações detalhadas sobre o status de outros autores no sistema e, conforme mencionado acima, aqueles sem componentes incluídos não precisarão participar da operação VSS.

Um solicitante pode determinar quais componentes foram explicitamente incluídos em uma operação.

O [**método IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) retorna o número de autores com informações de componente armazenadas no Documento de Componentes de Backup (e não o número de componentes no documento).

O solicitante indexa por meio das informações do autor armazenado usando [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), que retorna instâncias da interface [**IVssWriterComponentsExt.**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) A interface **IVssWriterComponentsExt** permite que o [](vssgloss-w.md) solicitante [](vssgloss-w.md) obtenha a classe de autor e a instância de autor dos autores participantes, bem como para acessar informações sobre os componentes armazenados no Documento de Componentes de Backup.

## <a name="information-on-included-components"></a>Informações sobre componentes incluídos

A representação do Documento de Componentes de Backup dos dados do componente (que não inclui informações de especificação de arquivo e caminho), que é acessada por meio de instâncias da interface [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Solicitantes e autores obtém acesso a instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) de maneiras diferentes.

Um solicitante examina os dados do componente em um writer por writer usando instâncias da interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retornada por [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Além das informações de identificação do autor, a interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) fornece uma matriz de instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , uma para cada um dos componentes incluídos pelos autores selecionados.

Conforme registrado no Ciclo de Vida do Documento componentes de [backup,](backup-components-document-life-cycle.md)os autores podem obter acesso às mesmas informações por meio da interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) ao manipular o evento PrepareForBackup, PrepareForSnapshot, PostSnapshot, BackupComplete, PreRestore ou PostRestore.

[**O IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite que o autor e os solicitantes recebam as seguintes informações:

-   Nome, tipo e caminho lógico de um componente [*(*](vssgloss-l.md) [**GetComponentName,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname) [**GetComponentType,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype) [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Como um componente deve ser restaurado conforme indicado pelo destino [*de restauração*](vssgloss-r.md) ([**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Se um local alternativo foi usado na restauração de um arquivo ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Novas informações de destino, se alguma ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Mensagens de erro de pré e pós-restauração ([**GetPreRestoreFailureMsg,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Se um [*componente selecionável para backup*](vssgloss-s.md) que define um conjunto de componentes tiver sido selecionado para restauração ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Se um backup ou restauração foi bem-sucedido ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Quaisquer opções de backup ou restauração específicas do autor que possam ter sido definidas por [**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) ou [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**GetBackupOptions,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions) [**GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Qualquer backup de metadados específicos do autor ou metadados de restauração ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Informações de carimbo de data/hora ([**GetBackupStamp,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp) [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informações sobre subcomponentes de backup explicitamente incluídos em uma restauração ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

Ao contrário dos solicitantes, os autores podem alterar determinadas informações no Documento de Componentes de Backup por meio da interface [**IVssComponent:**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

-   Como um componente deve ser restaurado conforme indicado pelo destino de restauração ([**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Metadados de backup e restauração específicos do autor ([**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Informações de carimbo de data/hora ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Mensagens de erro de pré e pós-restauração ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Informações de estado do solicitante

Os solicitantes inserão informações sobre o estado de uma operação de backup ou restauração no Documento de Componentes de Backup usando a interface [**IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) Os aplicativos de autor podem consultar essas informações por meio da [**classe CVssWriter.**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)

As informações de estado armazenadas no documento Componentes de Backup incluem o seguinte:

Informações gerais sobre o backup

-   O tipo de backup geral (incremental, diferencial ou completo)<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por autores usando [ **CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por autores usando [ **CVssWriter::AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por autores usando [ **CVssWriter::IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperado por autores usando [ **CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Informações gerais sobre a restauração

-   O tipo de restauração geral (se a restauração é por cópia ou importação)<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Recuperado por autores usando [ **CVssWriter::GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informações sobre arquivos de suporte

-   O local dos arquivos de intervalos usados por um componente específico em operações parciais de arquivo<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Recuperado por autores (ou solicitantes) usando [ **IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Status das informações

-   Indique se um dos componentes de um determinado autor foi feito backup com êxito<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Recuperado por autores e solicitantes usando [ **IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Definido por solicitantes usando [ **IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Recuperado por autores e solicitante usando [ **IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Writer-Settable informações

-   Especificação de backup adicional para um dos componentes de um determinado autor<dl> <dt>

Definido por autores usando [ **IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Recuperado por autores e solicitantes usando [ **IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Definido por autores usando [ **IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Recuperado por autores e solicitantes usando [ **IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Definido por autores usando [ **IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Recuperado por autores e solicitantes usando [ **IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Armazenado e definido por solicitantes para um componente específico usando [ **IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Recuperado por autores e solicitantes usando [ **IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Definido por autores usando [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) ou [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Recuperado por autores e solicitantes usando [**IVssComponent::GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) ou [**IVssComponent::GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
