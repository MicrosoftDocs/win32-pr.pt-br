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
# <a name="conversation-management"></a><span data-ttu-id="46863-115">Gerenciamento de conversa</span><span class="sxs-lookup"><span data-stu-id="46863-115">Conversation Management</span></span>

<span data-ttu-id="46863-116">Uma conversa entre um cliente e um servidor é sempre estabelecida com a solicitação do cliente.</span><span class="sxs-lookup"><span data-stu-id="46863-116">A conversation between a client and a server is always established at the request of the client.</span></span> <span data-ttu-id="46863-117">Quando uma conversa é estabelecida, cada parceiro recebe um identificador que identifica a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-117">When a conversation is established, each partner receives a handle that identifies the conversation.</span></span> <span data-ttu-id="46863-118">Os parceiros usam esse identificador em outras funções de DDEML (biblioteca de gerenciamento de troca dinâmica de dados) para enviar transações e gerenciar a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-118">The partners use this handle in other Dynamic Data Exchange Management Library (DDEML) functions to send transactions and manage the conversation.</span></span> <span data-ttu-id="46863-119">Um cliente pode solicitar uma conversa com um único servidor ou pode solicitar várias conversas com um ou mais servidores.</span><span class="sxs-lookup"><span data-stu-id="46863-119">A client can request a conversation with a single server, or it can request multiple conversations with one or more servers.</span></span>

<span data-ttu-id="46863-120">Os tópicos a seguir descrevem como um aplicativo estabelece novas conversas e obtém informações sobre conversas existentes.</span><span class="sxs-lookup"><span data-stu-id="46863-120">The following topics describe how an application establishes new conversations and gets information about existing conversations.</span></span>

