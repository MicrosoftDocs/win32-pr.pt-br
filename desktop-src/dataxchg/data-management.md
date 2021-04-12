---
title: Gerenciamento de dados
description: Este tópico discute como os objetos de memória passam dados de um aplicativo para outro.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), gerenciamento de dados
- DDE (troca dinâmica de dados), gerenciamento de dados
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), gerenciamento de dados
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), gerenciamento de dados
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- Troca dinâmica de dados (DDE), objetos
- DDE (troca dinâmica de dados), objetos
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), objetos
- DDEML (troca dinâmica de dados biblioteca de gerenciamento), objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364460"
---
# <a name="data-management"></a>Gerenciamento de dados

Como troca dinâmica de dados (DDE) usa objetos de memória para passar dados de um aplicativo para outro, a troca dinâmica de dados biblioteca de gerenciamento (DDEML) fornece um conjunto de funções que os aplicativos DDE podem usar para criar e gerenciar objetos DDE.

Todas as transações que envolvem a troca de dados exigem que o aplicativo forneça os dados para criar um buffer local contendo os dados e, em seguida, chamar a função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) . Essa função aloca um objeto DDE, copia os dados do buffer para o objeto e retorna um identificador de dados. Um identificador de dados é um valor **DWORD** que o ddeml usa para fornecer acesso aos dados no objeto DDE. Para compartilhar os dados em um objeto DDE, um aplicativo passa o identificador de dados para o DDEML, e o DDEML passa o identificador para a função de retorno de chamada DDE do aplicativo que está recebendo a transação de dados.

O exemplo a seguir mostra como criar um objeto DDE e obter um identificador para o objeto. Durante a transação [**XTYP \_ ADVREQ**](xtyp-advreq.md) , a função de retorno de chamada converte a hora atual em uma cadeia de caracteres ASCII, copia a cadeia de caracteres em um buffer local e, em seguida, cria um objeto DDE que contém a cadeia de caracteres. A função de retorno de chamada retorna o identificador para o objeto DDE (HDDEDATA) para o DDEML, que passa o identificador para o aplicativo cliente.


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
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
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



O aplicativo receptor Obtém um ponteiro para o objeto DDE passando o identificador de dados para a função [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) . O ponteiro retornado por **DdeAccessData** fornece acesso somente leitura. O aplicativo deve usar o ponteiro para revisar os dados e, em seguida, chamar a função [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) para invalidar o ponteiro. O aplicativo pode copiar os dados para um buffer local usando a função [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .

O exemplo a seguir obtém um ponteiro para o objeto DDE identificado pelo parâmetro *hData* , copia o conteúdo para um buffer local e, em seguida, invalida o ponteiro.


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



Normalmente, quando um aplicativo que criou um identificador de dados passa esse identificador para o DDEML, o identificador torna-se inválido no aplicativo de criação. Essa situação não será um problema se o aplicativo precisar compartilhar dados com apenas um único aplicativo. Se um aplicativo precisar compartilhar os mesmos dados com vários aplicativos, no entanto, o aplicativo de criação deverá especificar o \_ sinalizador HDATA APPOWNED no [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle). Isso fornece a propriedade do objeto DDE para o aplicativo de criação e impede que o DDEML invalide o identificador de dados. O aplicativo pode passar o identificador de dados a qualquer número de vezes depois de chamar **DdeCreateDataHandle** apenas uma vez.

Se um aplicativo especificar o \_ sinalizador HDATA APPOWNED no parâmetro *AfCmd* de [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), ele deverá chamar a função [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) para liberar o identificador de memória, independentemente de ter passado o identificador para o ddeml. Antes de ser encerrado, um aplicativo deve chamar **DdeFreeDataHandle** para liberar qualquer identificador de dados que ele criou, mas não passou para o ddeml.

Um aplicativo que ainda não passou o identificador para um objeto DDE para o DDEML pode adicionar dados ao objeto ou substituir dados no objeto usando a função [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) . Normalmente, um aplicativo usa **DdeAddData** para preencher um objeto DDE não inicializado. Depois que um aplicativo passa um identificador de dados para o DDEML, o objeto DDE identificado pelo identificador não pode ser alterado; Ele só pode ser liberado.

 

 




