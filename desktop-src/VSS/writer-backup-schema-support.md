---
description: Para implementar totalmente um backup, é necessário participar dos gravadores do sistema.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Suporte ao esquema de backup do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593df12f552f206d5d0eedbf8d021b69ef955c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164492"
---
# <a name="writer-backup-schema-support"></a>Suporte ao esquema de backup do gravador

Para implementar totalmente um backup, é necessário participar dos gravadores do sistema. Os diferentes tipos de backups com suporte são chamados de esquemas e são indicados por um bitmask (ou bit ou) de membros da enumeração do [**\_ \_ esquema de backup do VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) . Os esquemas válidos atualmente com suporte incluem o seguinte:

-   Esquema padrão: completo (VSS \_ BS \_ indefinido) — indica que um gravador dá suporte a um backup no qual será feito backup de todos os arquivos, independentemente da data do último backup. O histórico de backup de cada arquivo pode ser atualizado pelo solicitante, e os gravadores que dão suporte ao valor de enumeração de carimbo de data e hora do VSS \_ BS \_ serão armazenados em um carimbo de data/hora atualizado com o solicitante. Esse esquema de backup pode ser usado como a base de um backup incremental ou diferencial.

    A restauração de um backup completo requer apenas uma única imagem de backup.

-   Copiar backup (cópia do VSS \_ BS \_ ) — como o \_ esquema de backup completo do VSS BS \_ , indica que um gravador dá suporte a um backup no qual será feito backup de todos os arquivos, independentemente da data do último backup. No entanto, o histórico de backup de cada arquivo não será atualizado pelo solicitante ou gravador, e esse tipo de backup não poderá ser usado como a base de um backup incremental ou diferencial.
-   Arquivo de log ( \_ log de BS \_ do VSS) — somente os arquivos de log de um gravador devem ser copiados em backup. Isso requer que um gravador tenha adicionado pelo menos um arquivo a pelo menos um componente usando o método [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Esse tipo de backup é específico do VSS.
-   Locais de restauração personalizados (o gravador do VSS \_ BS \_ \_ dá suporte ao \_ novo \_ destino) — indica o suporte do gravador para um solicitante mudar, no momento da restauração, em que seus arquivos são restaurados. Isso significa que um gravador foi codificado para verificar tal realocação (usando [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) e tem a capacidade de trabalhar com arquivos realocados.
-   Restaurar com movimentação (o \_ gravador do VSS BS \_ \_ dá suporte à \_ restauração \_ com \_ movimentação) — indica que o gravador dá suporte à execução de várias instâncias de gravador com a mesma ID de classe e dá suporte a um solicitante que move um componente para uma instância de gravador diferente no momento da restauração. A instância do gravador é especificada usando um nome de instância de gravador persistente que foi passado como o parâmetro *wszWriterInstanceName* para o método [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) . Um solicitante pode obter o nome da instância do gravador usando [**IVssExamineWriterMetadataEx:: GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) e mover os componentes durante a restauração usando [**IVssBackupComponentsEx:: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex).

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até o Windows Server 2003 com Service Pack 1 (SP1).

-   Incremental (VSS \_ BS \_ incremental) — indica que o gravador usa a API do VSS para ajudar o solicitante, garantindo que apenas os arquivos que foram alterados ou adicionados desde o último backup completo ou incremental sejam copiados para um meio de armazenamento.

    A restauração de um backup incremental requer a imagem de backup original e todas as imagens de backup incremental feitas desde o backup inicial.

-   Diferencial ( \_ diferencial do VSS BS \_ ) — indica que o gravador usa a API do VSS para ajudar o solicitante a garantir que apenas os arquivos que foram alterados ou adicionados desde o último backup completo sejam copiados para um meio de armazenamento; todas as informações de backup intermediários são ignoradas.

    A restauração de um backup diferencial requer a imagem de backup original e a imagem de backup diferencial mais recente feita desde o último backup completo.

-   Incremental/diferencial: suporte a carimbo de data/hora ( \_ \_ o carimbo de data/hora VSS BS) — indica que um gravador dá suporte ao uso do mecanismo de carimbo de data/hora do VSS para incluir arquivos em operações incrementais ou diferenciais. No backup, o gravador deve armazenar um carimbo de backup [*do conjunto de arquivos*](vssgloss-f.md) com o método [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) e, em Restore, recuperá-lo com [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).
-   Incremental/diferencial: tempo de último suporte à modificação (VSS \_ BS \_ última \_ modificação) — indica que ao implementar backups incrementais ou diferenciais com arquivos com diferenças, um gravador pode fornecer informações de hora da última modificação independentemente. Essas informações podem ser fornecidas a um solicitante por meio do método [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) .
-   Incremental/diferencial: limitação de suporte \_ ( \_ \_ diferenciação incremental exclusiva do VSS BS \_ ) — indica suporte a gravador de esquemas de backup diferencial ou incrementais, mas somente exclusivamente: por exemplo, você não pode seguir um backup incremental com um backup diferencial.
-   Estado do sistema independente ( \_ \_ estado do \_ sistema independente do VSS BS \_ ) — indica que o gravador dá suporte ao backup de dados que faz parte do estado do sistema, mas que também pode ser feito backup independentemente do estado do sistema.

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até o Windows Vista.

-   Restauração de Roll-Forward (VSS \_ BS \_ avanço \_ Restore) – indica que o gravador dá suporte a uma configuração de solicitante de um ponto de restauração de roll-forward usando [**IVssBackupComponentsEx2:: SetRollForward**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward).

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até o Windows Vista.

-   Restore Rename (VSS \_ BS \_ Restore \_ Rename) – indica que o gravador dá suporte a uma configuração de solicitante como um nome de restauração usando [**IVssBackupComponentsEx2:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename).

    **Windows Server 2003 e Windows XP:** Esse valor não tem suporte até o Windows Vista.

-   Restauração autoritativa ( \_ restauração autoritativa do VSS BS \_ \_ ) — indica que o gravador oferece suporte a uma restauração autoritativa de configuração de solicitante usando [**IVssBackupComponentsEx2:: SetAuthoritativeRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore).

Os gravadores definem seus esquemas usando o método [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) , e um solicitante Obtém o esquema de cada gravador chamando [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



