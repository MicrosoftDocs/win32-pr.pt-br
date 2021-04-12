---
description: Há situações em que os dados de um gravador dependem dos dados gerenciados por outro gravador. Nesses casos, você deve fazer backup ou restaurar dados de ambos os gravadores.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dependências entre componentes gerenciados por diferentes gravadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba3be6a2c2f0a722c4c5f06ca95351e004e1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297503"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dependências entre componentes gerenciados por diferentes gravadores

Há situações em que os dados de um gravador dependem dos dados gerenciados por outro gravador. Nesses casos, você deve fazer backup ou restaurar dados de ambos os gravadores.

O VSS lida com esse problema por meio da noção de uma dependência de componente de gravador explícita e da interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) .

Um gravador adiciona uma ou mais dependências ao criar o documento de metadados do gravador usando o método [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) . O gravador passa o método, o nome e o caminho lógico do componente dependente (que ele gerencia), bem como o nome e o caminho lógico e a [*ID da classe do gravador*](vssgloss-w.md) (o GUID que identifica a classe) do componente sobre o qual ele depende.

Depois de estabelecida, essa dependência informa ao solicitante que, durante qualquer operação de backup ou restauração, o componente dependente e os destinos de suas dependências devem participar.

Um determinado componente pode ter várias dependências, o que exige que ele e todos os seus destinos dependentes participem do backup e da restauração juntos.

O componente dependente e/ou os destinos de suas dependências podem ser incluídos de forma [*explícita*](vssgloss-e.md) ou [*implícita*](vssgloss-i.md) em operações de backup ou restauração.

O mecanismo de dependência do componente de gravador explícito não deve ser usado para criar uma dependência entre dois componentes no mesmo gravador. As regras de seleção podem fornecer a mesma funcionalidade com mais eficiência, sem risco de dependências circulares.

Por exemplo, [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) poderia ser usado para definir a dependência do componente writerData (com o caminho lógico "") do gravador myWriter no componente internetData (com um caminho lógico de "conexões") de um gravador chamado InternetConnector com uma ID de classe de gravador X. (embora seja possível que vários gravadores com a mesma ID de classe estejam no sistema simultaneamente, a confusão será evitada porque a combinação de caminho lógico e nome do componente é exclusiva no sistema em VSS.)

Um gravador adiciona várias dependências a um determinado componente simplesmente chamando [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) repetido com componentes diferentes de diferentes gravadores. O número de outros componentes dos quais um determinado componente depende pode ser encontrado examinando o membro **cDependencies** da [**estrutura \_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) .

Um gravador ou solicitante recupera instâncias da interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) com [**IVssWMComponent:: getdependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). O **IVssWMDependency** retorna o nome do componente, o caminho lógico e a ID de classe do gravador que gerencia o componente que é o destino da dependência.

O mecanismo de dependência não prescreve nenhuma ordem de preferência específica entre o componente dependente e os destinos de suas dependências. Conforme observado acima, toda a dependência indica que, sempre que um determinado componente é submetido a backup ou restauração, o componente ou os componentes dos quais ele depende também devem ser armazenados em backup ou restaurado. A implementação exata da dependência é a critério do aplicativo de backup.

Por exemplo, no caso acima, o componente writerData (caminho lógico "") depende do componente InternetConnector ("conexões" do caminho lógico). Um solicitante é gratuito para interpretar isso de uma das seguintes maneiras:

-   Se o componente dependente, writerData, for selecionado (implicitamente ou explicitamente) para backup ou restauração, o solicitante deverá selecionar (implicitamente ou explicitamente) o destino de sua dependência, internetData
-   Se o destino de sua dependência, internetData, não for selecionado para backup, o componente dependente, writerData, não deverá ser selecionado.

No entanto, ao desenvolver suporte para dependências, os desenvolvedores de solicitantes devem estar cientes de que não há como um gravador pode determinar se um de seus componentes é um destino de uma dependência.

