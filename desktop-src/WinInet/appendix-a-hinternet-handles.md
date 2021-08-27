---
title: Alças HINTERNET
description: Esta seção contém informações sobre os alças que são usados pelas funções WinINet e a hierarquia na qual eles funcionam.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051888"
---
# <a name="hinternet-handles"></a>Alças HINTERNET

Esta seção contém informações sobre os alças que são usados pelas funções WinINet e a hierarquia na qual eles funcionam.

-   [Sobre os alças HINTERNET](#about-hinternet-handles)
-   [Hierarquia de alça](#handle-hierarchy)
-   [Hierarquia FTP](#ftp-hierarchy)
-   [Hierarquia HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Sobre os alças HINTERNET

Os identificador criados e usados pelas funções WinINet são do **tipo HINTERNET.** As funções WinINet retornam **alças HINTERNET** que não são intercambiáveis com outros tipos de alça. Portanto, eles não podem ser usados com funções como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Da mesma forma, outros tipos de alça não podem ser usados com as funções WinINet. Por exemplo, um handle retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) não pode ser passado para [**InternetReadFile.**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)

A [**função InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) fecha os identificador do **tipo HINTERNET.** Observe que os valores de alça são reciclados rapidamente; portanto, se um alça for fechado e um novo alça for gerado imediatamente, haverá uma boa chance de que o novo alça tenha o mesmo valor que o alça recém-fechado.

## <a name="handle-hierarchy"></a>Hierarquia de alça

Os **alças HINTERNET** são mantidos em uma hierarquia de árvore. O handle retornado pela [**função InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) é o nó raiz. Os alças retornados pela [**função InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ocupam o próximo nível. Os handles retornados pelas [**funções FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)e [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) são os nós folha.

**Windows XP e Windows Server 2003 R2 e anteriores:** Os handles retornados por , [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)e [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) também são nós folha.

O diagrama a seguir ilustra a hierarquia dos **alças HINTERNET.** Cada caixa no diagrama representa uma função que retorna um **handle HINTERNET.**

![funções que criam alças](images/ax-wnt01.png)

No nível superior está a [**função InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) que cria o alça raiz. O próximo nível contém as [**funções InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) As funções que usam o handle retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) comem o último nível.

O diagrama a seguir mostra as funções que dependem do handle criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). As caixas sombreadas representam funções que retornam alças **HINTERNET,** enquanto as caixas simples representam funções que usam o alça **HINTERNET** criado pela função associada.

![funções que usam a alça internetopenurl](images/ax-wnt02.png)

As [**funções InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) usam o handle **HINTERNET** criado por [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)

## <a name="ftp-hierarchy"></a>Hierarquia FTP

O diagrama a seguir mostra as funções FTP que dependem do handle de sessão FTP retornado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) As caixas sombreadas representam funções que retornam alças **HINTERNET,** enquanto as caixas simples representam funções que usam o alça **HINTERNET** criado pela função da qual dependem.

![funções que usam o alça de sessão ftp](images/ax-wnt06.png)

As funções [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**FtpGetCurrentDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**FtpRemoveDirectory,**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) usam o handle **HINTERNET** criado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

O diagrama a seguir mostra as duas funções FTP que retornam as alças e as funções que dependem delas. As caixas sombreadas representam funções que retornam alças **HINTERNET,** enquanto as caixas simples representam funções que usam o alça **HINTERNET** criado pela função da qual dependem.

![funções que usam o handle de ftpopen e ftpfindfirstfile](images/ax-wnt03.png)

A [**função InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) depende do handle criado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), enquanto [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) usam o alça criado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).

## <a name="http-hierarchy"></a>Hierarquia HTTP

O diagrama a seguir mostra as relações das funções usadas para o protocolo HTTP. As caixas sombreadas representam funções que retornam alças **HINTERNET,** enquanto as caixas simples representam funções que usam o alça **HINTERNET** criado pela função da qual dependem.

![funções que usam o handle de httpopenrequest](images/ax-wnt05.png)

As [**funções HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**HttpQueryInfo,**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) [**HttpSendRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)e [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) dependem do handle criado por [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)

O diagrama a seguir mostra as funções que usam o handle **HINTERNET** criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) depois que ele é enviado por [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) As caixas sombreadas representam funções que retornam alças **HINTERNET,** enquanto as caixas simples representam funções que usam o alça **HINTERNET** criado pela função da qual dependem.

![funções que usam o handle após httpsendrequest](images/ax-wnt07.png)

Depois [**que HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) tiver usado o handle retornado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), ele poderá ser usado por [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer.**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)

![funções que usam o handle após httpsendrequestex](images/ax-wnt08.png)

Depois [**que HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) tiver usado o handle retornado por [**HttpOpenRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)o handle poderá ser usado por [**HttpEndRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile). Depois [**que HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) tiver sido chamado, o handle poderá ser usado por [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)e [**InternetQueryDataAvailable.**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)

> [!Note]  
> O WinINet não dá suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o WinHTTP (Microsoft Windows HTTP Services).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 