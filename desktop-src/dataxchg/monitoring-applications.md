---
title: Monitorando aplicativos
description: este tópico discute como os elementos da biblioteca de gerenciamento de troca dinâmica de dados podem ser usados para criar um aplicativo que monitora a atividade de troca de dados dinâmicos no sistema.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Windows Interface do usuário, troca dinâmica de dados (DDE)
- troca dinâmica de dados (DDE), monitoramento de aplicativos
- DDE (troca dinâmica de dados), monitorando aplicativos
- troca de dados, troca dinâmica de dados (DDE)
- Windows Interface do usuário, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), aplicativos de monitoramento
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), aplicativos de monitoramento
- data exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbf6db1faa765378ea2b22b1146de770e9c94b14cf7e9e511ab862be48369c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128548"
---
# <a name="monitoring-applications"></a>Monitorando aplicativos

os elementos de API da biblioteca de gerenciamento de troca dinâmica de dados (DDEML) podem ser usados para criar um aplicativo que monitora a atividade de troca dinâmica de dados (DDE) no sistema. Como qualquer aplicativo de DDEML, um aplicativo de monitoramento de DDE contém uma função de retorno de chamada DDE. O DDEML notifica uma função de retorno de chamada DDE do aplicativo de monitoramento sempre que um evento DDE ocorrer, passando informações sobre o evento para a função de retorno de chamada. O aplicativo normalmente exibe as informações em uma janela ou grava-as em um arquivo.

Para receber notificações do DDEML, um aplicativo deve ter sido registrado como um monitor DDE, especificando o \_ sinalizador do monitor APPCLASS em uma chamada para a função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Nesta mesma chamada, o aplicativo pode especificar um ou mais sinalizadores de monitor para indicar os tipos de eventos para os quais o DDEML é notificar a função de retorno de chamada do aplicativo. Os sinalizadores de monitor a seguir podem ser especificados por um aplicativo:



| Sinalizador          | Descrição                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_retornos de chamada MF | Notifica a função de retorno de chamada sempre que uma transação é enviada para qualquer função de retorno de chamada DDE no sistema.                                                                                                                                           |
| CONV de MF \_      | Notifica a função de retorno de chamada sempre que uma conversa é estabelecida ou terminada.                                                                                                                                                                |
| erros de MF \_    | Notifica a função de retorno de chamada sempre que ocorrer um erro DDEML.                                                                                                                                                                                       |
| \_informações de HSZ MF \_ | Notifica a função de retorno de chamada sempre que um aplicativo DDEML cria, libera ou incrementa a contagem de uso de um identificador de cadeia de caracteres ou sempre que um identificador de cadeia de caracteres é liberado como resultado de uma chamada para a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . |
| \_links MF     | Notifica a função de retorno de chamada sempre que um loop de aviso é iniciado ou encerrado.                                                                                                                                                                         |
| MENSAGENS de MF \_  | Notifica a função de retorno de chamada sempre que o sistema ou um aplicativo postar uma mensagem DDE.                                                                                                                                                           |
| \_SENDMSGS MF  | Notifica a função de retorno de chamada sempre que o sistema ou um aplicativo envia uma mensagem DDE.                                                                                                                                                           |



 

O exemplo a seguir mostra como registrar um aplicativo de monitoramento de DDE para que sua função de retorno de chamada DDE receba notificações de todos os eventos DDE.


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



O DDEML informa um aplicativo de monitoramento de um evento DDE enviando uma transação de [**\_ Monitor de XTYP**](xtyp-monitor.md) para a função de retorno de chamada DDE do aplicativo. Durante essa transação, o DDEML passa um sinalizador de monitor que especifica o tipo de evento DDE que ocorreu e um identificador para um objeto DDE que contém informações detalhadas sobre o evento. O DDEML fornece um conjunto de estruturas que o aplicativo pode usar para extrair as informações do objeto DDE. Há uma estrutura correspondente para cada tipo de evento DDE.



| Estrutura                                  | Descrição                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Contém informações sobre uma transação.                         |
| [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Contém informações sobre uma conversa.                        |
| [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Contém informações sobre o erro DDE mais recente.                  |
| [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Contém informações sobre um loop de aviso.                        |
| [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Contém informações sobre um identificador de cadeia de caracteres.                       |
| [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Contém informações sobre uma mensagem DDE que foi enviada ou postada. |



 

O exemplo a seguir mostra a função de retorno de chamada DDE de um aplicativo de monitoramento DDE que formata informações sobre cada evento de identificador de cadeia de caracteres e, em seguida, exibe as informações em uma janela. A função usa a estrutura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) para extrair as informações do objeto DDE.


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




