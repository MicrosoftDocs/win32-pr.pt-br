---
description: 'Esse estágio do backup Inicializa o gravador e o solicitante, preenchendo suas estruturas de dados internas, especificando o backup e estabelece a comunicação do gravador/solicitante por meio da chamada necessária para IVssBackupComponents:: GatherWriterMetadata. Para obter mais informações, consulte Visão geral do processamento de um backup em VSS.'
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Visão geral da inicialização do backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fb97b43cf19ca60e3e4601899700e35bdad3aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784945"
---
# <a name="overview-of-backup-initialization"></a>Visão geral da inicialização do backup

Esse estágio do backup Inicializa o gravador e o solicitante, preenchendo suas estruturas de dados internas, especificando o backup e estabelece a comunicação do gravador/solicitante por meio da chamada necessária para [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Para obter mais informações, consulte [visão geral do processamento de um backup em VSS](overview-of-processing-a-backup-under-vss.md).

A tabela a seguir mostra a sequência de ações e eventos que são necessários para a inicialização do backup.



| Ação do solicitante                                                                                                                                                                                                                                                                                                                            | Evento                                                     | Ação do gravador                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cria uma interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e a inicializa para gerenciar um backup (consulte [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) e, opcionalmente, habilitar ou desabilitar gravadores no sistema. | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                       |
| Opcionalmente, defina o contexto para operações de cópia de sombra e, opcionalmente, consulte o sistema sobre os provedores e as cópias de sombra com suporte (Confira [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                       |
| O solicitante pode fornecer informações adicionais sobre como lidar com operações de backup e restauração (consulte [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate))                                                                                                                                                        | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                       |
| Inicia o contato assíncrono com gravadores (consulte [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                           | [*Identificar*](vssgloss-i.md) | Cria um documento de metadados do gravador (consulte [trabalhando com o documento de metadados do gravador](working-with-the-writer-metadata-document.md), [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Ações do solicitante durante a inicialização do backup

Um objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pode ser usado somente para um backup. Portanto, um solicitante deve prosseguir até o final do backup, incluindo a liberação da interface **IVssBackupComponents** . Se o backup precisar ser encerrado prematuramente, o solicitante precisará chamar [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e, em seguida, liberar o objeto **IVssBackupComponents** (consulte [anulando operações do VSS](aborting-vss-operations.md) para obter mais informações). Não tente retomar a interface **IVssBackupComponents** .

Normalmente, o documento de componentes de backup de um solicitante é inicializado como vazio. Um documento de componentes de backup armazenados pode ser carregado quando [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) é chamado, normalmente em suporte a volumes copiados de sombra transportável. Nesse caso, a comunicação do gravador-solicitante será um pouco diferente do que está descrito abaixo. (Consulte [importação de volumes copiados de sombra transportável](importing-transportable-shadow-copied-volumes.md) para obter mais informações.)

Para adicionar volumes ao conjunto de cópias de sombra, um solicitante deve primeiro definir o contexto para a operação de cópia de sombra chamando [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Se esse método não for chamado, o contexto padrão para cópias de sombra, \_ backup do VSS CTX \_ , será usado. Para obter informações sobre como definir o contexto de cópia de sombra, consulte [configurações de contexto de cópia de sombra](shadow-copy-context-configurations.md).

Para começar a conclusão de sua configuração antes do backup, um solicitante deve chamar [**IVssBackupComponents:: Setbackupstate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Ao fazer isso, um solicitante indica aos gravadores:

-   O tipo de backup (conforme definido no [**\_ \_ tipo de backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Se o backup inclui um estado de sistema inicializável
-   Se o solicitante dá suporte à seleção de componentes individuais ou faz backup de volumes inteiros.

Todos os solicitantes que participam de operações de backup e restauração sempre devem chamar [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Esse método inicia a comunicação do gravador-solicitante gerando um evento de [*identificação*](vssgloss-i.md) do VSS, em resposta à qual um gravador cria seu documento de metadados.

Antes de chamar [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), um solicitante tem a oportunidade de habilitar ou desabilitar explicitamente certos gravadores e classes de gravador específicos usando [**IVssBackupComponents:: EnableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses), [**IVssBackupComponents::D Isablewriterinstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)e [**IVssBackupComponents::D isablewriterclasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (por padrão, todas as classes são habilitadas). Depois que **IVssBackupComponents:: GatherWriterMetadata** for chamado, essas chamadas não terão efeito.

Como não há nenhuma maneira de obter uma lista de gravadores no sistema antes de chamar [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), os solicitantes podem considerar a criação e a exclusão de uma segunda instância de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para obter a lista.

Não é necessário chamar [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) após a conclusão de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Os gravadores que não processarem o evento de [*identificação*](vssgloss-i.md) gerado pelas chamadas não serão parte da lista de gravadores que fornecem metadados encontrados por [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte [determinando o status do gravador](determining-writer-status.md)).

## <a name="writer-actions-during-backup-initialization"></a>Ações do gravador durante a inicialização do backup

Em resposta ao evento de identificação, o VSS chama o método de manipulador virtual de cada gravador, [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify). Um gravador cria seu documento de metadados do gravador substituindo a implementação padrão de **CVssWriter:: Onidentification** e usando a interface [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) .

Observe que os aplicativos que não sejam o solicitante atual (por exemplo, aplicativos de sistema) podem gerar eventos de identificação que devem ser manipulados pelo gravador. Além disso, não há nenhuma maneira de um gravador determinar de dentro de [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qual aplicativo gerou o evento de identificação.

Esse é o caso, uma vez que um gravador pode receber vários eventos de identificação durante o processamento de uma operação de backup, um gravador nunca deve definir informações de estado no manipulador [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) .

Em vez disso, [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) deve executar um algoritmo consistente para criar o documento de metadados do gravador do gravador, particularmente porque depois que um gravador cria o documento, nem o solicitante nem o gravador pode modificá-lo. Deste ponto em diante, ele é um documento somente leitura.

Isso significa que o número e o tipo de [*componentes*](vssgloss-c.md) associados a um gravador, quais arquivos fazem parte de cada componente, e a exclusão explícita de arquivos de operações de backup ou restauração não pode ser alterada depois que um gravador retorna do processamento do evento de identificação.

Todos os gravadores que participam do VSS são necessários para fazer o seguinte:

1.  Indique um método de restauração para todos os componentes gerenciados pelo gravador usando [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Adicione pelo menos um componente usando [**IVssCreateWriterMetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) (consulte [definição de componentes por gravadores](definition-of-components-by-writers.md) para obter mais informações sobre a especificação do componente).

Um gravador indica os arquivos para participar de uma operação de backup ou restauração adicionando [*conjuntos de arquivos*](vssgloss-f.md)— uma combinação de um caminho, uma especificação de arquivo e um sinalizador de recursão — a um determinado componente usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles), dependendo do tipo (consulte [Adicionando arquivos aos componentes](definition-of-components-by-writers.md).)

Um gravador também pode ter um ou mais componentes vazios, componentes para os quais nenhum arquivo foi adicionado. Eles são muito úteis para organizar os componentes do gravador. (Consulte o [caminho lógico dos componentes](logical-pathing-of-components.md).)

Um gravador usa [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) para impedir explicitamente que arquivos sejam incluídos no backup. Essa exclusão explícita é útil porque caracteres curinga podem ser usados para especificar arquivos para inclusão (consulte [excluir especificação de lista de arquivos](writer-metadata-document-contents.md)). Observe que a lista de arquivos de exclusão tem precedência sobre as listas de arquivos de componentes.

[**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) é usado para criar [*mapeamentos de local alternativos*](vssgloss-a.md) para os conjuntos de arquivos especificados que foram adicionados a um dos componentes do gravador. Esses mapeamentos são usados durante a restauração do arquivo quando a restauração para o local original de um arquivo não é possível ou desejável. (Consulte [visão geral de restauração de arquivo real](overview-of-actual-file-restoration.md) e [locais de backup e restauração não padrão](non-default-backup-and-restore-locations.md).)

Como o conjunto de arquivos de backup é especificado no documento de metadados do gravador, ele não pode ser modificado posteriormente. Portanto, um gravador deve ser codificado para que a definição do conjunto de arquivos inclua todos os arquivos necessários no backup, seja pelo nome ou por caracteres curinga. É muito provável que isso inclua alguns arquivos que podem ser criados após o evento de identificação.

 

 



