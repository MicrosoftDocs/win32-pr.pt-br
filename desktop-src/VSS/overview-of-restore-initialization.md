---
description: Ao inicializar uma operação de restauração do VSS, um solicitante precisa recuperar o documento do componente de backup e cada documento de metadados do gravador relevante criado e salvo durante a operação de backup.
ms.assetid: 0a087125-c9d4-460a-8153-3e2e26633ac2
title: Visão geral da inicialização da restauração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb62e5282a74e38cd53d36c8ba004f4b8069746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091431"
---
# <a name="overview-of-restore-initialization"></a>Visão geral da inicialização da restauração

Ao inicializar uma operação de restauração do VSS, um solicitante precisa recuperar o documento do componente de backup e cada documento de metadados do gravador relevante criado e salvo durante a operação de backup. O gravador terá seu estado atual consultado na manipulação do [*evento de identificação*](vssgloss-i.md) que o solicitante gera. Para obter mais informações, consulte [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md).

A tabela a seguir mostra a sequência de ações e eventos necessários para inicializar uma operação de restauração.



| Ação do solicitante                                                                                                                                                                                                                                                                                                       | Evento                                                     | Ação do gravador                                                                                                                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Crie uma interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , inicialize-a para gerenciar uma restauração e carregue os metadados do solicitante armazenado (consulte [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents), [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore)). | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                                                                                      |
| Chame [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para criar interfaces [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) e carregá-las com metadados de gravador armazenados.                                                                                                           | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                                                                                      |
| Inicie o contato assíncrono com gravadores (consulte [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).)                                                                                                                                                                      | [*Identificar*](vssgloss-i.md) | O gravador inicia o tratamento de eventos para dar suporte à restauração. Cria o documento de metadados do gravador (consulte [trabalhando com o documento de metadados do gravador](working-with-the-writer-metadata-document.md), [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify), [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)). |
| O solicitante aguarda que os gravadores sejam inicializados chamando [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync).                                                                                                                                                                                                                               | Nenhum                                                      | Nenhum                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requester-actions-during-restore-initialization"></a>Ações do solicitante durante a inicialização da restauração

Durante a fase de inicialização de uma restauração, o solicitante precisa ter acesso ao documento de componentes de backup armazenados e a todos os documentos de metadados do gravador.

Dependendo da implementação, isso significa que o solicitante exigirá que a mídia de backup seja montada e legível, ou que algum outro mecanismo para acessar os metadados armazenados esteja disponível.

O solicitante usa o documento XML armazenado que contém o documento de componentes de backup do solicitante que realizou o backup para inicializar seu documento de componentes de backup usando [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) pode acessar as informações.

Como foi o caso durante o backup, o documento de componentes de backup não tem informações suficientes para dar suporte a uma restauração; Portanto, o solicitante precisa acessar os documentos de metadados do gravador armazenados durante o backup (consulte [uso de componentes pelo solicitante](use-of-components-by-the-requestor.md)).

O solicitante recupera os metadados do gravador armazenado chamando [**CreateVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) para cada gravador cujos dados foram armazenados em backup e agora deve ser restaurado. Essa função cria um objeto [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para cada gravador e carrega o documento de metadados do gravador do gravador no objeto.

Como foi o caso durante o backup, para iniciar a cooperação entre si mesmo e os gravadores do sistema, um solicitante deve gerar um evento de [*identificação*](vssgloss-i.md) chamando [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Não é necessário chamar [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) após a conclusão de [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata). Os gravadores que não processarem o evento de [*identificação*](vssgloss-i.md) não serão incluídos na lista de gravadores que fornecem os metadados a serem retornados por [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte [determinando o status do gravador](determining-writer-status.md)).

Assim como acontece com a operação de backup, um solicitante precisará consultar e analisar as informações no documento componentes de backup e compará-las aos dados nos documentos de metadados do gravador para determinar quais componentes foram armazenados em backup e escolher aqueles a serem restaurados (consulte [visão geral da preparação para a restauração](overview-of-preparing-for-restore.md)). Além disso, o solicitante precisará gerar uma lista detalhada contendo informações sobre os arquivos na mídia de backup selecionada para restauração, além de como e onde eles devem ser restaurados. (Consulte [gerando um conjunto de restauração](generating-a-restore-set.md).)

Portanto, alguns aplicativos de backup podem achar útil armazenar na mídia de backup sua própria lista (em seu próprio formato otimizado) dos arquivos e suas informações de gravador, componente, procedimento de restauração e local associadas. Essa lista pode ser usada para minimizar a quantidade de análise e comparação de documentos de metadados do gravador e os documentos do componente de backup necessários para dar suporte a uma restauração.

## <a name="writer-actions-during-restore-initialization"></a>Ações do gravador durante a inicialização da restauração

Assim como é feito durante uma operação de restauração, em resposta ao evento de identificação, o VSS chama o método de manipulador virtual de cada gravador [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify).

Observe que os aplicativos que não sejam o solicitante atual (por exemplo, aplicativos de sistema) podem gerar eventos de identificação, que devem ser manipulados pelo gravador. Além disso, não há nenhuma maneira de um gravador determinar de dentro de [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) qual aplicativo gerou o evento de identificação.

Considerando que um gravador pode receber vários eventos de identificação durante o processamento de uma operação de restauração, os gravadores nunca devem definir informações de estado no manipulador [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) . Em vez disso, eles devem usar o mesmo algoritmo para criar o documento de metadados do gravador como foi feito durante as operações de backup (consulte as [ações do gravador durante a inicialização do backup](overview-of-backup-initialization.md) para obter mais informações).

 

 



