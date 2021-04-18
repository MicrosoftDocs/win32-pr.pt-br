---
title: Gerenciamento de conversa
description: Este tópico discute as conversas entre um cliente e um servidor.
ms.assetid: 4e5ff1a1-d46a-4e2a-a37c-8df951f2a1ee
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), conversas
- DDE (troca dinâmica de dados), conversas
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), conversas
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), conversas
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- Troca dinâmica de dados (DDE), várias conversas
- DDE (troca dinâmica de dados), várias conversas
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), várias conversas
- DDEML (troca dinâmica de dados biblioteca de gerenciamento), várias conversas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca1a0a8e02bceb6b2f69051d89df289871fdd42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764304"
---
# <a name="conversation-management"></a>Gerenciamento de conversa

Uma conversa entre um cliente e um servidor é sempre estabelecida com a solicitação do cliente. Quando uma conversa é estabelecida, cada parceiro recebe um identificador que identifica a conversa. Os parceiros usam esse identificador em outras funções de DDEML (biblioteca de gerenciamento de troca dinâmica de dados) para enviar transações e gerenciar a conversa. Um cliente pode solicitar uma conversa com um único servidor ou pode solicitar várias conversas com um ou mais servidores.

Os tópicos a seguir descrevem como um aplicativo estabelece novas conversas e obtém informações sobre conversas existentes.