## <a name="declaring-remote-dependencies"></a>Declarando dependências remotas

Um aplicativo distribuído é um aplicativo que pode ser configurado para usar um ou mais computadores de cada vez. Normalmente, o aplicativo é executado em um ou mais computadores do servidor de aplicativos e se comunica com (mas pode ou não ser executado de fato em) um ou mais computadores do servidor de banco de dados. Essa configuração às vezes é chamada de implantação de vários sistemas. Geralmente, o mesmo aplicativo também pode ser configurado para ser executado em um único computador que executa um servidor de aplicativos e um servidor de banco de dados. Essa configuração é chamada de implantação de sistema único. Em ambas as configurações, o servidor de aplicativos e o servidor de banco de dados têm seus próprios gravadores VSS independentes.

Em uma implantação de vários sistemas, se um componente gerenciado pelo gravador do aplicativo depender de um componente remoto gerenciado pelo gravador do servidor de banco de dados, isso será chamado de dependência remota. (Uma implantação de sistema único, por outro lado, tem apenas dependências locais.)

Como exemplo de uma implantação de vários sistemas, considere um servidor de aplicativos que usa um servidor de banco de dados SQL Server como um armazenamento de dados. Os dados específicos do aplicativo, que incluem as Web Parts, os arquivos de conteúdo da Web e a metabase do IIS, residem em um ou mais computadores, chamados de servidores Web front-end. O armazenamento de dados SQL real, que inclui o banco de dado config e vários bancos de dados de conteúdo, reside em um ou mais computadores, chamados de servidores de banco de dados back-end. Cada um dos servidores Web front-end contém o mesmo conteúdo e configuração específicos do aplicativo. Cada um dos servidores de banco de dados back-end pode hospedar qualquer um dos bancos de dados de conteúdo ou de configuração. O software de aplicativo é executado somente nos servidores Web front-end, não nos servidores de banco de dados. Nessa configuração, o gravador VSS do aplicativo tem dependências remotas nos componentes gerenciados pelo gravador do SQL.

