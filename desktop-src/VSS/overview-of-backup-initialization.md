---
description: Essa fase do backup inicializa o autor e o solicitante, preenchendo suas estruturas de dados internas, especificando o backup e estabelece a comunicação do autor/solicitante por meio da chamada necessária para IVssBackupComponents::GatherWriterMetadata. Para obter mais informações, consulte Visão geral do processamento de um backup no VSS.
ms.assetid: 1fc46062-c4a0-4aa2-ae05-3d7cded18584
title: Visão geral da inicialização de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4054dc644056100a4db28ea11b6dcaf9c358084a1b01b9ad28c13e14133fc5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591350"
---
# <a name="overview-of-backup-initialization"></a>Visão geral da inicialização de backup

Esta fase do backup inicializa o autor e o solicitante, preenchendo suas estruturas de dados internas, especificando o backup e estabelece a comunicação do autor/solicitante por meio da chamada necessária para [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Para obter mais informações, consulte [Visão geral do processamento de um backup no VSS.](overview-of-processing-a-backup-under-vss.md)

A tabela a seguir mostra a sequência de ações e eventos necessários para inicialização de backup.



| Ação do solicitante                                                                                                                                                                                                                                                                                                                            | Evento                                                     | Ação do autor                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cria uma interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e a inicializa para gerenciar um backup (consulte [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup)) e, opcionalmente, habilitar ou desabilitar os autores no sistema. | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                       |
| Opcionalmente, de definir o contexto para operações de cópia de sombra e, opcionalmente, consultar o sistema sobre os provedores e cópias de sombra com suporte (consulte [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)).                                               | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                       |
| O solicitante pode fornecer informações adicionais sobre como lidar com operações de backup e restauração (consulte [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate))                                                                                                                                                        | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                       |
| Inicia o contato assíncrono com os autores (consulte [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata))                                                                                                                                                                                           | [*Identificar*](vssgloss-i.md) | Cria um documento de metadados de autor (consulte Trabalhando com o documento de metadados do autor [,](working-with-the-writer-metadata-document.md) [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)) |



 

## <a name="requester-actions-during-backup-initialization"></a>Ações do solicitante durante a inicialização de backup

Um [**objeto IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pode ser usado para apenas um backup. Portanto, um solicitante deve prosseguir até o final do backup, incluindo a liberação da interface **IVssBackupComponents.** Se o backup precisar ser encerrado prematuramente, o solicitante precisará chamar [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e, em seguida, liberar o objeto **IVssBackupComponents** (consulte Anulando operações [vss](aborting-vss-operations.md) para obter mais informações). Não tente retomar a interface **IVssBackupComponents.**

Normalmente, o Documento de Componentes de Backup de um solicitante é inicializado como vazio. Um Documento de Componentes de Backup armazenado pode ser carregado quando [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) é chamado, normalmente em suporte a volumes copiados de sombra transportáveis. Nesse caso, a comunicação do autor-solicitante será um pouco diferente da descrita abaixo. (Consulte [Importando volumes copiados de sombra transportáveis](importing-transportable-shadow-copied-volumes.md) para obter mais informações.)

Para adicionar volumes ao conjunto de cópias de sombra, um solicitante deve primeiro definir o contexto para a operação de cópia de sombra chamando [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext). Se esse método não for chamado, o contexto padrão para cópias de sombra, \_ VSS CTX \_ BACKUP, será usado. Para obter informações sobre como definir o contexto de cópia de sombra, consulte [Configurações de contexto de cópia de sombra.](shadow-copy-context-configurations.md)

Para iniciar a conclusão de sua configuração antes do backup, um solicitante deve chamar [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Ao fazer isso, um solicitante indica aos autores:

-   O tipo de backup (conforme definido em [**VSS \_ BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type))
-   Se o backup inclui um estado inicializável do sistema
-   Se o solicitante dá suporte à seleção de componentes individuais ou faz o back-up de volumes inteiros.

Todos os solicitantes que participam das operações de backup e restauração sempre devem chamar [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Esse método inicia a comunicação do autor-solicitante gerando um evento VSS [*Identify,*](vssgloss-i.md) em resposta ao qual um autor cria seu documento de metadados.

Antes de chamar [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), um solicitante tem a oportunidade de habilitar ou desabilitar explicitamente determinados editores e classes de autor específicos usando [**IVssBackupComponents::EnableWriterClasses,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses) [**IVssBackupComponents::D isableWriterInstances**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances)e [**IVssBackupComponents::D isableWriterClasses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses) (por padrão, todas as classes são habilitadas). Depois **que IVssBackupComponents::GatherWriterMetadata** for chamado, essas chamadas não terão nenhum efeito.

Como não há nenhuma maneira de obter uma lista de autores no sistema antes de chamar [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), os solicitantes podem considerar a criação e a exclusão de uma segunda instância [**de IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) para obter a lista.

Não é necessário chamar [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) após a conclusão de [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Os autores que [](vssgloss-i.md) não processarem o evento Identificar gerado pelas chamadas não fazem parte da lista de autores que fornece metadados encontrados por [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte Determinando o status do [autor).](determining-writer-status.md)

## <a name="writer-actions-during-backup-initialization"></a>Ações de writer durante a inicialização de backup

Em resposta ao evento Identify, o VSS chama o método de manipulador virtual de cada autor, [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Um autor cria seu Documento de Metadados do Writer substituindo a implementação padrão **de CVssWriter::OnIdentify** e usando a interface [**IVssCreateWriterMetadata.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)

Observe que aplicativos diferentes do solicitante atual (por exemplo, aplicativos do sistema) podem gerar Eventos de identificação que devem ser manipulados pelo autor. Além disso, não há como um autor determinar de dentro [**de CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qual aplicativo gerou o evento Identify.

Esse é o caso, considerando que um autor pode receber vários Eventos de identificação durante o processamento de uma operação de backup, um autor nunca deve definir informações de estado no manipulador [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)

Em vez disso, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) deve executar um algoritmo consistente para criar o Documento de Metadados do Autor do autor, especialmente porque, depois que um autor cria o documento, nem o solicitante nem o autor podem modificá-lo. Desse ponto em diante, é um documento somente leitura.

Isso significa que o [](vssgloss-c.md) número e o tipo de componentes associados a um autor, quais arquivos fazem parte de cada componente, e a exclusão explícita de arquivos de operações de backup ou restauração não pode ser alterada depois que um autor retorna do processamento do evento Identificar.

Todos os autores que participam do VSS precisam fazer o seguinte:

1.  Indique um método de restauração para todos os componentes gerenciados pelo autor usando [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
2.  Adicione pelo menos um componente usando [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) (consulte Definição de componentes por [autores](definition-of-components-by-writers.md) para obter mais informações sobre a especificação do componente).

Um autor indica os arquivos para participar de uma operação de backup ou restauração adicionando conjuntos de arquivos [*–*](vssgloss-f.md)uma combinação de um caminho, especificação de arquivo e um sinalizador de recursão – a um determinado componente usando [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata::AddDatabaseLogFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)dependendo do tipo (Consulte Adicionando arquivos aos componentes [.)](definition-of-components-by-writers.md)

Um autor também pode ter um ou mais componentes vazios, componentes aos quais nenhum arquivo foi adicionado. Eles são muito úteis para organizar os componentes do autor. (Consulte [Caminho lógico de componentes](logical-pathing-of-components.md).)

Um autor usa [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles) para impedir explicitamente que os arquivos são incluídos no backup. Essa exclusão explícita é útil porque caracteres curinga podem ser usados para especificar arquivos para inclusão (consulte [Excluir especificação de lista de arquivos](writer-metadata-document-contents.md)). Observe que a lista de arquivos de exclusão tem precedência sobre listas de arquivos de componente.

[**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) é usado para criar mapeamentos de localização alternativos para conjuntos de arquivos especificados que foram adicionados a um dos [*componentes*](vssgloss-a.md) do autor. Esses mapeamentos são usados durante a restauração de arquivo ao restaurar para o local original de um arquivo não é possível ou desejável. (Consulte Visão [geral da restauração de arquivo real](overview-of-actual-file-restoration.md) e locais de backup e restauração não [padrão](non-default-backup-and-restore-locations.md).)

Como o conjunto de arquivos de backup é especificado no Documento de Metadados do Writer, ele não pode ser modificado posteriormente. Portanto, um autor deve ser codificado para que a definição do conjunto de arquivos inclua todos os arquivos necessários no backup, seja por nome ou por meio de caracteres curinga. De forma concebível, isso pode incluir alguns arquivos que podem ser criados após o evento Identificar.

 

 



