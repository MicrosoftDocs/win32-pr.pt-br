---
description: Ao inicializar uma operação de restauração do VSS, um solicitante precisa recuperar o Documento do Componente de Backup e cada Documento de Metadados do Writer relevante criado e salvo durante a operação de backup.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Visão geral da inicialização de restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c531e4b47c49e5bd5538ea30583a31273bb6645a445ef1b1ea851bac539411c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751685"
---
# <a name="overview-of-restore-initialization"></a>Visão geral da inicialização de restauração

Ao inicializar uma operação de restauração do VSS, um solicitante precisa recuperar o Documento do Componente de Backup e cada Documento de Metadados do Writer relevante criado e salvo durante a operação de backup. O autor terá seu estado atual consultado ao manipular o evento [*Identificar*](vssgloss-i.md) que o solicitante gera. Para obter mais informações, consulte [Visão geral do processamento de uma restauração no VSS.](overview-of-processing-a-restore-under-vss.md)

A tabela a seguir mostra a sequência de ações e eventos necessários para inicializar uma operação de restauração.



| Ação do solicitante                                                                                                                                                                                                                                                                                                       | Evento                                                     | Ação do autor                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crie uma interface [**IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) inicialize-a para gerenciar uma restauração e carregar metadados armazenados do solicitante (consulte [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)). | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                                                                                      |
| Chame [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para criar interfaces [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) e carregá-las com metadados de writer armazenados.                                                                                                           | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                                                                                      |
| Iniciar contato assíncrono com os autores (consulte [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).)                                                                                                                                                                      | [*Identificar*](vssgloss-i.md) | O autor inicia a manipulação de eventos para dar suporte à restauração. Cria o documento de metadados do autor (consulte Trabalhando com o documento de metadados do autor [,](working-with-the-writer-metadata-document.md) [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| O solicitante aguarda a inicialização dos autores chamando [**IVssAsync.**](/windows/desktop/api/Vss/nn-vss-ivssasync)                                                                                                                                                                                                                               | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Ações do solicitante durante a inicialização de restauração

Durante a fase de inicialização de uma restauração, o solicitante precisa ter acesso ao Documento de Componentes de Backup armazenados e a todos os Documentos de Metadados do Autor.

Dependendo da implementação, isso significa que o solicitante exigirá que a mídia de backup seja montada e acessível ou que algum outro mecanismo para acessar os metadados armazenados estará disponível.

O solicitante usa o documento XML armazenado que contém o Documento de Componentes de Backup do solicitante que realizou o backup para inicializar seu Documento de Componentes de Backup usando [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) pode acessar as informações.

Como foi o caso durante o backup, o Documento de Componentes de Backup tem informações insuficientes para dar suporte a uma restauração; portanto, o solicitante precisa de acesso a esses Documentos de Metadados do Writer armazenados durante o backup (consulte [Uso de componentes pelo solicitante](use-of-components-by-the-requestor.md)).

O solicitante recupera os metadados armazenados do autor chamando [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para cada autor cujos dados foram armazenados em backup e agora devem ser restaurados. Essa função cria um [**objeto IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para cada autor e carrega o Documento de Metadados do Autor do autor no objeto .

Como foi o caso durante o backup, para iniciar a cooperação entre [](vssgloss-i.md) si e os autores do sistema, um solicitante deve gerar um evento Identify chamando [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Não é necessário chamar [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) após a conclusão de [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Os autores que [](vssgloss-i.md) não processarem o evento Identificar não serão incluídos na lista de autores que fornecerão os metadados a serem retornados por [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte [Determining Writer Status](determining-writer-status.md)).

Assim como ocorre com a operação de backup, um solicitante precisará consultar e analisar as informações no Documento de Componentes de Backup e compará-las aos dados nos Documentos de Metadados do Writer para determinar quais componentes foram backup e escolher os componentes a serem restaurados (consulte Visão geral de Preparação para [restauração).](overview-of-preparing-for-restore.md) Além disso, o solicitante precisará gerar uma lista detalhada contendo informações sobre os arquivos na mídia de backup selecionada para restauração, bem como como e onde eles devem ser restaurados. (Consulte [Gerando um conjunto de restauração](generating-a-restore-set.md).)

Portanto, alguns aplicativos de backup podem achar útil ter armazenado na mídia de backup sua própria lista (em seu próprio formato otimizado) dos arquivos e suas informações associadas de writer, component, restore procedure e location. Essa lista pode ser usada para minimizar a quantidade de análise e comparação de Documentos de Metadados do Writer e os Documentos de Componente de Backup necessários para dar suporte a uma restauração.

## <a name="writer-actions-during-restore-initialization"></a>Ações de writer durante a inicialização de restauração

Assim como é feito durante uma operação de restauração, em resposta ao evento Identificar, o VSS chama o método de manipulador virtual de cada autor [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify).

Observe que aplicativos diferentes do solicitante atual (por exemplo, aplicativos do sistema) podem gerar eventos de Identificação, que devem ser manipulados pelo autor. Além disso, não há como um autor determinar de dentro [**de CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qual aplicativo gerou o evento Identify.

Considerando que um autor pode receber vários Eventos de identificação durante o processamento de uma operação de restauração, os autores nunca devem definir informações de estado no manipulador [**CVssWriter::OnIdentify.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) Em vez disso, eles devem usar o mesmo algoritmo para criar o documento de metadados do Writer como foi feito durante as operações de backup (consulte Ações de writer durante a inicialização [de backup](overview-of-backup-initialization.md) para obter mais informações).

 

 



