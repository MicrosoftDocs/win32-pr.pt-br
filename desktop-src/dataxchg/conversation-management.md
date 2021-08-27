---
title: Gerenciamento de conversa
description: Este tópico discute conversas entre um cliente e um servidor.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Windows Interface do Usuário,Dados Dinâmicos Exchange (DDE)
- Dados Dinâmicos Exchange (DDE), conversas
- DDE (Dados Dinâmicos Exchange), conversas
- troca de dados, Dados Dinâmicos Exchange (DDE)
- Windows Interface do Usuário,Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados Dinâmicos Exchange)
- Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange), conversas
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento),conversas
- troca de dados, Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados)
- Dados Dinâmicos Exchange (DDE), várias conversas
- DDE (Dados Dinâmicos Exchange), várias conversas
- Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange), várias conversas
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento), várias conversas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3531cc396a3b4d0eca5d7c11e3677aec9ea2ee35dcdac110455daee252f798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991326"
---
# <a name="conversation-management"></a>Gerenciamento de conversa

Uma conversa entre um cliente e um servidor é sempre estabelecida por solicitação do cliente. Quando uma conversa é estabelecida, cada parceiro recebe um identificador que identifica a conversa. Os parceiros usam esse handle em outras funções Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados) para enviar transações e gerenciar a conversa. Um cliente pode solicitar uma conversa com um único servidor ou pode solicitar várias conversas com um ou mais servidores.

Os tópicos a seguir descrevem como um aplicativo estabelece novas conversas e obtém informações sobre conversas existentes.

