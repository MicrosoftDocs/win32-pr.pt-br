---
description: Há situações em que os dados de um autor dependem dos dados gerenciados por outro. Nesses casos, você deve fazer backup ou restaurar dados de ambos os autores.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dependências entre componentes gerenciados por diferentes autores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d50e88e13899951802b2ec3aa0bd9e651c16928b9f57409329035a28cfa1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122146"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dependências entre componentes gerenciados por diferentes autores

Há situações em que os dados de um autor dependem dos dados gerenciados por outro. Nesses casos, você deve fazer backup ou restaurar dados de ambos os autores.

O VSS lida com esse problema por meio da noção de uma dependência explícita de componente de autor e da interface [**IVssWMDependency.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

Um autor adiciona uma ou mais dependências ao criar o Documento de Metadados do Writer usando o método [**IVssCreateWriterMetadata::AddComponentDependency.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) O autor passa ao método o nome e o caminho lógico do componente dependente (que ele gerencia), bem como o nome e o caminho lógico e a [*ID*](vssgloss-w.md) da classe de autor (o GUID que identifica a classe) do componente do qual ele depende.

Depois de estabelecida, essa dependência informa ao solicitante que, durante qualquer operação de backup ou restauração, o componente dependente e os destinos de suas dependências devem participar.

Um determinado componente pode ter várias dependências, o que exige que ele e todos os seus destinos dependentes participem do backup e da restauração juntos.

O componente dependente e/ou os destinos de suas [](vssgloss-e.md) dependências podem ser incluídos explicitamente ou [*implicitamente*](vssgloss-i.md) em operações de backup ou restauração.

O mecanismo de dependência do componente de autor explícito não deve ser usado para criar uma dependência entre dois componentes no mesmo autor. As regras de seleção podem fornecer a mesma funcionalidade com mais eficiência sem o risco de dependências circulares.

Por exemplo, [**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) pode ser usado para definir a dependência do componente writerData (com o caminho lógico "") do autor MyWriter no componente internetData (com um caminho lógico de "Conexões") de um autor chamado InternetConnector com uma ID de Classe X de autor. (Embora seja possível que vários autores com a mesma ID de classe sejam simultaneamente no sistema, a confusão será evitada porque a combinação de caminho lógico e nome do componente é exclusiva no sistema no VSS.)

Um autor adiciona várias dependências a um determinado componente simplesmente chamando [**IVssCreateWriterMetadata::AddComponentDependency repetidas**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) com diferentes componentes de diferentes autores. O número de outros componentes dos que um determinado componente depende pode ser encontrado examinando o membro **cDependencies** da estrutura [**\_ COMPONENTINFO do VSS.**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)

Um autor ou solicitante recupera instâncias da interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) com [**IVssWMComponent::GetDependency.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency) O **IVssWMDependency** retorna o nome do componente, o caminho lógico e a ID de classe do autor que gerencia o componente que é o destino da dependência.

O mecanismo de dependência não determina nenhuma ordem específica de preferência entre o componente dependente e os destinos de suas dependências. Conforme indicado acima, todas as dependências indicam que sempre que um determinado componente é feito backup ou restaurado, o componente ou componente dos que ele depende também deve ser feito backup ou restaurado. A implementação exata da dependência está a critério do aplicativo de backup.

Por exemplo, no caso acima, o componente writerData (caminho lógico "") depende do componente InternetConnector (caminho lógico "Conexões"). Um solicitante é livre para interpretar isso de uma das seguintes maneiras:

-   Se o componente dependente, writerData, for selecionado (implicitamente ou explicitamente) para backup ou restauração, o solicitante deverá selecionar (implicitamente ou explicitamente) o destino de sua dependência, internetData
-   Se o destino de sua dependência, internetData, não estiver selecionado para backup, o componente dependente, writerData, não deverá ser selecionado.

No entanto, ao desenvolver suporte para dependências, os desenvolvedores de solicitantes devem estar cientes de que não há nenhuma maneira de um autor determinar se um de seus componentes é um destino de uma dependência.

## <a name="declaring-remote-dependencies"></a>Declarando dependências remotas

