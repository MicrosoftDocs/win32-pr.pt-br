---
description: Controle do rastreamento do Winsock
ms.assetid: b079bdfc-b192-451c-967d-dcefa94b7ec7
title: Controle do rastreamento do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc80251410b95e2d02106474ae97ab3c6ea57759dcfdbc76987d6621794c822e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996806"
---
# <a name="control-of-winsock-tracing"></a>Controle do rastreamento do Winsock

O rastreamento do Winsock pode ser controlado usando um dos seguintes métodos:

-   Ferramentas da linha de comando

    duas ferramentas de linha de comando são incluídas no Windows Vista e no Windows Server 2008 que são usados para controlar o rastreamento e converter o arquivo de log de rastreamento binário em texto legível.

    A ferramenta **logman.exe** é usada para iniciar ou parar o rastreamento do Winsock.

    A ferramenta de **tracerpt.exe** é usada para converter o arquivo de log de rastreamento binário em um arquivo de texto legível.

-   Visualizador de Eventos

    o Visualizador de Eventos no Windows Vista e posterior também pode ser usado para habilitar o rastreamento do Winsock. o Visualizador de Eventos é acessível nas ferramentas administrativas do menu Iniciar.

## <a name="using-logman-and-tracert"></a>Usando Logman e tracert

o rastreamento de eventos de rede do Winsock é desabilitado por padrão no Windows Vista e posterior.

O comando a seguir inicia o rastreamento de eventos de rede do Winsock em um computador, define o nome da sessão de rastreamento de eventos como mywinsocksession e envia a saída para um arquivo de log binário chamado winsocklogfile. etl:

**logman start-ets mywinsocksession-o winsocklogfile. etl-p Microsoft-Windows-Winsock-AFD**

Os arquivos de log são criados no diretório atual com nomes de arquivo do formato winsocklogfile \_ 000001. etl

O comando a seguir interrompe o rastreamento do Winsock acima em um computador para a sessão chamada mywinsocksession:

**logman Stop-ETS mywinsocksession**

Um arquivo de log binário será gravado no local especificado pelo parâmetro – o. Para converter o arquivo binário em um arquivo de texto legível, **tracerpt.exe** é usado:

**tracerpt.exe <nome do arquivo. etl> – o winsocktracelog.txt**

Se um arquivo de saída contendo XML em vez de texto sem formatação for preferencial, o seguinte comando será usado:

**tracerpt.exe <nome do arquivo. etl> – o winsocktracelog.xml – do XML**

o rastreamento de alterações do catálogo Winsock é habilitado por padrão no Windows Vista e posterior.

> [!Note]  
> Os provedores de serviço em camadas são preteridos. começando com Windows 8 e Windows Server 2012, use [Windows plataforma de filtragem](../fwp/windows-filtering-platform-start-page.md).

 

O comando a seguir inicia o rastreamento de alterações do catálogo Winsock para provedores de serviço em camadas (LSPs) em um computador, define o nome da sessão de rastreamento de eventos como mywinsockcatalogsession e envia a saída para um arquivo de log binário chamado winsockcataloglogfile. etl:

**logman start-ets mywinsockcatalogsession-o winsockcataloglogfile. etl-p Microsoft-Windows-Winsock-WS2HELP**

Os arquivos de log são criados no diretório atual com nomes de arquivo do formato winsockcataloglogfile \_ 000001. etl

O comando a seguir interrompe o rastreamento do Winsock acima em um computador para a sessão chamada MySession:

**logman Stop-ETS mywinsockcatalogsession**

Um arquivo de log binário será gravado no local especificado pelo parâmetro – o. Para converter o arquivo binário em um arquivo de texto legível, **tracerpt.exe** é usado:

**tracerpt.exe <nome do arquivo. etl> – o winsockcatalogtracelog.txt**

Se um arquivo de saída contendo XML em vez de texto sem formatação for preferencial, o seguinte comando será usado:

**tracerpt.exe <nome do arquivo. etl> – o winsockcatalogtracelog.xml – do XML**

## <a name="using-event-viewer-to-start-winsock-network-event-tracing"></a>Usando Visualizador de Eventos para iniciar o rastreamento de eventos de rede do Winsock

Quando você abre Visualizador de Eventos, o painel esquerdo contém a lista de eventos. abra **Logs de aplicativos e serviços** e navegue até **Microsoft \\ Windows evento de \\ rede Winsock** como a origem e selecione **operacional**.

No painel Ação, selecione **Propriedades do log** e marque a caixa de seleção **habilitar registro em log** . Quando o registro em log estiver habilitado, você também poderá alterar o tamanho do arquivo de log se isso for necessário.

O rastreamento de eventos de rede do Winsock agora está habilitado e tudo o que você precisa fazer é pressionar a ação atualizar para atualizar a lista de eventos que foram registrados. Para interromper o registro em log, basta desmarcar o mesmo botão de opção.