-   [Conversas individuais](#single-conversations)
-   [Várias conversas](#multiple-conversations)

## <a name="single-conversations"></a>Conversas individuais

Um aplicativo cliente solicita uma única conversa com um servidor chamando a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e especificando identificador de cadeia de caracteres que identificam as cadeias de caracteres que contêm o nome do serviço do aplicativo de servidor e o nome do tópico para a conversa. O DDEML responde enviando a transação [**XTYP \_ CONNECT**](xtyp-connect.md) para a função de retorno de chamada DDE (Dados Dinâmicos Exchange) de cada aplicativo de servidor que registrou um nome de serviço que corresponde ao especificado em **DdeConnect** ou que tenha desligado a filtragem de nome de serviço chamando [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Um servidor também pode filtrar **transações XTYP \_ CONNECT** especificando o sinalizador de filtro CBF FAIL CONNECTIONS na \_ função \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Durante a **transação do XTYP \_ CONNECT,** o DDEML passa o nome do serviço e o nome do tópico para o servidor. O servidor deverá examinar os nomes e retornar **TRUE** se ele for compatível com o nome do serviço e o par de nomes do tópico ou **FALSE** se não o fizer.

Se nenhum servidor responder positivamente à solicitação do cliente para se conectar, o cliente receberá **NULL** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e nenhuma conversa será estabelecida. Se um servidor retornar **TRUE**, uma conversa será estabelecida e o cliente receberá um identificador de conversa – um **valor DWORD** que identifica a conversa. O cliente usa o handle em chamadas DDEML subsequentes para obter dados do servidor. O servidor recebe a transação CONFIRM do [**XTYP \_ CONNECT \_**](xtyp-connect-confirm.md) (a menos que o servidor tenha especificado o sinalizador de filtro CBF \_ SKIP CONNECT \_ \_ CONFIRMS). Essa transação passa o alça de conversa para o servidor.

O exemplo a seguir solicita uma conversa no tópico Sistema com um servidor que reconhece o nome do serviço MyServer. Os *parâmetros hszServName* *e hszSysTopic* são alças de cadeia de caracteres criadas anteriormente.


```
HCONV hConv;         // conversation handle 
HWND hwndParent;     // parent window handle 
HSZ hszServName;     // service name string handle 
HSZ hszSysTopic;     // System topic string handle 
 
hConv = DdeConnect( 
    idInst,               // instance identifier 
    hszServName,          // service name string handle 
    hszSysTopic,          // System topic string handle 
    (PCONVCONTEXT) NULL); // use default context 
 
if (hConv == NULL) 
{ 
    MessageBox(hwndParent, "MyServer is unavailable.", 
        (LPSTR) NULL, MB_OK); 
    return FALSE; 
} 
```



No exemplo anterior, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) faz com que a função de retorno de chamada DDE do aplicativo MyServer receba uma [**transação XTYP \_ CONNECT.**](xtyp-connect.md)

No exemplo a seguir, o servidor responde à transação [**XTYP \_ CONNECT**](xtyp-connect.md) comparando a cadeia de caracteres de nome do tópico que trata o DDEML passado para o servidor com cada elemento na matriz de cadeia de caracteres de nome de tópico que o servidor dá suporte. Se o servidor encontrar uma combinação, ele estabelecerá a conversa.


```
#define CTOPICS 5 
 
HSZ hsz1;                  // string handle passed by DDEML 
HSZ ahszTopics[CTOPICS];   // array of supported topics 
int i;                     // loop counter 
 
// Use a switch statement to examine transaction types. 
// Here is the connect case.
 
    case XTYP_CONNECT: 
        for (i = 0; i < CTOPICS; i++) 
        { 
            if (hsz1 == ahszTopics[i]) 
                return TRUE;   // establish a conversation 
        } 
 
        return FALSE; // Topic not supported; deny conversation.  
 
// Process other transaction types. 
```



Se o servidor retornar **TRUE** em resposta à transação [**XTYP \_ CONNECT,**](xtyp-connect.md) o DDEML enviará uma transação CONFIRM do [**XTYP \_ CONNECT \_**](xtyp-connect-confirm.md) para a função de retorno de chamada DDE do servidor. O servidor pode obter o alçamento para a conversa processando essa transação.

Um cliente pode estabelecer uma conversa curinga especificando **NULL** para o handle de cadeia de caracteres de nome de serviço, o alçamento de cadeia de caracteres do nome do tópico ou ambos em uma chamada para [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect). Se pelo menos um dos alças de cadeia de caracteres for **NULL,** o DDEML enviará a transação [**\_ WILDCONNECT XTYP**](xtyp-wildconnect.md) para as funções de retorno de chamada de todos os aplicativos DDE (exceto aqueles que filtram a transação **XTYP \_ WILDCONNECT).** Cada aplicativo de servidor deve responder retornando um identificador de dados que identifica uma matriz terminada em nulo de estruturas [**HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) Se o aplicativo de servidor não tiver chamado [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar seus nomes de serviço e se a filtragem estiver em, o servidor não receberá transações **XTYP \_ WILDCONNECT.** Para obter mais informações sobre os handles de dados, [consulte Gerenciamento de Dados](data-management.md).

A matriz deve conter uma estrutura para cada nome de serviço e par de nomes de tópico que corresponde ao par especificado pelo cliente. O DDEML seleciona um dos pares para estabelecer uma conversa e retorna ao cliente um identificador que identifica a conversa. O DDEML envia a transação CONFIRM do [**XTYP \_ CONNECT \_**](xtyp-connect-confirm.md) para o servidor (a menos que o servidor filtra essa transação). O exemplo a seguir mostra uma resposta típica do servidor para a [**transação XTYP \_ WILDCONNECT.**](xtyp-wildconnect.md)


```
#define CTOPICS 2 
 
UINT uType; 
HSZPAIR ahszp[(CTOPICS + 1)]; 
HSZ ahszTopicList[CTOPICS]; 
HSZ hszServ, hszTopic; 
WORD i, j; 
 
if (uType == XTYP_WILDCONNECT) 
{ 
    // Scan the topic list and create an array of HSZPAIR structures. 
 
    j = 0; 
    for (i = 0; i < CTOPICS; i++) 
    { 
        if (hszTopic == (HSZ) NULL || 
                hszTopic == ahszTopicList[i]) 
        { 
            ahszp[j].hszSvc = hszServ; 
            ahszp[j++].hszTopic = ahszTopicList[i]; 
        } 
    } 
 
    // End the list with an HSZPAIR structure that contains NULL 
    // string handles as its members. 
 
    ahszp[j].hszSvc = NULL; 
    ahszp[j++].hszTopic = NULL; 
 
    // Return a handle to a global memory object containing the 
    // HSZPAIR structures. 
 
    return DdeCreateDataHandle( 
        idInst,          // instance identifier 
        (LPBYTE) &ahszp, // pointer to HSZPAIR array 
        sizeof(HSZ) * j, // length of the array 
        0,               // start at the beginning 
        (HSZ) NULL,      // no item name string 
        0,               // return the same format 
        0);              // let the system own it 
} 
```



O cliente ou o servidor pode encerrar uma conversa a qualquer momento chamando a [**função DdeDisconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) Essa função faz com que a função de retorno de chamada do parceiro na conversa receba a transação [**XTYP \_ DISCONNECT**](xtyp-disconnect.md) (a menos que o parceiro tenha especificado o sinalizador de filtro CBF \_ SKIP \_ DISCONNECTS). Normalmente, um aplicativo responde à transação **XTYP \_ DISCONNECT** usando a [**função DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obter informações sobre a conversa que terminou. Depois que a função de retorno de chamada retornar do processamento da transação **\_ XTYP DISCONNECT,** o handle de conversa não será mais válido.

Um aplicativo cliente que recebe uma transação [**XTYP \_ DISCONNECT**](xtyp-disconnect.md) em sua função de retorno de chamada DDE pode tentar restabelecer a conversa chamando a [**função DdeReconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) O cliente deve chamar **DdeReconnect de** dentro de sua função de retorno de chamada DDE.

## <a name="multiple-conversations"></a>Várias conversas

Um aplicativo cliente pode usar a [**função DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para determinar se os servidores de interesse estão disponíveis no sistema. Um cliente especifica um nome de serviço e um nome de tópico ao chamar **DdeConnectList**, fazendo com que o DDEML transmitisse a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para as funções de retorno de chamada DDE de todos os servidores que corresponderem ao nome do serviço (exceto aqueles que filtram a transação). A função de retorno de chamada de um servidor deve retornar um identificador de dados que identifica uma matriz terminada em nulo de estruturas [**HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) A matriz deve conter uma estrutura para cada nome de serviço e par de nomes de tópico que corresponde ao par especificado pelo cliente. O DDEML estabelece uma conversa para cada estrutura **HSZPAIR** preenchida pelo servidor e retorna um alça de lista de conversa para o cliente. O servidor recebe o handle de conversa por meio da transação [**XTYP \_ CONNECT**](xtyp-connect.md) (a menos que o servidor filtra essa transação).

Um cliente pode especificar **NULL** para o nome do serviço, o nome do tópico ou ambos quando ele chama [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Se o nome do serviço for **NULL,** todos os servidores no sistema que deem suporte ao nome do tópico especificado responderão. Uma conversa é estabelecida com cada servidor de resposta, incluindo várias instâncias do mesmo servidor. Se o nome do tópico for **NULL,** uma conversa será estabelecida em cada tópico reconhecido por cada servidor que corresponde ao nome do serviço.

Um cliente pode usar as funções [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para identificar os servidores que respondem ao [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). **DdeQueryNextServer** retorna a próxima alça de conversa em uma lista de conversa e **DdeQueryConvInfo** preenche uma estrutura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) com informações sobre a conversa. O cliente pode manter as alças de conversa de que precisa e descartar o restante da lista de conversa.

O exemplo a seguir usa [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para estabelecer conversas com todos os servidores que suportam o tópico Sistema e, em seguida, usa as funções [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obter os alças de cadeia de caracteres de nome de serviço dos servidores e armazená-los em um buffer.


```
HCONVLIST hconvList; // conversation list 
DWORD idInst;        // instance identifier 
HSZ hszSystem;       // System topic 
HCONV hconv = NULL;  // conversation handle 
CONVINFO ci;         // holds conversation data 
UINT cConv = 0;      // count of conv. handles 
HSZ *pHsz, *aHsz;    // point to string handles 
 
// Connect to all servers that support the System topic. 
 
hconvList = DdeConnectList(idInst, NULL, hszSystem, NULL, NULL); 
 
// Count the number of handles in the conversation list. 
 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
    cConv++; 
 
// Allocate a buffer for the string handles. 
 
hconv = NULL; 
aHsz = (HSZ *) LocalAlloc(LMEM_FIXED, cConv * sizeof(HSZ)); 
 
// Copy the string handles to the buffer. 
 
pHsz = aHsz; 
while ((hconv = DdeQueryNextServer(hconvList, hconv)) != NULL) 
{ 
    DdeQueryConvInfo(hconv, QID_SYNC, (PCONVINFO) &ci); 
    DdeKeepStringHandle(idInst, ci.hszSvcPartner); 
    *pHsz++ = ci.hszSvcPartner; 
} 
 
// Use the handles; converse with the servers. 
 
// Free the memory and terminate the conversations. 
 
LocalFree((HANDLE) aHsz); 
DdeDisconnectList(hconvList); 
```



Um aplicativo pode encerrar uma conversa individual em uma lista de conversa chamando a [**função DdeDisconnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) Um aplicativo pode encerrar todas as conversas em uma lista de conversas chamando a [**função DdeDisconnectList.**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) Ambas as funções faz com que o DDEML envie transações [**\_ DISCONNECT XTYP**](xtyp-disconnect.md) para a função de retorno de chamada DDE de cada parceiro. **DdeDisconnectList** envia uma transação **\_ DISCONNECT XTYP** para cada alça de conversa na lista.

Um cliente pode recuperar uma lista de alças de conversa em uma lista de conversa passando um alça de lista de conversa existente para [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). O processo de enumeração remove os alças de conversas encerradas da lista e as conversas não duplicadas que se ajustam ao nome do serviço e ao nome do tópico especificados são adicionadas.

Se [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) especificar um alça de lista de conversa existente, a função criará uma nova lista de conversa que contém os alças de todas as novas conversas e os alças da lista existente.

Se existirem conversas duplicadas, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tentará impedir os alças de conversa duplicados na lista de conversas. Uma conversa duplicada é uma segunda conversa com o mesmo servidor com o mesmo nome de serviço e nome do tópico. Duas dessas conversas teriam identificador diferentes, mas identificariam a mesma conversa.

 

 




