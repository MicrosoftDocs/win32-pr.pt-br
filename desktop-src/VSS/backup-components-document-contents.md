---
description: O documento de componentes de backup é mantido por instâncias da interface IVssBackupComponents.
ms.assetid: 8c7ebba8-58c4-4733-ba59-802abf902c5e
title: Conteúdo do documento de componentes de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e12c88ebffa0037702e1f30dd818d4fd23fe4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837265"
---
# <a name="backup-components-document-contents"></a>Conteúdo do documento de componentes de backup

O documento de componentes de backup é mantido por instâncias da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Essa interface também contém vários métodos para controlar as operações de backup, manipular cópias de sombra e consultar o estado do sistema. No entanto, nem todas as informações do documento são diretamente acessíveis por meio dessa interface.

O documento de componentes de backup consiste em vários conjuntos de dados:

-   Informações sobre quais componentes foram explicitamente incluídos em uma operação de backup ou restauração
-   Uma representação do componente armazenado e informações do gravador
-   Informações de estado sobre a operação de backup/recuperação

Embora as informações do componente estejam disponíveis para o solicitante e o gravador, somente o gravador tem acesso às informações de estado.

## <a name="component-inclusion-information"></a>Informações de inclusão de componente

O documento componentes de backup contém uma lista desses componentes explicitamente incluídos no backup e na restauração pelo solicitante. A lista contém o seguinte:

-   [*Componentes selecionáveis*](vssgloss-s.md)explicitamente incluídos.

    A inclusão desses arquivos em operações de backup é indicada por [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e em operações de restauração por [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Não selecionável para subcomponentes de backup sem selecionável para componente de backup ancestral.

    Todos esses componentes devem ser incluídos se algum componente do gravador for incluído na operação. A inclusão desses arquivos em operações de backup é indicada por [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) e em operações de restauração por [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).

-   Componentes adicionados implicitamente ao backup ([*Subcomponentes*](vssgloss-s.md)) que são [*selecionáveis para restauração*](vssgloss-s.md) e são adicionados explicitamente à restauração.

    Esses componentes podem ser selecionáveis ou não selecionáveis, mas têm um ancestral selecionável que foi usado para selecioná-los implicitamente para backup. Eles são adicionados ao documento de componentes de backup por [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

As identidades dos componentes incluídos implicitamente na restauração não são armazenadas no documento componentes de backup.

O VSS tem acesso a informações sobre inclusão de componentes: gravadores sem componentes explicitamente incluídos em uma restauração ou backup não recebem eventos VSS após a geração dos eventos [*PrepareForBackup*](vssgloss-p.md) ou [*prerestore*](vssgloss-p.md) .

Os gravadores não podem consultar essas informações diretamente. Essa não é uma limitação significativa porque, por design, os gravadores de VSS individuais não devem exigir informações detalhadas sobre o status de outros gravadores no sistema e, como mencionado acima, aqueles sem componentes incluídos não precisarão participar da operação VSS.

Um solicitante pode determinar quais componentes foram explicitamente incluídos em uma operação.

O método [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) retorna o número de gravadores com informações de componente armazenadas no documento de componentes de backup (e não o número de componentes no documento).

O solicitante indexa por meio das informações do gravador armazenado usando [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents), que retorna instâncias da interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) . A interface **IVssWriterComponentsExt** permite que o solicitante obtenha a [*classe do gravador*](vssgloss-w.md) e a [*instância do gravador*](vssgloss-w.md) de escritores participantes, bem como acesse informações sobre aqueles de seus componentes armazenados no documento de componentes de backup.

## <a name="information-on-included-components"></a>Informações sobre os componentes incluídos

A representação do documento dos componentes de backup dos dados do componente (que não inclui informações de especificação de caminho e arquivo), que é acessado por meio de instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Os solicitantes e os gravadores obtêm acesso a instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) de diferentes maneiras.

Um solicitante examina os dados do componente em um gravador por gravador usando instâncias da interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retornada por [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Além das informações de identificação do gravador, a interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) fornece uma matriz de instâncias da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) — uma para cada um dos componentes do gravadores incluídos.

Conforme observado no [ciclo de vida do documento dos componentes de backup](backup-components-document-life-cycle.md), os gravadores podem obter acesso às mesmas informações por meio da interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) ao manipular o evento PrepareForBackup, PrepareForSnapshot, upsnapshot, BackupComplete, prerestore ou createrestore.

