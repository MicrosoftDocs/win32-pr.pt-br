---
description: Para implementar totalmente um backup, é necessária a participação dos autores do sistema.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Suporte ao esquema de backup do writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b037591d6deda2657acdfe4f4e4755fef96b52bafc92e4cc51e4ef7119de1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344239"
---
# <a name="writer-backup-schema-support"></a>Suporte ao esquema de backup do writer

Para implementar totalmente um backup, é necessária a participação dos autores do sistema. Diferentes tipos de backups com suporte são chamados de esquemas e são indicados por um bitmask (ou OR bit a bit) de membros da enumeração [**VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Os esquemas válidos com suporte no momento incluem o seguinte:

-   Esquema padrão: Completo \_ (VSS BS UNDEFINED)— indica que um autor dá suporte a um backup em que todos os arquivos terão o backup feito independentemente da data do \_ último backup. O histórico de backup de cada arquivo pode ser atualizado pelo solicitante e os autores que suportam o valor de \_ enumeração TIMESTAMPED do VSS BS armazenarão um carimbo de data/hora atualizado com o \_ solicitante. Esse esquema de backup pode ser usado como base de um backup incremental ou diferencial.

    A restauração de um backup completo requer apenas uma única imagem de backup.

-   Copiar Backup (VSS BS COPY)— como o esquema de backup COMPLETO do \_ \_ \_ VSS BS, indica que um autor dá suporte a um backup em que todos os arquivos serão copiados em backup, independentemente da data do \_ último backup. No entanto, o histórico de backup de cada arquivo não será atualizado pelo solicitante ou pelo autor, e esse tipo de backup não pode ser usado como base de um backup incremental ou diferencial.
-   Arquivo de Log (LOG do VSS BS) – somente os arquivos de log de um \_ \_ autor devem ser armazenados em backup. Isso exige que um autor tenha adicionado pelo menos um arquivo a pelo menos um componente usando o [**método IVssCreateWriterMetadata::AddDatabaseLogFiles.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) Esse tipo de backup é específico do VSS.
-   Locais de restauração personalizados (VSS BS WRITER DÁ SUPORTE a NOVO DESTINO) — indica o suporte do autor para uma alteração de solicitante, no momento da restauração, em que seus \_ \_ arquivos são \_ \_ \_ restaurados. Isso significa que um autor foi codificado para verificar essa realocação (usando [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) e tem a capacidade de trabalhar com arquivos realocados.
-   Restaurar com Mover (VSS BS WRITER DÁ SUPORTE a RESTORE WITH MOVE) — indica que o autor dá suporte à execução de várias instâncias de writer com a mesma ID de classe e dá suporte a um solicitante movendo um componente para uma instância de writer diferente no momento da \_ \_ \_ \_ \_ \_ restauração. A instância de writer é especificada usando um nome de instância de writer persistente que foi passado como o *parâmetro wszWriterInstanceName* para o [**método CVssWriter::Initialize.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) Um solicitante pode obter o nome da instância do autor usando [**IVssExamineWriterMetadataEx::GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) e mover componentes durante a restauração usando [**IVssBackupComponentsEx::SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até Windows Server 2003 com Service Pack 1 (SP1).

-   Incremental (VSS BS INCREMENTAL)— indica que o autor usa a API do VSS para ajudar o solicitante, garantindo que somente os arquivos que foram alterados ou adicionados desde o último backup completo ou incremental sejam copiados para uma mídia de \_ \_ armazenamento.

    A restauração de um backup incremental requer a imagem de backup original e todas as imagens de backup incrementais feitas desde o backup inicial.

-   Diferencial (VSS BS DIFFERENTIAL)— indica que o autor usa a API do VSS para ajudar o solicitante a garantir que somente os arquivos que foram alterados ou adicionados desde o último backup completo sejam copiados para uma mídia de armazenamento; todas as informações de backup intermediárias são \_ \_ ignoradas.

    A restauração de um backup diferencial requer a imagem de backup original e a imagem de backup diferencial mais recente feita desde o último backup completo.

-   Incremental/diferencial: suporte a carimbo de data/hora \_ (VSS BS TIMESTAMPED)— indica que um autor dá suporte ao uso do mecanismo de carimbo de data/hora do VSS para incluir arquivos em operações incrementais ou \_ diferenciais. No backup, o autor deve armazenar o carimbo de [*backup*](vssgloss-f.md) de um conjunto de arquivos com o método [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) e, na restauração, recuperá-lo com [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incremental/diferencial: hora do suporte à última modificação (VSS BS LAST MODIFY)— indica que, ao implementar backups incrementais ou diferenciais com arquivos diferentes, um autor pode fornecer informações de hora de última modificação \_ \_ \_ independentemente. Essas informações podem ser fornecidas a um solicitante por meio do [**método IVssComponent::AddDifferencedFilesByLastModifyTime.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)
-   Incremental/diferencial: limitação de suporte (DIFERENCIAL INCREMENTAL EXCLUSIVO DO VSS BS) — indica o suporte do autor de esquemas de backup diferenciais ou incrementais, mas apenas exclusivamente: por exemplo, você não pode seguir um backup incremental com um \_ backup \_ \_ \_ diferencial.
-   Estado independente do sistema (ESTADO DO SISTEMA INDEPENDENTE DO VSS BS) — indica que o autor dá suporte ao backup de dados que fazem parte do estado do sistema, mas que também podem ser feito backups independentemente do estado do \_ \_ \_ \_ sistema.

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até Windows Vista.

-   Roll-Forward Restore (VSS BS ROLLFORWARD RESTORE)— indica que o autor dá suporte a um solicitante definindo um ponto de restauração \_ \_ roll-forward usando \_ [**IVssBackupComponentsEx2::SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até Windows Vista.

-   Restaurar Renomeação (VSS BS RESTORE RENAME)— indica que o autor dá suporte a um solicitante definindo um nome de restauração usando \_ \_ \_ [**IVssBackupComponentsEx2::SetRestoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até Windows Vista.

-   Restauração autoritativa (VSS BS AUTHORITATIVE RESTORE)— indica que o autor dá suporte a uma restauração autoritativa de configuração do solicitante usando \_ \_ \_ [**IVssBackupComponentsEx2::SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

Os autores configuram seus esquemas usando o método [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) e um solicitante obtém o esquema de cada autor chamando [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



