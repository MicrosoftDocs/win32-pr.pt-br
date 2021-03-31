---
title: Operação assíncrona
description: No modo assíncrono, um aplicativo pode executar qualquer função que inclua um valor de contexto como um de seus parâmetros e possa continuar a executar outros comandos ou funções enquanto o aplicativo aguarda a função concluir sua tarefa.
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7e1d0cf84aa92691e1d926d771ea809d31a171
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641507"
---
# <a name="asynchronous-operation"></a>Operação assíncrona

A quantidade de tempo que leva um aplicativo para acessar um recurso da Internet depende de vários fatores, como a conexão que está sendo usada, o servidor no qual o recurso está localizado e o número de usuários tentando acessar o recurso. Para aplicativos que baixam vários recursos ou lidam com várias tarefas (incluindo um ou mais downloads), aguardando a conclusão de cada download antes de passar para a próxima tarefa pode ser extremamente ineficiente. Para diminuir a quantidade de tempo que um aplicativo precisa esperar, muitas das funções WinINet podem operar de forma assíncrona.

No modo assíncrono, um aplicativo pode executar qualquer função que inclua um valor de contexto como um de seus parâmetros e possa continuar a executar outros comandos ou funções enquanto o aplicativo aguarda a função concluir sua tarefa. Enquanto a tarefa estiver sendo concluída, uma função de retorno de chamada de status fornecida pelo aplicativo será notificada sobre o progresso da tarefa e quando ela for concluída. Neste momento, a função de retorno de chamada de status pode chamar outras funções ou executar outras tarefas necessárias que dependem da conclusão da tarefa.

Não há nenhum thread de retorno de chamada afinity quando você chama o WinINet de forma assíncrona: uma chamada pode iniciar de um thread, mas qualquer outro thread pode receber o retorno de chamada.

-   [Benefícios](#benefits)
-   [Cenários](#scenarios)
-   [Tópicos relacionados](#related-topics)

## <a name="benefits"></a>Benefícios

Há vários benefícios para operar de forma assíncrona. Por exemplo:

-   Baixar vários recursos da Internet simultaneamente.

    Você pode se conectar a vários recursos da Internet ao mesmo tempo e baixá-los à medida que eles forem disponibilizados.

-   Aumentando o desempenho do seu aplicativo.

    Um aplicativo que usa as funções do WinINet de forma assíncrona não precisa esperar até que a solicitação seja concluída, portanto, o aplicativo está livre para realizar outras tarefas que não dependem da solicitação, melhorando assim o desempenho geral do aplicativo.

-   Monitore o progresso do download.

    A função de retorno de chamada de status recebe notificações enquanto está processando uma solicitação. Se necessário, seu aplicativo pode usar as informações fornecidas por essa função de retorno de chamada de status para manter o usuário informado sobre o progresso da operação ou para interromper solicitações que estão demorando muito para serem concluídas.

## <a name="scenarios"></a>Cenários

Digamos que seu aplicativo precise baixar preços de café do Downfall café & chá e os sites da Fourth Coffee e comparar os preços. O site da Fourth Coffee geralmente tem um tempo de resposta mais lento, de modo que seu aplicativo deve baixar as informações do Downfall café & primeiro chá.

Duas versões do aplicativo são desenvolvidas. Um deles funciona de forma síncrona, baixando os preços do site do Downfall café & de chá e, em seguida, os preços do site da Fourth Coffee. O segundo funciona de forma assíncrona, enviando solicitações para ambos os sites e baixando os preços quando eles se tornam disponíveis.

A tabela a seguir ilustra o que aconteceria se o site da Fourth Coffee fosse mais rápido em um determinado dia.



| Evento                                                            | Versão síncrona                        | Versão assíncrona                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| Iniciar                                                            | Enviar solicitação para Downfall café & chá      | Envie solicitações para Downfall café & chá e Fourth Coffee |
| Solicitação da versão assíncrona para a Fourth Coffee concluída | Aguardando                                    | Baixar preços do Fourth Coffee                       |
| Solicitação para Downfall café & chá concluído                       | Baixar preços do Downfall café & chá | Baixar preços do Downfall café & chá               |
| Após o Downfall café & os preços de chá são baixados              | Enviar solicitação para Fourth Coffee              | Comparar preços                                           |
| Comparação da versão assíncrona concluída                      | Aguardando                                    | Operação concluída                                       |
| Solicitação da versão síncrona para a Fourth Coffee concluída  | Baixar preços do Fourth Coffee         | n/a                                                      |
| Após o download dos preços da Fourth Coffee                      | Comparar preços                             | n/a                                                      |
| Comparação da versão síncrona concluída                       | Operação concluída                         | n/a                                                      |



 

Outro exemplo seria um navegador da Web, como o Microsoft Internet Explorer. Quando o navegador baixa uma página, ele geralmente precisa baixar outros recursos, como imagens e arquivos de som. No modo assíncrono, a página e seus recursos associados podem ser solicitados simultaneamente e baixados à medida que são disponibilizados, em vez de solicitar e baixar a página e cada recurso, um de cada vez.

## <a name="related-topics"></a>Tópicos relacionados

A seguir estão os links relacionados.

Tutoriais

-   [Criando funções de retorno de chamada de status](creating-status-callback-functions.md)

Funções necessárias para configurar a operação assíncrona

-   [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

Funções que podem ser usadas de forma assíncrona

-   [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
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
-   [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> As funções [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)e [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) usam o valor de contexto fornecido na chamada para a função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .

 

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 