O [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite que o gravador e os solicitantes obtenham as seguintes informações:

-   O nome, o tipo e o [*caminho lógico*](vssgloss-l.md) do componente [**(GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponentname), [**getcomponenttype**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getcomponenttype), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath))
-   Como um componente deve ser restaurado conforme indicado pelo [*destino de restauração*](vssgloss-r.md) ([**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget))
-   Se um local alternativo foi usado na restauração de um arquivo ([**GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping), [**GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount))
-   Novas informações de destino, se houver ([**GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget), [**GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount))
-   Mensagens de erro de pré e pós-restauração ([**GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg))
-   Se uma seleção para o componente [*de backup*](vssgloss-s.md) que define um conjunto de componentes tiver sido selecionada para restauração ([**IsSelectedForRestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-isselectedforrestore))
-   Se um backup ou restauração foi bem-sucedido ([**GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded), [**GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus))
-   Qualquer opção de backup ou restauração específica do gravador que possa ter sido definida por [**IVssBackupComponents:: setbackupoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions) ou [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) ([**getbackupoptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions), [**getrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions))
-   Qualquer backup de metadados específico do gravador ou metadados de restauração ([**GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)), [**GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata))
-   Informações de carimbo de data/hora ([**GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp), [**GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp))
-   Informações sobre subcomponentes de backup incluídos explicitamente em uma restauração ([**GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent), [**GetRestoreSubcomponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount))

Ao contrário dos solicitantes, os gravadores podem alterar determinadas informações no documento componentes de backup por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) :

-   Como um componente deve ser restaurado conforme indicado pelo destino de restauração ([**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget))
-   Metadados de backup e restauração específicos do gravador ([**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata), [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata))
-   Informações de carimbo de data/hora ([**SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp))
-   Mensagens de erro de pré e pós-restauração ([**SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg), [**SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg))

## <a name="requester-state-information"></a>Informações de estado do solicitante

Os solicitantes inserem informações sobre o estado de uma operação de backup ou restauração no documento componentes de backup usando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) . Aplicativos de gravador são capazes de consultar essas informações por meio da classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) .

As informações de estado armazenadas no documento componentes de backup incluem o seguinte:

Informações gerais sobre o backup

-   O tipo de backup geral (incremental, diferencial ou completo)<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperados por gravadores usando [ **CVssWriter:: getbackuptype**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype)
</dt> </dl>
-   Whether component operations are supported<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperados por gravadores usando [ **CVssWriter:: AreComponentsSelected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-arecomponentsselected)
</dt> </dl>
-   Whether the bootable system state is backed up<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperados por gravadores usando [ **CVssWriter:: IsBootableStateBackedUp**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-isbootablesystemstatebackedup)
</dt> </dl>
-   Whether partial file operations are supported<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate)
</dt> <dt>

Recuperados por gravadores usando [ **CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)
</dt> </dl>

Informações gerais sobre a restauração

-   O tipo de restauração geral (se a restauração é por cópia ou importação)<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)
</dt> <dt>

Recuperados por gravadores usando [ **CVssWriter:: getrestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)
</dt> </dl>

Informações sobre arquivos de suporte

-   O local dos arquivos de intervalos usados por um componente específico em operações de arquivo parcial<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)
</dt> <dt>

Recuperados por gravadores (ou solicitantes) usando [ **IVssComponent:: getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)
</dt> </dl>

Status das informações

-   Indicar se um dos componentes de um determinado gravador foi submetido a backup com êxito<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
</dt> <dt>

Recuperados por gravadores e solicitantes usando [ **IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)
</dt> </dl>
-   Indicate whether one of a given writer's components was successfully restored<dl> <dt>

Definir por solicitantes usando [ **IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)
</dt> <dt>

Recuperados por gravadores e solicitante usando [ **IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)
</dt> </dl>

Informações de Writer-Settable

-   Especificação de backup adicional para um dos componentes de um determinado gravador<dl> <dt>

Definido por gravadores usando [ **IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)
</dt> <dt>

Recuperados por gravadores e solicitantes usando [ **IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)
</dt> </dl>
-   Additional restore specification for one of a given writer's components<dl> <dt>

Definido por gravadores usando [ **IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)
</dt> <dt>

Recuperados por gravadores e solicitantes usando [ **IVssComponent:: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the current backup of one of its component's backups<dl> <dt>

Definido por gravadores usando [ **IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)
</dt> <dt>

Recuperados por gravadores e solicitantes usando [ **IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)
</dt> </dl>
-   A backup stamp that indicates, in a writer's own specific format, the time of the last backup of one of its components' backups using a backup stamp initially set by <a href="/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp">IVssComponent::SetBackupStamp</a><dl> <dt>

Armazenados e definidos por solicitantes para um componente específico usando [ **IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp)
</dt> <dt>

Recuperados por gravadores e solicitantes usando [ **IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
</dt> </dl>
-   Error messages for failure before and after restore operations<dl> <dt>

Definido por gravadores usando [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg) ou [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)
</dt> <dt>

Recuperados por gravadores e solicitantes usando [**IVssComponent:: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg) ou [**IVssComponent:: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg)
</dt> </dl>

 

 
