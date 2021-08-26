---
title: Gerenciamento de dados
description: Este tópico discute como os objetos de memória passam dados de um aplicativo para outro.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Windows Interface do Usuário,Dados Dinâmicos Exchange (DDE)
- Dados Dinâmicos Exchange (DDE), gerenciamento de dados
- DDE (Dados Dinâmicos Exchange), gerenciamento de dados
- troca de dados, Dados Dinâmicos Exchange (DDE)
- Windows Interface do Usuário,Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados Dinâmicos Exchange)
- DDEML (biblioteca de gerenciamento de Dados Dinâmicos Exchange), gerenciamento de dados
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento de dados), gerenciamento de dados
- troca de dados, Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados)
- Dados Dinâmicos Exchange (DDE), objetos
- DDE (Dados Dinâmicos Exchange), objetos
- DDEML (biblioteca de gerenciamento do Dados Dinâmicos Exchange), objetos
- DDEML (biblioteca Dados Dinâmicos Exchange de gerenciamento),objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dc9b8ccd82d184866ac9ed28f15bdeac424ec0bf9bd7767a520dea69bc4d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953736"
---
# <a name="data-management"></a>Gerenciamento de dados

Como Dados Dinâmicos Exchange (DDE) usa objetos de memória para passar dados de um aplicativo para outro, a DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange) fornece um conjunto de funções que os aplicativos DDE podem usar para criar e gerenciar objetos DDE.

Todas as transações que envolvem a troca de dados exigem que o aplicativo que fornece os dados crie um buffer local contendo os dados e, em seguida, chame a [**função DdeCreateDataHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) Essa função aloca um objeto DDE, copia os dados do buffer para o objeto e retorna um identificador de dados. Um identificador de dados é **um valor DWORD** que o DDEML usa para fornecer acesso aos dados no objeto DDE. Para compartilhar os dados em um objeto DDE, um aplicativo passa o identificador de dados para o DDEML e o DDEML passa o identificador para a função de retorno de chamada DDE do aplicativo que está recebendo a transação de dados.

O exemplo a seguir mostra como criar um objeto DDE e obter um identificador para o objeto . Durante a transação [**DO XTYP \_ ADVREQ,**](xtyp-advreq.md) a função de retorno de chamada converte a hora atual em uma cadeia de caracteres ASCII, copia a cadeia de caracteres para um buffer local e, em seguida, cria um objeto DDE que contém a cadeia de caracteres. A função de retorno de chamada retorna o identificador para o objeto DDE (HDDEDATA) para o DDEML, que passa o identificador para o aplicativo cliente.


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



O aplicativo receptor obtém um ponteiro para o objeto DDE passando o identificador de dados para a [**função DdeAccessData.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) O ponteiro retornado por **DdeAccessData** fornece acesso somente leitura. O aplicativo deve usar o ponteiro para revisar os dados e, em seguida, chamar a [**função DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) para invalidar o ponteiro. O aplicativo pode copiar os dados para um buffer local usando a [**função DdeGetData.**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)

O exemplo a seguir obtém um ponteiro para o objeto DDE identificado pelo parâmetro *hData,* copia o conteúdo para um buffer local e invalida o ponteiro.


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



Normalmente, quando um aplicativo que criou um handle de dados passa esse manipular para o DDEML, o handle se torna inválido no aplicativo de criação. Essa situação não será um problema se o aplicativo deve compartilhar dados com apenas um único aplicativo. Se um aplicativo precisar compartilhar os mesmos dados com vários aplicativos, no entanto, o aplicativo de criação deverá especificar o sinalizador \_ HDATA APPOWNED [**em DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle). Isso fornece a propriedade do objeto DDE ao aplicativo de criação e impede que o DDEML invalide o identificador de dados. O aplicativo pode passar o lidar com os dados várias vezes depois de chamar **DdeCreateDataHandle** apenas uma vez.

Se um aplicativo especificar o sinalizador HDATA APPOWNED no parâmetro \_ *afCmd* de [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), ele deverá chamar a função [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) para liberar o alçamento de memória, independentemente de ter passado o handle para o DDEML. Antes de ser encerrado, um aplicativo deve chamar **DdeFreeDataHandle** para liberar qualquer alça de dados que ele criou, mas não passou para o DDEML.

Um aplicativo que ainda não passou o identificador para um objeto DDE para o DDEML pode adicionar dados ao objeto ou substituir dados no objeto usando a [**função DdeAddData.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) Normalmente, um aplicativo usa **DdeAddData** para preencher um objeto DDE não reinicializado. Depois que um aplicativo passa um identificador de dados para o DDEML, o objeto DDE identificado pelo identificador não pode ser alterado; ele só pode ser liberado.

 

 




