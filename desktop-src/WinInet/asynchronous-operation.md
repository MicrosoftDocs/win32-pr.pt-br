---
title: Operação assíncrona
description: No modo assíncrono, um aplicativo pode executar qualquer função que inclua um valor de contexto como um de seus parâmetros e pode continuar a executar outros comandos ou funções enquanto o aplicativo aguarda a função concluir sua tarefa.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e494b79b28b9aaf005fc6b1790d0cf84b07ceade6606f03ce03198426ac33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118562088"
---
# <a name="asynchronous-operation"></a>Operação assíncrona

A quantidade de tempo que leva um aplicativo para acessar um recurso da Internet depende de vários fatores, como a conexão que está sendo usada, o servidor no qual o recurso está localizado e o número de usuários tentando acessar o recurso. Para aplicativos que baixam vários recursos ou lidam com várias tarefas (incluindo um ou mais downloads), aguardar a conclusão de cada download antes de passar para a próxima tarefa pode ser extremamente ineficiente. Para diminuir a quantidade de tempo que um aplicativo precisa aguardar, muitas das funções do WinINet podem operar de forma assíncrona.

No modo assíncrono, um aplicativo pode executar qualquer função que inclua um valor de contexto como um de seus parâmetros e pode continuar a executar outros comandos ou funções enquanto o aplicativo aguarda a função concluir sua tarefa. Enquanto a tarefa está sendo concluída, uma função de retorno de chamada de status fornecida pelo aplicativo é notificada sobre o progresso da tarefa e quando ela é concluída. Neste momento, a função de retorno de chamada de status pode chamar outras funções ou executar qualquer outra tarefa necessária que dependa da conclusão da tarefa.

Não há nenhuma afinidade de thread de retorno de chamada quando você chama WinINet de forma assíncrona: uma chamada pode começar de um thread, mas qualquer outro thread pode receber o retorno de chamada.

-   [Benefícios](#benefits)
-   [Cenários](#scenarios)
-   [Tópicos relacionados](#related-topics)

## <a name="benefits"></a>Benefícios

Há vários benefícios em operar de forma assíncrona. Por exemplo:

-   Baixando vários recursos da Internet simultaneamente.

    Você pode se conectar a vários recursos da Internet ao mesmo tempo e baixá-los à medida que eles ficam disponíveis.

-   Aumentar o desempenho do aplicativo.

    Um aplicativo que usa as funções winINet de forma assíncrona não precisa esperar até que a solicitação seja concluída, portanto, o aplicativo é livre para realizar outras tarefas que não dependem da solicitação, melhorando assim o desempenho geral do aplicativo.

-   Monitore o progresso do download.

    A função de retorno de chamada de status recebe notificações durante o processamento de uma solicitação. Se necessário, seu aplicativo pode usar as informações fornecidas por essa função de retorno de chamada de status para manter o usuário informado sobre o progresso da operação ou interromper solicitações que estão demorando muito para ser concluídas.

## <a name="scenarios"></a>Cenários

Digamos que seu aplicativo precise baixar os preços de café dos cafés de baixo & De café e dos sites quarto café e comparar os preços. O quarto site café geralmente tem um tempo de resposta mais lento, portanto, seu aplicativo deve baixar as informações do Downfall Coffee & Primeiro.

Duas versões do aplicativo são desenvolvidas. Uma delas funciona de forma síncrona, primeiro baixando os preços do site do Café de & Desincronicamente e, em seguida, os preços do quarto site de Café. O segundo funciona de forma assíncrona, enviando solicitações para ambos os sites e baixando os preços quando eles ficam disponíveis.

A tabela a seguir ilustra o que aconteceria se o quarto site de Café fosse mais rápido em um dia específico.



| Evento                                                            | Versão síncrona                        | Versão assíncrona                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Iniciar                                                            | Enviar solicitação para o Café de & Café      | Enviar solicitações para o Café de & e o Quarto Café |
| Solicitação da versão assíncrona para Quarto Café concluída | Aguardando                                    | Baixar preços do Quarto Café                       |
| Solicitação para o café de & de café concluído                       | Baixar preços do Café em Queda & Café | Baixar preços do Café em Queda & Café               |
| Após o downfall Coffee & preços do Bule são baixados              | Enviar solicitação para o Quarto Café              | Comparar preços                                           |
| Comparação da versão assíncrona concluída                      | Aguardando                                    | Operação concluída                                       |
| Solicitação da versão síncrona para Quarto Café concluída  | Baixar preços do Quarto Café         | n/d                                                      |
| Depois que os preços do Quarto Café são baixados                      | Comparar preços                             | n/d                                                      |
| Comparação da versão síncrona concluída                       | Operação concluída                         | n/d                                                      |



 

Outro exemplo seria um navegador da Web, como o Microsoft Internet Explorer. Quando o navegador baixa uma página, geralmente ele precisa baixar outros recursos, como imagens e arquivos de som. No modo assíncrono, a página e seus recursos associados podem ser solicitados simultaneamente e baixados à medida que ficam disponíveis, em vez de solicitar e baixar a página e cada recurso um por vez.

## <a name="related-topics"></a>Tópicos relacionados

A seguir estão os links relacionados.

Tutoriais

-   [Criando funções de retorno de chamada de status](creating-status-callback-functions.md)

Funções necessárias para configurar a operação assíncrona

-   [**InternetA abrir**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funções que podem ser usadas de forma assíncrona

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**Ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**Internetopenurl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> As funções [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) [**FtpGetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)e [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) usam o valor de contexto fornecido na chamada para a [**função InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

 

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 