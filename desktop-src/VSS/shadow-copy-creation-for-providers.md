---
description: Criação de cópia de sombra para provedores
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Criação de cópia de sombra para provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cc7306e7a13ef8e96ab032016a922411a70f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010848"
---
# <a name="shadow-copy-creation-for-providers"></a>Criação de cópia de sombra para provedores

## <a name="the-shadow-copy-creation-process"></a>O processo de criação de cópia de sombra

Um solicitante é o aplicativo que inicia a solicitação para criar uma cópia de sombra. Normalmente, o solicitante é um aplicativo de backup. Se necessário, o VSS chamará os provedores envolvidos. A maioria dos provedores está interessada em três solicitações específicas do solicitante.

1.  O solicitante inicia a atividade de criação de cópia de sombra com uma chamada para [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Isso gera um **GUID** do tipo **\_ ID do VSS** que identifica exclusivamente esse conjunto de cópias de sombra específico – o SnapshotSetId. O provedor não está envolvido nesta etapa, mas o SnapshotSetId é usado extensivamente em todas as etapas subsequentes.
2.  Para cada volume que deseja incluir nesse conjunto de cópia de sombra, o solicitante chama [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). O VSS determina qual provedor será usado para copiar a sombra do volume.
    -   Vários provedores podem participar de um conjunto de cópias de sombra. Por exemplo, se o volume do sistema e um volume de dados fizerem parte do mesmo conjunto de cópias de sombra, o provedor do sistema poderá servir como o provedor de cópia de sombra para o volume do sistema, enquanto um provedor de hardware pode servir como o provedor de cópia de sombra para o volume de dados. Ambos os provedores fazem parte do mesmo conjunto de cópias de sombra e o usuário esperaria a mesma consistência pontual em ambos os volumes.
    -   Para que um provedor de hardware seja selecionado, o provedor de hardware deve ser capaz de dar suporte a todos os LUNs que contribuem para o volume especificado.
    -   Todos os provedores registrados têm a oportunidade de indicar o suporte para um determinado volume durante a criação da cópia de sombra. Se mais de um provedor indicar suporte, o VSS primeiro usará como padrão os provedores de hardware, os provedores de software e, por fim, o provedor do sistema (se nenhum outro provedor indicar suporte para esse volume).
    -   Um solicitante pode substituir essa ordem padrão indicando explicitamente o provedor necessário para criar a cópia de sombra.
    -   Se houver vários provedores de hardware que dão suporte a um determinado volume, não haverá garantia para a ordem em que os provedores de hardware serão chamados.
3.  Após uma ou mais chamadas para [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), o solicitante pode solicitar que a cópia de sombra seja criada usando o método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) . Em seguida, o VSS funciona com o sistema para criar a cópia de sombra. O método **DoSnapshotSet** executa esse trabalho de forma assíncrona e o solicitante pode sondar ou aguardar a conclusão do processo de criação de cópia de sombra.

Este diagrama mostra as interações entre o solicitante, o serviço VSS, o suporte ao kernel do VSS, quaisquer gravadores VSS envolvidos e quaisquer provedores de hardware VSS. Consulte [o processo de criação de cópia de sombra](the-shadow-copy-creation-process.md) para obter uma descrição detalhada dessas interações.

![interações entre o solicitante, os componentes de backup, os gravadores e os provedores](images/vssimpl.png)

Quando o processo de criação de cópia de sombra é concluído, o solicitante pode determinar se a criação da cópia de sombra foi bem-sucedida e, se não, determinar a origem da falha.

O intervalo de tempo entre o congelamento e descongelamento dos aplicativos do gravador deve ser minimizado. O provedor deve iniciar de forma assíncrona todo o trabalho de preparação relacionado à cópia de sombra (como um provedor de hardware que usa plexes que iniciam a sincronização) no método [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) e aguardar as conclusões no método [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) .

