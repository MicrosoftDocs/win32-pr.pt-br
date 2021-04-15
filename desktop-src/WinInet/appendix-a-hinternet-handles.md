---
title: Identificadores de HINTERNET
description: Esta seção contém informações sobre os identificadores que são usados pelas funções WinINet e a hierarquia em que funcionam.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba70d2fadbd0d8393685fec2075ebf0dc4aa11c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454272"
---
# <a name="hinternet-handles"></a>Identificadores de HINTERNET

Esta seção contém informações sobre os identificadores que são usados pelas funções WinINet e a hierarquia em que funcionam.

-   [Sobre identificadores de HINTERNET](#about-hinternet-handles)
-   [Hierarquia de identificadores](#handle-hierarchy)
-   [Hierarquia de FTP](#ftp-hierarchy)
-   [Hierarquia HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>Sobre identificadores de HINTERNET

Os identificadores criados e usados pelas funções do WinINet são do tipo **HINTERNET**. As funções WinINet retornam identificadores **HINTERNET** que não são intercambiáveis com outros tipos de identificador. Portanto, eles não podem ser usados com funções como [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). Da mesma forma, outros tipos de identificador não podem ser usados com as funções WinINet. Por exemplo, um identificador retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) não pode ser passado para [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

A função [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) fecha identificadores do tipo **HINTERNET**. Observe que os valores de identificador são reciclados rapidamente; Portanto, se um identificador for fechado e um novo identificador for gerado imediatamente, haverá uma boa chance de que o novo identificador tenha o mesmo valor que o identificador acabou de fechar.

## <a name="handle-hierarchy"></a>Hierarquia de identificadores

Os identificadores **HINTERNET** são mantidos em uma hierarquia de árvore. O identificador retornado pela função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) é o nó raiz. Os identificadores retornados pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ocupam o próximo nível. Os identificadores retornados pelas funções [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)e [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) são os nós folha.

**Windows XP e Windows Server 2003 R2 e anteriores:** Os identificadores retornados por, [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)e [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) também são nós folha.

O diagrama a seguir ilustra a hierarquia dos identificadores **HINTERNET** . Cada caixa no diagrama representa uma função que retorna um identificador **HINTERNET** .

![funções que criam identificadores](images/ax-wnt01.png)

No nível superior está a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , que cria o identificador raiz. O próximo nível contém as funções [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . As funções que usam o identificador retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) compõem o último nível.

O diagrama a seguir mostra as funções que dependem do identificador criado pelo [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). As caixas sombreadas representam funções que retornam identificadores **HINTERNET** , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função associada.

![funções que usam o identificador InternetOpenUrl](images/ax-wnt02.png)

As funções [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) usam o identificador **HINTERNET** criado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

## <a name="ftp-hierarchy"></a>Hierarquia de FTP

O diagrama a seguir mostra as funções de FTP que dependem do identificador de sessão de FTP retornado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). As caixas sombreadas representam funções que retornam identificadores **HINTERNET** , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.

![funções que usam o identificador de sessão de FTP](images/ax-wnt06.png)

As funções [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)e [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) usam o identificador **HINTERNET** criado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

O diagrama a seguir mostra as duas funções FTP que retornam identificadores e as funções que dependem delas. As caixas sombreadas representam funções que retornam identificadores **HINTERNET** , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.

![funções que usam o identificador de ftpopen e FtpFindFirstFile](images/ax-wnt03.png)

A função [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) é dependente do identificador criado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), enquanto [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) usam o identificador criado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).

## <a name="http-hierarchy"></a>Hierarquia HTTP

O diagrama a seguir mostra as relações das funções que são usadas para o protocolo HTTP. As caixas sombreadas representam funções que retornam identificadores **HINTERNET** , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.

![funções que usam o identificador de HttpOpenRequest](images/ax-wnt05.png)

As funções [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa), [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)e [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) são dependentes do identificador criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

O diagrama a seguir mostra as funções que usam o identificador **HINTERNET** criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) após ele ser enviado pelo [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). As caixas sombreadas representam funções que retornam identificadores **HINTERNET** , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.

![funções que usam o identificador após httpsendrequest](images/ax-wnt07.png)

Depois que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) tiver usado o identificador retornado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), ele poderá ser usado por [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer).

![funções que usam o identificador após HttpSendRequestEx](images/ax-wnt08.png)

Depois que [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) tiver usado o identificador retornado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), o identificador poderá ser usado por [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta), [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)e [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile). Depois que [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) tiver sido chamado, o identificador poderá ser usado por [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)e [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable).

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 