---
description: Às vezes, é desejável criar uma cópia de sombra em um sistema, mas usar a cópia de sombra em um segundo sistema.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importando volumes copiados de sombra transportável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d259fbc047d088ee1f7064804a3ee98fe48da1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091436"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importando volumes copiados de sombra transportável

Às vezes, é desejável criar uma cópia de sombra em um sistema, mas usar a cópia de sombra em um segundo sistema.

Considere o caso em que os dados de backup são normalmente gerenciados por um determinado sistema (*systemOne*) durante operações normais e que esses dados são armazenados fisicamente em uma matriz de armazenamento ou um dispositivo.

Para minimizar qualquer interrupção em *systemOne* (como as operações de backup podem consumir muitos recursos), é desejável executar o backup usando o *systemTwo*, um servidor de backup, que tem acesso à mesma matriz de armazenamento que *systemOne*.

Para garantir uma cópia de sombra adequada — cooperar com os gravadores no *systemOne* e preservar o estado adequadamente para tarefas em andamento — a cópia de sombra deve ser executada pelo *systemOne*.

Portanto, *systemOne* deve criar uma [*cópia de sombra transportável*](vssgloss-t.md), que *systemTwo* será importada.

**Windows server 2003, Standard Edition, Windows server 2003, Web Edition e Windows XP:** Não há suporte para conjuntos de cópia de sombra transportáveis. Todas as edições do Windows Server 2003 com Service Pack 1 (SP1) oferecem suporte a conjuntos de cópia de sombra transportáveis.

Um exemplo típico de importação de uma cópia de sombra transportável pode proceder da seguinte maneira:

1.  Inicialmente, a LUN (unidade lógica) fornecida pela matriz de armazenamento é montada como um volume em *systemOne* (digamos, F:).
2.  Um solicitante em execução em *systemOne* instancia uma instância de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e prossegue como se estivesse se preparando para um backup. (Consulte [visão geral da inicialização de backup](overview-of-backup-initialization.md), [visão geral da fase de descoberta de backup](overview-of-the-backup-discovery-phase.md)e [visão geral de tarefas de pré-backup](overview-of-pre-backup-tasks.md) para obter mais informações.)
3.  O solicitante em *systemOne* modifica o contexto de cópia de sombra que normalmente é usado para a operação de backup local (**\_ backup de \_ aplicativo \_ do VSS CTX**) para indicar que uma cópia de sombra transportável será criada (**VSS \_ VOLSNAP \_ attr \_ transportável**). O atributo transportável também pode ser adicionado a outros contextos de cópia de sombra.
4.  Com um contexto de cópia de sombra do VSS CTX o VSS de **\_ \_ \_ backup de aplicativo do VSS** de não \| **\_ \_ \_ Transportable**, o solicitante que está no *systemOne* cria uma cópia de sombra chamando [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).
5.  *SystemOne* usa [**IVssBackupComponents:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) para salvar o estado atual do documento de componentes de backup e [**IVssExamineWriterMetadata:: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) para salvar os documentos de metadados do gravador de cada gravador. As cadeias de caracteres XML que contêm esses documentos são disponibilizadas para um solicitante em execução no *systemTwo*.

    O solicitante transfere o documento de componentes de backup para *systemTwo*.

    Observe que o solicitante em *systemOne* não libera sua instância de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) neste ponto se a finalidade da cópia de sombra for backup. A interface deve permanecer aberta até que o *systemTwo* conclua com êxito suas operações de backup. Somente o solicitante deve emitir um evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , uma vez que alguns gravadores truncarão logs e farão outro trabalho após um backup bem-sucedido. Se a meta da cópia de sombra for Data Mining ou outras finalidades, a interface poderá ser fechada nesta etapa.

6.  O solicitante em *systemTwo* então chama [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) para obter acesso à cópia de sombra que foi criada pelo solicitante no *systemOne*.
    > [!Note]  
    > O solicitante é responsável por serializar a operação de cópia de sombra de importação. Além disso, se a chamada para [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) falhar, o VSS não limpará os LUNs sozinhos. O solicitante precisa iniciar a limpeza de LUNs.

     

7.  O solicitante em *systemTwo* prossegue com o backup do material copiado de sombra exatamente como se estivesse fazendo backup de uma cópia de sombra criada por si só (consulte [visão geral do backup real de arquivos](overview-of-actual-backup-of-files.md)).

    O solicitante em *systemTwo* Obtém o [*objeto de dispositivo*](vssgloss-d.md) da cópia de sombra usando [**IVssBackupComponents:: getsnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) na cópia de sombra importada e acrescenta isso ao início dos caminhos de arquivo originais que foram obtidos dos metadados para acessar os arquivos cujo backup será feito.

8.  Depois de usar a cópia de sombra, o solicitante em *systemTwo* deve excluir a cópia de sombra. Assim como ocorre com cópias de sombra não transportáveis, se o contexto de cópia de sombra indicar cópias de sombra de liberação automática (por exemplo, **\_ \_ backup CTX VSS**), a liberação do [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) no *systemTwo* fará com que o serviço VSS exclua a cópia de sombra. Caso contrário, se o contexto indicar uma cópia de sombra persistente (por exemplo, a **\_ \_ \_ reversão do aplicativo VSS CTX**), o solicitante em *systemTwo* deverá excluir explicitamente a cópia de sombra.

    Em seguida, o solicitante em *systemTwo* sinaliza o solicitante no *systemOne* que ele concluiu com o backup da cópia de sombra transportável.

9.  Depois que o solicitante no *systemOne* recebeu uma notificação de que o solicitante no *systemTwo* concluiu o backup da cópia de sombra transportável, ele notifica os gravadores em seu sistema gerando um evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) com uma chamada para **IVssBackupComponents:: BackupComplete**. Neste ponto, o solicitante no *systemOne* é gratuito para liberar sua instância do [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

**Cópias de sombra transportáveis em um cluster:** As cópias de sombra transportáveis devem ser importadas de fora do cluster, contanto que o volume original seja montado no cluster. Para obter informações sobre como implementar uma recuperação rápida em um cluster, consulte [recuperação rápida usando volumes copiados de sombra transportável](fast-recovery-using-transportable-shadow-copied-volumes.md).

 

 