Há várias janelas de limite de tempo que os provedores devem seguir. Como resultado, os provedores bem comprovados executarão todo o processamento desnecessário antes de [**IVssProviderCreateSnapshotSet::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) e depois de [**IVssProviderCreateSnapshotSet::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

O conjunto de cópias de sombra é fixo quando [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) é chamado. Volumes adicionais não podem ser adicionados mais tarde porque os volumes adicionais não compartilham o mesmo ponto no tempo.

Há um limite de 64 volumes no conjunto de cópias de sombra. Um volume específico pode ser mapeado para um LUN inteiro, uma parte de um LUN ou partes de vários LUNs. A maioria das configurações terá um volume por LUN, embora sejam possíveis mapeamentos arbitrários.

Não há limite para o número de conjuntos de cópias de sombra ou o número de conjuntos de cópias de sombra de um volume original. Um provedor pode definir limites específicos ou limitar dinamicamente com base nos recursos de hardware disponíveis.

### <a name="point-in-time-for-writerless-applications"></a>Ponto no tempo para aplicativos não gravados

O VSS inclui suporte especial que define o ponto no tempo que é comum para todos os volumes em um conjunto de cópias de sombra. Os provedores de hardware não precisam interagir diretamente com essas tecnologias de kernel, pois são invocados como parte do processamento normal de confirmação de cópia de sombra. No entanto, é útil entender os mecanismos usados porque explica a definição de "pontual" para aplicativos sem gravação (aplicativos que não apresentaram uma interface de gravador VSS e, portanto, não participam do processo de criação de cópias de sombra de volume.)

Esse suporte ao kernel do VSS para um ponto no tempo comum é distribuído entre o driver VolSnap.sys, os sistemas de arquivos e o VSS.

1.  Antes que o suporte ao kernel do VSS seja invocado, o VSS já tem:
    1.  Determinado quais volumes devem ser envolvidos na cópia de sombra.
    2.  Determinado qual provedor deve ser usado em cada volume.
    3.  Aplicativos congelado que estão aceitando congelar/descongelar mensagens.
    4.  Preparados os provedores para a cópia de sombra chamando os métodos [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) . Todos os provedores estão agora aguardando para fazer a criação da cópia de sombra real.
2.  Em seguida, o ponto no tempo é criado. O VSS libera simultaneamente os sistemas de arquivos em todos os volumes que devem ser copiados em sombra.
    1.  O VSS emite um \_ \_ comando de \_ controle flush e Hold de gravação do IOCTL \_ \_ em cada volume que libera os sistemas de arquivos. Esse IOCTL é passado para baixo na pilha de armazenamento para VolSnap.sys. Em seguida, VolSnap.sys mantém todas as gravações IRPs até a etapa 4 abaixo. Qualquer sistema de arquivos (como RAW) sem suporte para esse novo IOCTL passa o IOCTL desconhecido para baixo, onde ele é mantido novamente por VolSnap.sys. Em volumes NTFS, a liberação também confirma o log NTFS.
    2.  Isso suspende toda a atividade de metadados NTFS/FAT; os metadados do sistema de arquivos são confirmados corretamente.
    3.  A cópia de sombra instantânea: VolSnap.sys faz com que todas as gravações subsequentes IRPs sejam enfileiradas em todos os volumes que devem ser copiados em sombra.
    4.  VolSnap.sys aguarda que todas as gravações pendentes nos volumes de sombra copiados sejam concluídas. Os volumes agora estão inativos em relação às gravações e estavam inativos exatamente no mesmo momento em cada volume. Não há garantias sobre gravações em seções mapeadas do usuário ou gravações emitidas entre (a) e (b) em sistemas de arquivos que não implementam o IOCTL de liberação (por exemplo, RAW).
3.  O VSS instrui cada provedor a executar a cópia de sombra chamando os métodos [**IVssProviderCreateSnapshotSet:: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . Os provedores devem ter toda a preparação feita para que essa seja uma operação rápida.

    Observe que o sistema de e/s só é inativo enquanto esses métodos [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) estão em execução. Se um provedor executar qualquer sincronização dos LUNs de cópia de sombra e de origem, essa sincronização deverá ser concluída antes que o método **CommitSnapshots** do provedor seja retornado. Ele não pode ser executado de forma assíncrona.

4.  Imediatamente após o método [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) do último provedor retornar, o VSS libera Todas as gravações pendentes IRPs (incluindo a IRPs que estava bloqueando os sistemas de arquivos na conclusão de seus caminhos de confirmação) invocando outro IRP passado para VolSnap.sys.
5.  Se o processo de cópia de sombra tiver sido bem-sucedido, o VSS agora:
    1.  Chama [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) para os provedores envolvidos.
    2.  Chama [**CVssWriter:: descongelar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) para os gravadores envolvidos.
    3.  Informa ao solicitante que o processo de cópia de sombra foi concluído.

[**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), para [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) são críticos o tempo todo. Todas as e/s de aplicativos com gravadores são congeladas de **PreCommitSnapshots** para **PostCommitSnapshots**; os atrasos afetam a disponibilidade do aplicativo. Todas as e/s de arquivo, incluindo e/s de aplicativo não gravado, são suspensas durante a **CommitSnapshots**.

Os provedores devem concluir todo o trabalho de tempo crítico antes de retornar de [**EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots).

-   [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) deve ser retornado em segundos. A fase **CommitSnapshots** está localizada na janela liberar e manter. O suporte ao kernel do VSS cancelará a liberação e a suspensão que está mantendo a e/s se a versão subsequente não for recebida em até 10 segundos e o VSS falhará no processo de criação da cópia de sombra. Outras atividades ocorrerão no sistema, portanto, um provedor não deve contar com 10 segundos inteiros. O provedor não deve chamar as APIs do Win32 durante a confirmação, pois muitas resultarão em gravações e bloqueios inesperados. Se o provedor levar mais de alguns segundos para concluir a chamada, haverá uma alta probabilidade de que isso falhará.
-   A sequência completa de [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) para o retorno de [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) mapeia para a janela entre os gravadores que recebem os eventos Freeze e descongelar. O padrão do gravador para esta janela é de 60 segundos, mas um gravador pode substituir esse valor por um tempo limite menor. Por exemplo, o gravador do Microsoft Exchange Server altera o tempo limite para 20 segundos. Os provedores não devem passar mais de um segundo ou dois nesse método.

Durante a [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) , o provedor deve evitar qualquer e/s de arquivo que não seja de paginação; Essa e/s tem uma probabilidade muito alta de deadlocks. Em particular, o provedor não deve gravar de forma síncrona nenhum log de depuração ou de rastreamento.

 

 