Talvez seja necessário aumentar o tamanho do log dependendo de quantos eventos você deseja ver. Uma desvantagem de usar o Visualizador de Eventos para o rastreamento de Winsock é que ele não carrega todos os recursos de cadeia de caracteres, de modo que as mensagens exibidas no campo Descrição (depois que você seleciona um evento) às vezes são difíceis de serem lidas (um argumento que deve ser formatado como hex será exibido em decimal, por exemplo). No entanto, você pode selecionar a guia **detalhes** na descrição do evento que mostra a entrada de log XML bruto que geralmente tem mais facilidade para entender os argumentos.

## <a name="using-event-viewer-to-start-winsock-catalog-change-tracing"></a>Usando Visualizador de Eventos para iniciar o rastreamento de alterações do catálogo Winsock

Quando você abre Visualizador de Eventos, o painel esquerdo contém a lista de eventos. abra **Logs de aplicativos e serviços** e navegue até **Microsoft \\ Windows catálogo de \\ Winsock altere** como a origem e selecione **operacional**.

No painel Ação, selecione **Propriedades do log** e marque a caixa de seleção **habilitar registro em log** . Quando o registro em log estiver habilitado, você também poderá alterar o tamanho do arquivo de log se isso for necessário.

O rastreamento de alterações do catálogo do Winsock agora está habilitado e tudo o que você precisa fazer é pressionar a ação atualizar para atualizar a lista de eventos que foram registrados. Para interromper o registro em log, basta desmarcar o mesmo botão de opção.

Talvez seja necessário aumentar o tamanho do log dependendo de quantos eventos você deseja ver. Uma desvantagem de usar o Visualizador de Eventos para o rastreamento de Winsock é que ele não carrega todos os recursos de cadeia de caracteres, de modo que as mensagens exibidas no campo Descrição (depois que você seleciona um evento) às vezes são difíceis de serem lidas (um argumento que deve ser formatado como hex será exibido em decimal, por exemplo). No entanto, você pode selecionar a guia **detalhes** na descrição do evento que mostra a entrada de log XML bruto que geralmente tem mais facilidade para entender os argumentos.

## <a name="interpreting-winsock-tracing-logs"></a>Interpretando logs de rastreamento do Winsock

Todos os eventos de rastreamento do Winsock em um log contêm dois tipos de informações:

-   Sistema
-   EventData

As informações do sistema contêm o nível de log, a hora em que a entrada de log foi criada, a ID do evento que representa o tipo de evento, a ID do processo de execução, a ID do thread de execução e outras informações do sistema. Um nível de log de 4 no rastreamento do Winsock representa o log de eventos de informações. Um nível de log de 5 no rastreamento de Winsock representa o log de eventos detalhado.

A ID do processo de execução e a ID do thread nas informações do sistema indicam o processo e o thread que estava em execução quando o evento ocorreu. Em muitos casos, isso representará um kernel ou thread de trabalho e processo, não um thread de modo de usuário e ou o processo do aplicativo. Portanto, esse campo normalmente não é muito útil.

Cada tipo de evento de rastreamento do Winsock tem uma ID de evento exclusiva na seção do sistema dos dados registrados. Essas IDs de evento podem ser facilmente usadas para filtrar um arquivo de log para eventos de rastreamento Winsock específicos.

O EventData contém informações específicas para o tipo de evento.

O parâmetro Process nas informações de EVENTDATA é o endereço da estrutura EPROCESS do kernel para o processo, não o PID real. Para corresponder um evento à PID do modo de usuário, pegue o valor do processo das informações de EVENTDATA de qualquer entrada de log e examine antes no log um evento de criação de soquete com o valor do processo. Quando uma correspondência é encontrada, o último parâmetro nos dados de evento de criação de soquete é a ID de processo do modo de usuário que criou o soquete.

Um parâmetro de endereço nas informações de EVENTDATA é retornado em alguns eventos de rastreamento do Winsock. Um parâmetro de endereço representa um endereço IP, mas é exibido no arquivo de texto criado pela ferramenta de **tracerpt.exe** ou em Visualizador de eventos como bytes brutos ou um número. Os endereços IPv6 são exibidos em hexadecimal, para que sejam compreendidos com mais facilidade. Os endereços IPv4 são exibidos como um número decimal grande. Os desenvolvedores precisarão converter manualmente os bytes brutos de um endereço IPv4 para a notação de endereço decimal de IPv4 pontilhado e mais familiar para ser mais capaz de interpretar o valor.

Um parâmetro de erro no EVENTDATA é retornado em alguns eventos de rastreamento do Winsock. Um parâmetro de erro é da forma de um código de erro NTSTATUS ou HRESULT. Esse parâmetro de erro é exibido no arquivo de texto criado pela ferramenta de **tracerpt.exe** ou no Visualizador de eventos como um número decimal. Os desenvolvedores precisarão converter manualmente o número decimal para um número hexadecimal a fim de interpretar melhor o código de erro em alguns casos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalhes de rastreamento de alteração do catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Detalhes de rastreamento de eventos de rede do Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