Um aplicativo distribuído é um aplicativo que pode ser configurado para usar um ou mais computadores por vez. Normalmente, o aplicativo é executado em um ou mais computadores do servidor de aplicativos e se comunica com (mas pode ou não ser executado em) um ou mais computadores de servidor de banco de dados. Às vezes, essa configuração é chamada de implantação de vários sistemas. Geralmente, o mesmo aplicativo também pode ser configurado para ser executado em um único computador que executa um servidor de aplicativos e um servidor de banco de dados. Essa configuração é chamada de implantação de sistema único. Em ambas as configurações, o servidor de aplicativos e o servidor de banco de dados têm seus próprios autores VSS independentes.

Em uma implantação de vários sistemas, se um componente gerenciado pelo autor do aplicativo depender de um componente remoto gerenciado pelo autor do servidor de banco de dados, isso será chamado de dependência remota. (Uma implantação de sistema único, por outro lado, tem apenas dependências locais.)

Como exemplo de uma implantação de vários sistemas, considere um servidor de aplicativos que usa um servidor SQL Server banco de dados como um armazenamento de dados. Os dados específicos do aplicativo, que incluem as web parts, os arquivos de conteúdo da Web e a metabase do IIS, residem em um ou mais computadores, chamados servidores Web de front-end. O armazenamento SQL dados real, que inclui o banco de dados config e vários bancos de dados de Conteúdo, reside em um ou mais computadores, chamados de servidores de banco de dados de back-end. Cada um dos servidores Web front-end contém o mesmo conteúdo e configuração específicos do aplicativo. Cada um dos servidores de banco de dados de back-end pode hospedar qualquer um dos bancos de dados content ou o banco de dados config. O software do aplicativo é executado somente nos servidores Web front-end, não nos servidores de banco de dados. Nessa configuração, o vss writer do aplicativo tem dependências remotas nos componentes gerenciados pelo SQL.

Um autor pode declarar uma dependência remota chamando o método [**AddComponentDependency,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) prepending " \\ \\ *RemoteComputerName*", em que \\ *RemoteComputerName* é o nome do computador em que o componente remoto reside, para o caminho lógico no *parâmetro wszOnLogicalPath.* O valor de *RemoteComputerName* pode ser um endereço IP ou um nome de computador retornado pela [**função GetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)

**Windows Server 2003:** Um writer não pode declarar dependências remotas até Windows Server 2003 com Service Pack 1 (SP1).

Para identificar uma dependência, um solicitante chama os métodos [**GetWriterId,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid) [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)e [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) da interface [**IVssWMDependency.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) O solicitante deve examinar o nome do componente que **GetComponentName** retorna no *parâmetro pbstrComponentName.* Se o nome do componente começar com " ", o solicitante deverá presumir que ele especifica uma dependência remota e que o primeiro componente a seguir " " é o RemoteComputerName especificado quando o autor chamou \\ \\ \\ \\ [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency).  Se o nome do componente não começar com " ", o solicitante deverá assumir que \\ \\ especifica uma dependência local.

Se houver uma dependência remota, o solicitante deverá fazer o back-up do componente remoto quando ele faz o back-up do componente local. Para fazer backup do componente remoto, o solicitante deve ter um agente no computador remoto e deve iniciar o backup no computador remoto.

## <a name="structuring-remote-dependencies"></a>Estruturando dependências remotas

É importante entender que uma dependência não é um componente em si mesmo. Um componente é necessário para manter a dependência.

Os exemplos a seguir mostram duas maneiras de estruturar um conjunto de dependências.

``` syntax
Example 1:
    Writer 1
        Component A
            File A
            File B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")

Example 2:
    Writer 2
        Component A
            File A
            File B
        Component B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")
```

No exemplo 1, as dependências são mantidas pelo Componente A. Como somente os componentes podem ser selecionados, não arquivos individuais, estruturar as dependências do Componente A dessa maneira exigiria que todo o componente, os arquivos e as dependências, sempre deve ser feito backup e restaurado juntos. Eles não podem ser backup ou restaurados individualmente.