-   [Conversas únicas](#single-conversations)
-   [Várias conversas](#multiple-conversations)

## <a name="single-conversations"></a>Conversas únicas

Um aplicativo cliente solicita uma única conversa com um servidor chamando a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e especificando identificadores de cadeia que identificam as cadeias de caracteres que contêm o nome do serviço do aplicativo do servidor e o nome do tópico para a conversa. O DDEML responde enviando a transação [**XTYP \_ Connect**](xtyp-connect.md) para a função de retorno de chamada troca dinâmica de dados (DDE) de cada aplicativo de servidor que registrou um nome de serviço que corresponda ao especificado em **DdeConnect** ou que a filtragem de nome de serviço foi desativada chamando [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Um servidor também pode filtrar transações de **\_ conexão XTYP** especificando o \_ sinalizador de filtro CBF falha de \_ conexões na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Durante a transação **XTYP \_ Connect** , o ddeml passa o nome do serviço e o nome do tópico para o servidor. O servidor deve examinar os nomes e retornar **true** se ele der suporte ao nome do serviço e ao nome do tópico par ou **false** se não tiver.

Se nenhum servidor responder positivamente à solicitação do cliente para se conectar, o cliente receberá **NULL** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e nenhuma conversa será estabelecida. Se um servidor retornar **true**, uma conversa será estabelecida e o cliente receberá um identificador de conversa — um valor **DWORD** que identifica a conversa. O cliente usa o identificador em chamadas de DDEML subsequentes para obter dados do servidor. O servidor recebe a transação [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) (a menos que o servidor tenha especificado o \_ sinalizador de filtro CBF Skip \_ Connect \_ confirmations). Essa transação passa o identificador de conversa para o servidor.

O exemplo a seguir solicita uma conversa no tópico System com um servidor que reconhece o nome do serviço meuservidor. Os parâmetros *hszServName* e *hszSysTopic* são identificadores de cadeia de caracteres criados anteriormente.


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



No exemplo anterior, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) faz com que a função de retorno de chamada DDE do aplicativo meuservidor receba uma transação de [**\_ conexão XTYP**](xtyp-connect.md) .

No exemplo a seguir, o servidor responde à transação do [**XTYP \_ Connect**](xtyp-connect.md) comparando a cadeia de caracteres do nome do tópico que o ddeml passado para o servidor com cada elemento na matriz de cadeia de caracteres de nome de tópico que o servidor suporta. Se o servidor encontrar uma correspondência, ele estabelecerá a conversa.


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



Se o servidor retornar **true** em resposta à transação [**XTYP \_ Connect**](xtyp-connect.md) , o ddeml enviará uma transação [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) para a função de retorno de chamada DDE do servidor. O servidor pode obter o identificador para a conversa processando essa transação.

Um cliente pode estabelecer uma conversa de caractere curinga especificando **NULL** para o identificador de cadeia de caracteres do nome do serviço, o nome do tópico identificador de cadeia de caracteres ou ambos em uma chamada para [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect). Se pelo menos um dos identificadores de cadeia de caracteres for **NULL**, o ddeml envia a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para as funções de retorno de chamada de todos os aplicativos DDE (exceto aqueles que filtram a transação **XTYP \_ WILDCONNECT** ). Cada aplicativo de servidor deve responder retornando um identificador de dados que identifica uma matriz terminada em nulo de estruturas [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) . Se o aplicativo de servidor não tiver chamado [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar seus nomes de serviço e se a filtragem estiver ativada, o servidor não receberá transações **XTYP \_ WILDCONNECT** . Para obter mais informações sobre identificadores de dados, consulte [Gerenciamento de dados](data-management.md).

A matriz deve conter uma estrutura para cada nome de serviço e par de nome de tópico que corresponda ao par especificado pelo cliente. O DDEML seleciona um dos pares para estabelecer uma conversa e retorna ao cliente um identificador que identifica a conversa. O DDEML envia a transação de [**\_ \_ confirmação de XTYP Connect**](xtyp-connect-confirm.md) para o servidor (a menos que o servidor filtre essa transação). O exemplo a seguir mostra uma resposta de servidor típica para a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .


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



O cliente ou o servidor pode encerrar uma conversa a qualquer momento chamando a função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) . Essa função faz com que a função de retorno de chamada do parceiro na conversa receba a transação de [**\_ desconexão XTYP**](xtyp-disconnect.md) (a menos que o parceiro tenha especificado o \_ sinalizador de filtro CBF ignorar \_ desconexões). Normalmente, um aplicativo responde à transação **de \_ desconexão XTYP** usando a função [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obter informações sobre a conversa encerrada. Depois que a função de retorno de chamada retorna do processamento da transação de **\_ desconexão XTYP** , o identificador de conversa não é mais válido.

Um aplicativo cliente que recebe uma transação [**XTYP \_ Disconnect**](xtyp-disconnect.md) em sua função de retorno de chamada DDE pode tentar restabelecer a conversa chamando a função [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) . O cliente deve chamar **DdeReconnect** de dentro de sua função de retorno de chamada DDE.

## <a name="multiple-conversations"></a>Várias conversas

Um aplicativo cliente pode usar a função [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para determinar se algum servidor de interesse está disponível no sistema. Um cliente especifica um nome de serviço e nome de tópico quando chama **DdeConnectList**, fazendo com que o ddeml transmita a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para as funções de retorno de chamada DDE de todos os servidores que correspondem ao nome do serviço (exceto aqueles que filtram a transação). A função de retorno de chamada de um servidor deve retornar um identificador de dados que identifica uma matriz terminada em nulo de estruturas [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) . A matriz deve conter uma estrutura para cada nome de serviço e par de nome de tópico que corresponda ao par especificado pelo cliente. O DDEML estabelece uma conversa para cada estrutura **HSZPAIR** preenchida pelo servidor e retorna um identificador de lista de conversa para o cliente. O servidor recebe o identificador de conversa por meio da transação [**XTYP \_ Connect**](xtyp-connect.md) (a menos que o servidor filtre essa transação).

Um cliente pode especificar **NULL** para o nome do serviço, o nome do tópico ou ambos ao chamar [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). Se o nome do serviço for **nulo**, todos os servidores no sistema que dão suporte ao nome do tópico especificado responderão. Uma conversa é estabelecida com cada servidor de resposta, incluindo várias instâncias do mesmo servidor. Se o nome do tópico for **nulo**, uma conversa será estabelecida em cada tópico reconhecido por cada servidor que corresponde ao nome do serviço.

Um cliente pode usar as funções [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para identificar os servidores que respondem ao [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). **DdeQueryNextServer** retorna o próximo identificador de conversa em uma lista de conversa e **DdeQueryConvInfo** preenche uma estrutura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) com informações sobre a conversa. O cliente pode manter os identificadores de conversa necessários e descartar o restante da lista de conversa.

O exemplo a seguir usa [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para estabelecer conversas com todos os servidores que dão suporte ao tópico System e, em seguida, usa as funções [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obter os identificadores de cadeia de caracteres de nome de serviço dos servidores e armazená-los em um buffer.


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



Um aplicativo pode encerrar uma conversa individual em uma lista de conversa chamando a função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) . Um aplicativo pode encerrar todas as conversas em uma lista de conversa chamando a função [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) . Ambas as funções fazem com que o DDEML envie transações de [**\_ desconexão XTYP**](xtyp-disconnect.md) para a função de retorno de chamada DDE de cada parceiro. **DdeDisconnectList** envia uma transação de **\_ desconexão XTYP** para cada identificador de conversa na lista.

Um cliente pode recuperar uma lista de identificadores de conversa em uma lista de conversa passando um identificador de lista de conversa existente para [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist). O processo de enumeração remove os identificadores de conversas encerradas da lista e as conversas não duplicadas que se ajustam ao nome do serviço e ao nome do tópico especificados são adicionadas.

Se [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) especificar um identificador de lista de conversa existente, a função criará uma nova lista de conversa que contém os identificadores de novas conversas e os identificadores da lista existente.

Se houver conversas duplicadas, o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tentará impedir identificadores de conversa duplicados na lista de conversa. Uma conversa duplicada é uma segunda conversa com o mesmo servidor no mesmo nome de serviço e nome de tópico. Duas conversas desse tipo teriam identificadores diferentes, ainda que identifiquem a mesma conversa.

 

 