-   [<span data-ttu-id="46863-121">Conversas únicas</span><span class="sxs-lookup"><span data-stu-id="46863-121">Single Conversations</span></span>](#single-conversations)
-   [<span data-ttu-id="46863-122">Várias conversas</span><span class="sxs-lookup"><span data-stu-id="46863-122">Multiple Conversations</span></span>](#multiple-conversations)

## <a name="single-conversations"></a><span data-ttu-id="46863-123">Conversas únicas</span><span class="sxs-lookup"><span data-stu-id="46863-123">Single Conversations</span></span>

<span data-ttu-id="46863-124">Um aplicativo cliente solicita uma única conversa com um servidor chamando a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e especificando identificadores de cadeia que identificam as cadeias de caracteres que contêm o nome do serviço do aplicativo do servidor e o nome do tópico para a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-124">A client application requests a single conversation with a server by calling the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function and specifying string handles that identify the strings containing the service name of the server application and the topic name for the conversation.</span></span> <span data-ttu-id="46863-125">O DDEML responde enviando a transação [**XTYP \_ Connect**](xtyp-connect.md) para a função de retorno de chamada troca dinâmica de dados (DDE) de cada aplicativo de servidor que registrou um nome de serviço que corresponda ao especificado em **DdeConnect** ou que a filtragem de nome de serviço foi desativada chamando [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span><span class="sxs-lookup"><span data-stu-id="46863-125">The DDEML responds by sending the [**XTYP\_CONNECT**](xtyp-connect.md) transaction to the Dynamic Data Exchange (DDE) callback function of each server application that either has registered a service name that matches the one specified in **DdeConnect** or has turned service name filtering off by calling [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice).</span></span> <span data-ttu-id="46863-126">Um servidor também pode filtrar transações de **\_ conexão XTYP** especificando o \_ sinalizador de filtro CBF falha de \_ conexões na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="46863-126">A server can also filter **XTYP\_CONNECT** transactions by specifying the CBF\_FAIL\_CONNECTIONS filter flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="46863-127">Durante a transação **XTYP \_ Connect** , o ddeml passa o nome do serviço e o nome do tópico para o servidor.</span><span class="sxs-lookup"><span data-stu-id="46863-127">During the **XTYP\_CONNECT** transaction, the DDEML passes the service name and the topic name to the server.</span></span> <span data-ttu-id="46863-128">O servidor deve examinar os nomes e retornar **true** se ele der suporte ao nome do serviço e ao nome do tópico par ou **false** se não tiver.</span><span class="sxs-lookup"><span data-stu-id="46863-128">The server must examine the names and return **TRUE** if it supports the service name and topic name pair or **FALSE** if it does not.</span></span>

<span data-ttu-id="46863-129">Se nenhum servidor responder positivamente à solicitação do cliente para se conectar, o cliente receberá **NULL** de [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e nenhuma conversa será estabelecida.</span><span class="sxs-lookup"><span data-stu-id="46863-129">If no server responds positively to the client's request to connect, the client receives **NULL** from [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) and no conversation is established.</span></span> <span data-ttu-id="46863-130">Se um servidor retornar **true**, uma conversa será estabelecida e o cliente receberá um identificador de conversa — um valor **DWORD** que identifica a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-130">If a server returns **TRUE**, a conversation is established and the client receives a conversation handle — a **DWORD** value that identifies the conversation.</span></span> <span data-ttu-id="46863-131">O cliente usa o identificador em chamadas de DDEML subsequentes para obter dados do servidor.</span><span class="sxs-lookup"><span data-stu-id="46863-131">The client uses the handle in subsequent DDEML calls to obtain data from the server.</span></span> <span data-ttu-id="46863-132">O servidor recebe a transação [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) (a menos que o servidor tenha especificado o \_ sinalizador de filtro CBF Skip \_ Connect \_ confirmations).</span><span class="sxs-lookup"><span data-stu-id="46863-132">The server receives the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction (unless the server specified the CBF\_SKIP\_CONNECT\_CONFIRMS filter flag).</span></span> <span data-ttu-id="46863-133">Essa transação passa o identificador de conversa para o servidor.</span><span class="sxs-lookup"><span data-stu-id="46863-133">This transaction passes the conversation handle to the server.</span></span>

<span data-ttu-id="46863-134">O exemplo a seguir solicita uma conversa no tópico System com um servidor que reconhece o nome do serviço meuservidor.</span><span class="sxs-lookup"><span data-stu-id="46863-134">The following example requests a conversation on the System topic with a server that recognizes the service name MyServer.</span></span> <span data-ttu-id="46863-135">Os parâmetros *hszServName* e *hszSysTopic* são identificadores de cadeia de caracteres criados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="46863-135">The *hszServName* and *hszSysTopic* parameters are previously created string handles.</span></span>


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



<span data-ttu-id="46863-136">No exemplo anterior, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) faz com que a função de retorno de chamada DDE do aplicativo meuservidor receba uma transação de [**\_ conexão XTYP**](xtyp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="46863-136">In the preceding example, [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) causes the DDE callback function of the MyServer application to receive an [**XTYP\_CONNECT**](xtyp-connect.md) transaction.</span></span>

<span data-ttu-id="46863-137">No exemplo a seguir, o servidor responde à transação do [**XTYP \_ Connect**](xtyp-connect.md) comparando a cadeia de caracteres do nome do tópico que o ddeml passado para o servidor com cada elemento na matriz de cadeia de caracteres de nome de tópico que o servidor suporta.</span><span class="sxs-lookup"><span data-stu-id="46863-137">In the following example, the server responds to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction by comparing the topic name string handle the DDEML passed to the server with each element in the array of topic name string handles the server supports.</span></span> <span data-ttu-id="46863-138">Se o servidor encontrar uma correspondência, ele estabelecerá a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-138">If the server finds a match, it establishes the conversation.</span></span>


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



<span data-ttu-id="46863-139">Se o servidor retornar **true** em resposta à transação [**XTYP \_ Connect**](xtyp-connect.md) , o ddeml enviará uma transação [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) para a função de retorno de chamada DDE do servidor.</span><span class="sxs-lookup"><span data-stu-id="46863-139">If the server returns **TRUE** in response to the [**XTYP\_CONNECT**](xtyp-connect.md) transaction, the DDEML sends an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's DDE callback function.</span></span> <span data-ttu-id="46863-140">O servidor pode obter o identificador para a conversa processando essa transação.</span><span class="sxs-lookup"><span data-stu-id="46863-140">The server can obtain the handle to the conversation by processing this transaction.</span></span>

<span data-ttu-id="46863-141">Um cliente pode estabelecer uma conversa de caractere curinga especificando **NULL** para o identificador de cadeia de caracteres do nome do serviço, o nome do tópico identificador de cadeia de caracteres ou ambos em uma chamada para [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span><span class="sxs-lookup"><span data-stu-id="46863-141">A client can establish a wildcard conversation by specifying **NULL** for the service name string handle, the topic name string handle, or both in a call to [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect).</span></span> <span data-ttu-id="46863-142">Se pelo menos um dos identificadores de cadeia de caracteres for **NULL**, o ddeml envia a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para as funções de retorno de chamada de todos os aplicativos DDE (exceto aqueles que filtram a transação **XTYP \_ WILDCONNECT** ).</span><span class="sxs-lookup"><span data-stu-id="46863-142">If at least one of the string handles is **NULL**, the DDEML sends the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the callback functions of all DDE applications (except those that filter the **XTYP\_WILDCONNECT** transaction).</span></span> <span data-ttu-id="46863-143">Cada aplicativo de servidor deve responder retornando um identificador de dados que identifica uma matriz terminada em nulo de estruturas [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="46863-143">Each server application should respond by returning a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="46863-144">Se o aplicativo de servidor não tiver chamado [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar seus nomes de serviço e se a filtragem estiver ativada, o servidor não receberá transações **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="46863-144">If the server application has not called [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) to register its service names and if filtering is on, the server does not receive **XTYP\_WILDCONNECT** transactions.</span></span> <span data-ttu-id="46863-145">Para obter mais informações sobre identificadores de dados, consulte [Gerenciamento de dados](data-management.md).</span><span class="sxs-lookup"><span data-stu-id="46863-145">For more information about data handles, see [Data Management](data-management.md).</span></span>

<span data-ttu-id="46863-146">A matriz deve conter uma estrutura para cada nome de serviço e par de nome de tópico que corresponda ao par especificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="46863-146">The array must contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="46863-147">O DDEML seleciona um dos pares para estabelecer uma conversa e retorna ao cliente um identificador que identifica a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-147">The DDEML selects one of the pairs to establish a conversation and returns to the client a handle that identifies the conversation.</span></span> <span data-ttu-id="46863-148">O DDEML envia a transação de [**\_ \_ confirmação de XTYP Connect**](xtyp-connect-confirm.md) para o servidor (a menos que o servidor filtre essa transação).</span><span class="sxs-lookup"><span data-stu-id="46863-148">The DDEML sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server (unless the server filters this transaction).</span></span> <span data-ttu-id="46863-149">O exemplo a seguir mostra uma resposta de servidor típica para a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="46863-149">The following example shows a typical server response to the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


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



<span data-ttu-id="46863-150">O cliente ou o servidor pode encerrar uma conversa a qualquer momento chamando a função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="46863-150">Either the client or the server can terminate a conversation at any time by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="46863-151">Essa função faz com que a função de retorno de chamada do parceiro na conversa receba a transação de [**\_ desconexão XTYP**](xtyp-disconnect.md) (a menos que o parceiro tenha especificado o \_ sinalizador de filtro CBF ignorar \_ desconexões).</span><span class="sxs-lookup"><span data-stu-id="46863-151">This function causes the callback function of the partner in the conversation to receive the [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction (unless the partner specified the CBF\_SKIP\_DISCONNECTS filter flag).</span></span> <span data-ttu-id="46863-152">Normalmente, um aplicativo responde à transação **de \_ desconexão XTYP** usando a função [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obter informações sobre a conversa encerrada.</span><span class="sxs-lookup"><span data-stu-id="46863-152">Typically, an application responds to the **XTYP\_DISCONNECT** transaction by using the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function to obtain information about the conversation that terminated.</span></span> <span data-ttu-id="46863-153">Depois que a função de retorno de chamada retorna do processamento da transação de **\_ desconexão XTYP** , o identificador de conversa não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="46863-153">After the callback function returns from processing the **XTYP\_DISCONNECT** transaction, the conversation handle is no longer valid.</span></span>

<span data-ttu-id="46863-154">Um aplicativo cliente que recebe uma transação [**XTYP \_ Disconnect**](xtyp-disconnect.md) em sua função de retorno de chamada DDE pode tentar restabelecer a conversa chamando a função [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) .</span><span class="sxs-lookup"><span data-stu-id="46863-154">A client application that receives an [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transaction in its DDE callback function can attempt to reestablish the conversation by calling the [**DdeReconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect) function.</span></span> <span data-ttu-id="46863-155">O cliente deve chamar **DdeReconnect** de dentro de sua função de retorno de chamada DDE.</span><span class="sxs-lookup"><span data-stu-id="46863-155">The client must call **DdeReconnect** from within its DDE callback function.</span></span>

## <a name="multiple-conversations"></a><span data-ttu-id="46863-156">Várias conversas</span><span class="sxs-lookup"><span data-stu-id="46863-156">Multiple Conversations</span></span>

<span data-ttu-id="46863-157">Um aplicativo cliente pode usar a função [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para determinar se algum servidor de interesse está disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="46863-157">A client application can use the [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function to determine whether any servers of interest are available in the system.</span></span> <span data-ttu-id="46863-158">Um cliente especifica um nome de serviço e nome de tópico quando chama **DdeConnectList**, fazendo com que o ddeml transmita a transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para as funções de retorno de chamada DDE de todos os servidores que correspondem ao nome do serviço (exceto aqueles que filtram a transação).</span><span class="sxs-lookup"><span data-stu-id="46863-158">A client specifies a service name and topic name when it calls **DdeConnectList**, causing the DDEML to broadcast the [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction to the DDE callback functions of all servers that match the service name (except those that filter the transaction).</span></span> <span data-ttu-id="46863-159">A função de retorno de chamada de um servidor deve retornar um identificador de dados que identifica uma matriz terminada em nulo de estruturas [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="46863-159">A server's callback function should return a data handle that identifies a null-terminated array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="46863-160">A matriz deve conter uma estrutura para cada nome de serviço e par de nome de tópico que corresponda ao par especificado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="46863-160">The array should contain one structure for each service name and topic name pair that matches the pair specified by the client.</span></span> <span data-ttu-id="46863-161">O DDEML estabelece uma conversa para cada estrutura **HSZPAIR** preenchida pelo servidor e retorna um identificador de lista de conversa para o cliente.</span><span class="sxs-lookup"><span data-stu-id="46863-161">The DDEML establishes a conversation for each **HSZPAIR** structure filled by the server and returns a conversation list handle to the client.</span></span> <span data-ttu-id="46863-162">O servidor recebe o identificador de conversa por meio da transação [**XTYP \_ Connect**](xtyp-connect.md) (a menos que o servidor filtre essa transação).</span><span class="sxs-lookup"><span data-stu-id="46863-162">The server receives the conversation handle by way of the [**XTYP\_CONNECT**](xtyp-connect.md) transaction (unless the server filters this transaction).</span></span>

<span data-ttu-id="46863-163">Um cliente pode especificar **NULL** para o nome do serviço, o nome do tópico ou ambos ao chamar [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="46863-163">A client can specify **NULL** for the service name, topic name, or both when it calls [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="46863-164">Se o nome do serviço for **nulo**, todos os servidores no sistema que dão suporte ao nome do tópico especificado responderão.</span><span class="sxs-lookup"><span data-stu-id="46863-164">If the service name is **NULL**, all servers in the system that support the specified topic name respond.</span></span> <span data-ttu-id="46863-165">Uma conversa é estabelecida com cada servidor de resposta, incluindo várias instâncias do mesmo servidor.</span><span class="sxs-lookup"><span data-stu-id="46863-165">A conversation is established with each responding server, including multiple instances of the same server.</span></span> <span data-ttu-id="46863-166">Se o nome do tópico for **nulo**, uma conversa será estabelecida em cada tópico reconhecido por cada servidor que corresponde ao nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="46863-166">If the topic name is **NULL**, a conversation is established on each topic recognized by each server that matches the service name.</span></span>

<span data-ttu-id="46863-167">Um cliente pode usar as funções [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para identificar os servidores que respondem ao [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="46863-167">A client can use the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to identify the servers that respond to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="46863-168">**DdeQueryNextServer** retorna o próximo identificador de conversa em uma lista de conversa e **DdeQueryConvInfo** preenche uma estrutura [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) com informações sobre a conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-168">**DdeQueryNextServer** returns the next conversation handle in a conversation list, and **DdeQueryConvInfo** fills a [**CONVINFO**](/windows/win32/api/ddeml/ns-ddeml-convinfo) structure with information about the conversation.</span></span> <span data-ttu-id="46863-169">O cliente pode manter os identificadores de conversa necessários e descartar o restante da lista de conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-169">The client can keep the conversation handles that it needs and discard the rest from the conversation list.</span></span>

<span data-ttu-id="46863-170">O exemplo a seguir usa [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) para estabelecer conversas com todos os servidores que dão suporte ao tópico System e, em seguida, usa as funções [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) e [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) para obter os identificadores de cadeia de caracteres de nome de serviço dos servidores e armazená-los em um buffer.</span><span class="sxs-lookup"><span data-stu-id="46863-170">The following example uses [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) to establish conversations with all servers that support the System topic and then uses the [**DdeQueryNextServer**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver) and [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) functions to obtain the servers' service name string handles and store them in a buffer.</span></span>


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



<span data-ttu-id="46863-171">Um aplicativo pode encerrar uma conversa individual em uma lista de conversa chamando a função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) .</span><span class="sxs-lookup"><span data-stu-id="46863-171">An application can terminate an individual conversation in a conversation list by calling the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function.</span></span> <span data-ttu-id="46863-172">Um aplicativo pode encerrar todas as conversas em uma lista de conversa chamando a função [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="46863-172">An application can terminate all conversations in a conversation list by calling the [**DdeDisconnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist) function.</span></span> <span data-ttu-id="46863-173">Ambas as funções fazem com que o DDEML envie transações de [**\_ desconexão XTYP**](xtyp-disconnect.md) para a função de retorno de chamada DDE de cada parceiro.</span><span class="sxs-lookup"><span data-stu-id="46863-173">Both functions cause the DDEML to send [**XTYP\_DISCONNECT**](xtyp-disconnect.md) transactions to each partner's DDE callback function.</span></span> <span data-ttu-id="46863-174">**DdeDisconnectList** envia uma transação de **\_ desconexão XTYP** para cada identificador de conversa na lista.</span><span class="sxs-lookup"><span data-stu-id="46863-174">**DdeDisconnectList** sends an **XTYP\_DISCONNECT** transaction for each conversation handle in the list.</span></span>

<span data-ttu-id="46863-175">Um cliente pode recuperar uma lista de identificadores de conversa em uma lista de conversa passando um identificador de lista de conversa existente para [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span><span class="sxs-lookup"><span data-stu-id="46863-175">A client can retrieve a list of the conversation handles in a conversation list by passing an existing conversation list handle to [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist).</span></span> <span data-ttu-id="46863-176">O processo de enumeração remove os identificadores de conversas encerradas da lista e as conversas não duplicadas que se ajustam ao nome do serviço e ao nome do tópico especificados são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="46863-176">The enumeration process removes the handles of terminated conversations from the list, and nonduplicate conversations that fit the specified service name and topic name are added.</span></span>

<span data-ttu-id="46863-177">Se [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) especificar um identificador de lista de conversa existente, a função criará uma nova lista de conversa que contém os identificadores de novas conversas e os identificadores da lista existente.</span><span class="sxs-lookup"><span data-stu-id="46863-177">If [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) specifies an existing conversation list handle, the function creates a new conversation list that contains the handles of any new conversations and the handles from the existing list.</span></span>

<span data-ttu-id="46863-178">Se houver conversas duplicadas, o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) tentará impedir identificadores de conversa duplicados na lista de conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-178">If duplicate conversations exist, [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) attempts to prevent duplicate conversation handles in the conversation list.</span></span> <span data-ttu-id="46863-179">Uma conversa duplicada é uma segunda conversa com o mesmo servidor no mesmo nome de serviço e nome de tópico.</span><span class="sxs-lookup"><span data-stu-id="46863-179">A duplicate conversation is a second conversation with the same server on the same service name and topic name.</span></span> <span data-ttu-id="46863-180">Duas conversas desse tipo teriam identificadores diferentes, ainda que identifiquem a mesma conversa.</span><span class="sxs-lookup"><span data-stu-id="46863-180">Two such conversations would have different handles, yet they would identify the same conversation.</span></span>

 

 