No exemplo 2, componentes separados (Componentes A e B) resimentem cada uma das dependências. Nesse caso, os dois componentes podem ser selecionados independentemente e, portanto, backup e restauração independentemente. Estruturar as dependências dessa maneira oferece a um aplicativo distribuído muito mais flexibilidade para gerenciar suas dependências remotas.

## <a name="supporting-remote-dependencies"></a>Suporte a dependências remotas

Um solicitante pode fornecer suporte total ou parcial para dependências remotas.

Para fornecer suporte completo, o solicitante deve fazer o seguinte em tempo de backup e restauração.

No momento do backup, o solicitante deve iniciar o backup no computador de front-end (local), determinar as dependências existentes e fazer o spool de trabalhos de backup adicionais para capturar os bancos de dados de back-end. O solicitante deve aguardar até que os trabalhos de backup de back-end no computador remoto tenham sido concluídos antes de chamar os métodos [**IVssBackupComponents::SetBackupSucceededed**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**IVssBackupComponents::BackupComplete.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Se o solicitante aguardar até que o backup dos componentes de back-end seja concluído antes de chamar **BackupComplete**, isso produzirá um backup recuperável mais facilmente para um autor que implementa aprimoramentos adicionais, como bloqueio de topologia, por exemplo, durante o backup. O procedimento a seguir descreve o que o solicitante deve fazer:

1.  No computador local, o solicitante chama os métodos [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::P repareForBackup e**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
2.  Após a conclusão da cópia de sombra local, mas antes que o backup seja concluído, o solicitante faz o spool de trabalhos de backup adicionais enviando uma solicitação para seu agente no computador remoto.
3.  No computador remoto, o agente do solicitante executa a sequência de backup em spool chamando [**InitializeForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) [**GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**PrepareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) [**DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) [**SetBackupSucceeded e**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).
4.  Quando o agente do solicitante concluiu os trabalhos em spool no computador remoto, o solicitante conclui a sequência de backup chamando [**SetBackupSucceeded e**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

No momento da restauração, o solicitante deve iniciar a restauração que envolve o computador de front-end (local), selecionar os componentes e suas dependências a serem restaurados e, em seguida, enviar o evento [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) chamando o método **IVssBackupComponents::P reRestore.** Em seguida, o solicitante deve fazer o spool dos trabalhos de restauração de back-end no computador remoto e chamar o método [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) quando as restaurações de back-end são concluídas. Esse requisito dá ao autor de front-end mais controle sobre a experiência de restauração e uma melhor experiência geral do usuário administrador. Como os backups em cada um dos sistemas não ocorrem no mesmo ponto no tempo, o autor de front-end precisará executar alguma limpeza dos dados de back-end. No aplicativo de exemplo discutido na "Declaração de Dependências Remotas" anterior, o autor deve iniciar um remapeamento ou reindexação de site após a conclusão de uma restauração de um dos bancos de dados de back-end. Para fazer isso, o autor deve receber eventos no servidor front-end. O procedimento a seguir descreve o que o solicitante deve fazer:

1.  No computador local, o solicitante chama [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (ou [**IVssBackupComponentsEx::SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**PreRestore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
2.  Após a conclusão da fase [**PreRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) mas antes do início da fase [**PostRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) o solicitante faz o spool de trabalhos de restauração adicionais enviando uma solicitação para seu agente no computador remoto.
3.  No computador remoto, o agente do solicitante executa os trabalhos de restauração em spool chamando [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) [**(ou SetSelectedForRestoreEx)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)e [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Quando o agente do solicitante concluiu os trabalhos em spool no computador remoto, o solicitante conclui a sequência de restauração chamando [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) e [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Para fornecer suporte parcial para dependências remotas, o solicitante deve seguir dependências remotas e incluí-las como parte do backup, mas a ordenação de eventos em sistemas de front-end e back-end, conforme detalhado nos dois procedimentos anteriores, não seria necessária. Para um solicitante que implementa apenas o suporte parcial, o solicitante deve consultar a documentação de backup/restauração do aplicativo de autor para entender quais cenários podem ter suporte.

 

 