Um gravador pode declarar uma dependência remota chamando o método [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) , predependendo de " \\ \\ *RemoteComputerName* \\ ", em que *RemoteComputerName* é o nome do computador onde reside o componente remoto, no caminho lógico no parâmetro *wszOnLogicalPath* . O valor de *RemoteComputerName* pode ser um endereço IP ou um nome de computador retornado pela função [**GetComputerNameEx devia**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

**Windows Server 2003:** Um gravador não pode declarar dependências remotas até o Windows Server 2003 com Service Pack 1 (SP1).

Para identificar uma dependência, um solicitante chama os métodos [**Getwriterid**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)e [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) da interface [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) . O solicitante deve examinar o nome do componente que **GetComponentName** retorna no parâmetro *pbstrComponentName* . Se o nome do componente começar com " \\ \\ ", o solicitante deverá presumir que ele especifica uma dependência remota e que o primeiro componente após " \\ \\ " é o *RemoteComputerName* que foi especificado quando o gravador chamou [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency). Se o nome do componente não começar com " \\ \\ ", o solicitante deve assumir que ele especifica uma dependência local.

Se houver uma dependência remota, o solicitante deverá fazer backup do componente remoto quando fizer backup do componente local. Para fazer backup do componente remoto, o solicitante deve ter um agente no computador remoto e deve iniciar o backup no computador remoto.

## <a name="structuring-remote-dependencies"></a>Estruturando dependências remotas

É importante entender que uma dependência não é um componente por si só. Um componente é necessário para manter a dependência.

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

No exemplo 1, as dependências são mantidas pelo componente A. Como somente os componentes podem ser selecionados, não arquivos individuais, estruturar dependências do componente A dessa maneira exigiria que todo o componente, tanto os arquivos quanto as dependências, sempre deva ser submetido a backup e restaurado juntos. Eles não podem ser armazenados em backup ou restaurados individualmente.

No exemplo 2, componentes separados (componentes A e B) mantêm cada uma das dependências. Nesse caso, os dois componentes podem ser selecionados de forma independente e, portanto, são armazenados em backup e restaurados de forma independente. Estruturar as dependências dessa maneira dá a um aplicativo distribuído muito mais flexibilidade no gerenciamento de suas dependências remotas.

## <a name="supporting-remote-dependencies"></a>Suporte a dependências remotas

Um solicitante pode fornecer suporte total ou parcial para dependências remotas.

Para fornecer suporte completo, o solicitante deve fazer o seguinte no momento do backup e da restauração.

No momento do backup, o solicitante deve iniciar o backup no computador front-end (local), determinar as dependências que existem e spoolar trabalhos de backup adicionais para capturar os bancos de dados de back-end. O solicitante deve aguardar até que os trabalhos de backup de back-end no computador remoto sejam concluídos antes de chamar os métodos [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) . Se o solicitante aguardar até que o backup de componentes de back-end seja concluído antes de chamar **BackupComplete**, isso produzirá um backup mais facilmente recuperável para um gravador que implementa aprimoramentos adicionais, como o bloqueio de topologia, por exemplo, durante o backup. O procedimento a seguir descreve o que o solicitante deve fazer:

1.  No computador local, o solicitante chama os métodos [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::P Repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)e [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .
2.  Após a conclusão da cópia de sombra local, mas antes de o backup ser concluído, o solicitante coloca em spool os trabalhos de backup adicionais enviando uma solicitação para seu agente no computador remoto.
3.  No computador remoto, o agente do solicitante executa a sequência de backup em spool chamando [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)e [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).
4.  Quando o agente do solicitante tiver concluído os trabalhos em spool no computador remoto, o solicitante concluirá a sequência de backup chamando [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

No momento da restauração, o solicitante deve iniciar a restauração que envolve o computador front-end (local), selecionar os componentes e suas dependências a serem restaurados e, em seguida, enviar o evento de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) chamando o método **rerestore IVssBackupComponents::P** . O solicitante deve então armazenar em spool os trabalhos de restauração de back-end no computador remoto e chamar o método [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) quando as restaurações de back-end forem concluídas. Esse requisito fornece ao gravador de front-end mais controle sobre a experiência de restauração e uma melhor experiência de usuário de administrador geral. Como os backups em cada um dos sistemas não ocorrem no mesmo ponto no tempo, o gravador de front-end precisará executar alguma limpeza dos dados de back-end. No aplicativo de exemplo discutido no "declarando dependências remotas" anteriores, o gravador deve iniciar um remapeamento ou reindexação do site após a conclusão de uma restauração de um dos bancos de dados back-end. Para fazer isso, o gravador deve receber eventos no servidor front-end. O procedimento a seguir descreve o que o solicitante deve fazer:

1.  No computador local, o solicitante chama [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (ou [**IVssBackupComponentsEx:: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).
2.  Após a fase de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ser concluída, mas antes do início da fase de [**pós-restauração**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , o solicitante armazena em spool os trabalhos de restauração adicionais enviando uma solicitação para seu agente no computador remoto.
3.  No computador remoto, o agente do solicitante executa os trabalhos de restauração em spool chamando [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (ou [**SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**createrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Quando o agente do solicitante tiver concluído os trabalhos em spool no computador remoto, o solicitante concluirá a sequência de restauração chamando [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) e [**createrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Para fornecer suporte parcial para dependências remotas, o solicitante deve seguir as dependências remotas e incluí-las como parte do backup, mas a ordenação de eventos em sistemas de front-end e back-end, conforme detalhado nos dois procedimentos anteriores, não seria necessária. Para um solicitante que implementa apenas suporte parcial, o solicitante deve consultar a documentação de backup/restauração do aplicativo gravador para entender quais cenários podem ser suportados.

 

 
