---
title: Usando troca dinâmica de dados
description: Este tópico fornece exemplos de código relacionados à troca de dados dinâmicas.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Troca dinâmica de dados (DDE), conversas
- DDE (troca dinâmica de dados), conversas
- troca de dados, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), exemplos
- DDE (troca dinâmica de dados), exemplos
- Troca dinâmica de dados (DDE), comandos em aplicativos de servidor
- DDE (troca dinâmica de dados), comandos em aplicativos de servidor
- Troca dinâmica de dados (DDE), links de dados
- DDE (troca dinâmica de dados), links de dados
- Troca dinâmica de dados (DDE), itens
- DDE (troca dinâmica de dados), itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe20c4dedc38303fe9bcb9c4b0fae42d03ee536
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294169"
---
# <a name="using-dynamic-data-exchange"></a><span data-ttu-id="de79d-114">Usando troca dinâmica de dados</span><span class="sxs-lookup"><span data-stu-id="de79d-114">Using Dynamic Data Exchange</span></span>

<span data-ttu-id="de79d-115">Esta seção tem exemplos de código sobre as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="de79d-115">This section has code samples on the following tasks:</span></span>

-   [<span data-ttu-id="de79d-116">Iniciando uma conversa</span><span class="sxs-lookup"><span data-stu-id="de79d-116">Initiating a Conversation</span></span>](#initiating-a-conversation)
-   [<span data-ttu-id="de79d-117">Transferindo um único item</span><span class="sxs-lookup"><span data-stu-id="de79d-117">Transferring a Single Item</span></span>](#transferring-a-single-item)
    -   [<span data-ttu-id="de79d-118">Recuperando um item do servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-118">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
    -   [<span data-ttu-id="de79d-119">Enviando um item para o servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-119">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)
-   [<span data-ttu-id="de79d-120">Estabelecendo um link de dados permanente</span><span class="sxs-lookup"><span data-stu-id="de79d-120">Establishing a Permanent Data Link</span></span>](#establishing-a-permanent-data-link)
    -   [<span data-ttu-id="de79d-121">Iniciando um link de dados</span><span class="sxs-lookup"><span data-stu-id="de79d-121">Initiating a Data Link</span></span>](#initiating-a-data-link)
    -   [<span data-ttu-id="de79d-122">Iniciando um link de dados com o comando Colar vínculo</span><span class="sxs-lookup"><span data-stu-id="de79d-122">Initiating a Data Link with the Paste Link Command</span></span>](#initiating-a-data-link-with-the-paste-link-command)
    -   [<span data-ttu-id="de79d-123">Notificando o cliente que os dados foram alterados</span><span class="sxs-lookup"><span data-stu-id="de79d-123">Notifying the Client that Data Has Changed</span></span>](#notifying-the-client-that-data-has-changed)
    -   [<span data-ttu-id="de79d-124">Encerrando um link de dados</span><span class="sxs-lookup"><span data-stu-id="de79d-124">Terminating a Data Link</span></span>](#terminating-a-data-link)
-   [<span data-ttu-id="de79d-125">Executando comandos em um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-125">Carrying Out Commands in a Server Application</span></span>](#carrying-out-commands-in-a-server-application)
-   [<span data-ttu-id="de79d-126">Encerrando uma conversa</span><span class="sxs-lookup"><span data-stu-id="de79d-126">Terminating a Conversation</span></span>](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a><span data-ttu-id="de79d-127">Iniciando uma conversa</span><span class="sxs-lookup"><span data-stu-id="de79d-127">Initiating a Conversation</span></span>

<span data-ttu-id="de79d-128">Para iniciar uma conversa de troca dinâmica de dados (DDE), o cliente envia uma mensagem de [**\_ \_ inicialização do WM DDE**](wm-dde-initiate.md) .</span><span class="sxs-lookup"><span data-stu-id="de79d-128">To initiate a Dynamic Data Exchange (DDE) conversation, the client sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message.</span></span> <span data-ttu-id="de79d-129">Normalmente, o cliente transmite essa mensagem chamando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), com – 1 como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de79d-129">Usually, the client broadcasts this message by calling [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), with –1 as the first parameter.</span></span> <span data-ttu-id="de79d-130">Se o aplicativo já tiver o identificador de janela para o aplicativo de servidor, ele poderá enviar a mensagem diretamente para essa janela.</span><span class="sxs-lookup"><span data-stu-id="de79d-130">If the application already has the window handle to the server application, it can send the message directly to that window.</span></span> <span data-ttu-id="de79d-131">O cliente prepara os átomos para o nome do aplicativo e o nome do tópico chamando [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span><span class="sxs-lookup"><span data-stu-id="de79d-131">The client prepares atoms for the application name and topic name by calling [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma).</span></span> <span data-ttu-id="de79d-132">O cliente pode solicitar conversas com qualquer aplicativo de servidor em potencial e para qualquer tópico em potencial fornecendo Atoms **nulos** (curinga) para o aplicativo e o tópico.</span><span class="sxs-lookup"><span data-stu-id="de79d-132">The client can request conversations with any potential server application and for any potential topic by supplying **NULL** (wildcard) atoms for the application and topic.</span></span>

<span data-ttu-id="de79d-133">O exemplo a seguir ilustra como o cliente inicia uma conversa, onde o aplicativo e o tópico são especificados.</span><span class="sxs-lookup"><span data-stu-id="de79d-133">The following example illustrates how the client initiates a conversation, where both the application and topic are specified.</span></span>


```
    static BOOL fInInitiate = FALSE; 
    char *szApplication; 
    char *szTopic; 
    atomApplication = *szApplication == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szApplication); 
    atomTopic = *szTopic == 0 ? 
    NULL     : GlobalAddAtom((LPSTR) szTopic); 
 
    fInInitiate = TRUE; 
    SendMessage((HWND) HWND_BROADCAST, // broadcasts message 
        WM_DDE_INITIATE,               // initiates conversation 
        (WPARAM) hwndClientDDE,        // handle to client DDE window 
        MAKELONG(atomApplication,      // application-name atom 
            atomTopic));               // topic-name atom 
    fInInitiate = FALSE; 
    if (atomApplication != NULL) 
        GlobalDeleteAtom(atomApplication); 
    if (atomTopic != NULL) 
        GlobalDeleteAtom(atomTopic);
```



> [!Note]  
> <span data-ttu-id="de79d-134">Se seu aplicativo usar Atoms **nulos** , você não precisará usar as funções [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) e [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) .</span><span class="sxs-lookup"><span data-stu-id="de79d-134">If your application uses **NULL** atoms, you need not use the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) and [**GlobalDeleteAtom**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) functions.</span></span> <span data-ttu-id="de79d-135">Neste exemplo, o aplicativo cliente cria dois átomos globais contendo o nome do servidor e o nome do tópico, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="de79d-135">In this example, the client application creates two global atoms containing the name of the server and the name of the topic, respectively.</span></span>

 

<span data-ttu-id="de79d-136">O aplicativo cliente envia uma mensagem de [**\_ \_ inicialização do WM DDE**](wm-dde-initiate.md) com esses dois átomos no parâmetro *lParam* da mensagem.</span><span class="sxs-lookup"><span data-stu-id="de79d-136">The client application sends a [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message with these two atoms in the *lParam* parameter of the message.</span></span> <span data-ttu-id="de79d-137">Na chamada para a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , o identificador de janela especial – 1 direciona o sistema para enviar essa mensagem a todos os outros aplicativos ativos.</span><span class="sxs-lookup"><span data-stu-id="de79d-137">In the call to the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, the special window handle –1 directs the system to send this message to all other active applications.</span></span> <span data-ttu-id="de79d-138">**SendMessage** não retorna ao aplicativo cliente até que todos os aplicativos que receberem a mensagem tenham, por sua vez, retornado o controle para o sistema.</span><span class="sxs-lookup"><span data-stu-id="de79d-138">**SendMessage** does not return to the client application until all applications that receive the message have, in turn, returned control to the system.</span></span> <span data-ttu-id="de79d-139">Isso significa que todas as mensagens de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) enviadas em resposta pelos aplicativos do servidor têm a garantia de terem sido processadas pelo cliente no momento em que a chamada **SendMessage** foi retornada.</span><span class="sxs-lookup"><span data-stu-id="de79d-139">This means that all [**WM\_DDE\_ACK**](wm-dde-ack.md) messages sent in reply by the server applications are guaranteed to have been processed by the client by the time the **SendMessage** call has returned.</span></span>

<span data-ttu-id="de79d-140">Após o [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retornar, o aplicativo cliente exclui os átomos globais.</span><span class="sxs-lookup"><span data-stu-id="de79d-140">After [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application deletes the global atoms.</span></span>

<span data-ttu-id="de79d-141">Os aplicativos de servidor respondem de acordo com a lógica ilustrada no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-141">Server applications respond according to the logic illustrated in the following diagram.</span></span>

![lógica de resposta do aplicativo do servidor](images/csdde-01.png)

<span data-ttu-id="de79d-143">Para reconhecer um ou mais tópicos, o servidor deve criar Atoms para cada conversa (exigindo Atoms de nome de aplicativo duplicados se houver vários tópicos) e enviar uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para cada conversa, conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-143">To acknowledge one or more topics, the server must create atoms for each conversation (requiring duplicate application-name atoms if there are multiple topics) and send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each conversation, as illustrated in the following example.</span></span>


```
if ((atomApplication = GlobalAddAtom("Server")) != 0) 
{ 
    if ((atomTopic = GlobalAddAtom(szTopic)) != 0) 
    { 
        SendMessage(hwndClientDDE, 
            WM_DDE_ACK, 
            (WPARAM) hwndServerDDE, 
            MAKELONG(atomApplication, atomTopic)); 
        GlobalDeleteAtom(atomApplication); 
    } 
 
    GlobalDeleteAtom(atomTopic); 
} 
 
if ((atomApplication == 0) || (atomTopic == 0)) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="de79d-144">Quando um servidor responde com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) , o aplicativo cliente deve salvar um identificador na janela do servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-144">When a server responds with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client application should save a handle to the server window.</span></span> <span data-ttu-id="de79d-145">O cliente que recebe o identificador como o parâmetro *wParam* da mensagem de **\_ \_ ACK DDE do WM** envia, então, todas as mensagens de DDE subsequentes para a janela do servidor identificada por esse identificador.</span><span class="sxs-lookup"><span data-stu-id="de79d-145">The client receiving the handle as the *wParam* parameter of the **WM\_DDE\_ACK** message then sends all subsequent DDE messages to the server window this handle identifies.</span></span>

<span data-ttu-id="de79d-146">Se o aplicativo cliente usar um átomo **nulo** para o nome do aplicativo ou nome do tópico, espere que o aplicativo receba confirmações de mais de um aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-146">If your client application uses a **NULL** atom for the application name or topic name, expect the application to receive acknowledgments from more than one server application.</span></span> <span data-ttu-id="de79d-147">Várias confirmações também podem vir de várias instâncias de um servidor DDE, mesmo que o aplicativo cliente não use Atoms em **nulo** .</span><span class="sxs-lookup"><span data-stu-id="de79d-147">Multiple acknowledgements can also come from multiple instances of a DDE server, even if your client application does not **NULL** use atoms.</span></span> <span data-ttu-id="de79d-148">Um servidor sempre deve usar uma janela exclusiva para cada conversa.</span><span class="sxs-lookup"><span data-stu-id="de79d-148">A server should always use a unique window for each conversation.</span></span> <span data-ttu-id="de79d-149">O procedimento de janela no aplicativo cliente pode usar um identificador para a janela do servidor (fornecido como o parâmetro *lParam* do [**WM \_ DDE \_ Iniciar**](wm-dde-initiate.md)) para rastrear várias conversas.</span><span class="sxs-lookup"><span data-stu-id="de79d-149">The window procedure in the client application can use a handle to the server window (provided as the *lParam* parameter of [**WM\_DDE\_INITIATE**](wm-dde-initiate.md)) to track multiple conversations.</span></span> <span data-ttu-id="de79d-150">Isso permite que uma única janela de cliente processe várias conversas sem precisar encerrar e reconectar-se com uma nova janela de cliente para cada conversa.</span><span class="sxs-lookup"><span data-stu-id="de79d-150">This allows a single client window to process several conversations without needing to terminate and reconnect with a new client window for each conversation.</span></span>

## <a name="transferring-a-single-item"></a><span data-ttu-id="de79d-151">Transferindo um único item</span><span class="sxs-lookup"><span data-stu-id="de79d-151">Transferring a Single Item</span></span>

<span data-ttu-id="de79d-152">Depois que uma conversa DDE for estabelecida, o cliente poderá recuperar o valor de um item de dados do servidor emitindo a mensagem de [**\_ \_ solicitação de DDE do WM**](wm-dde-request.md) ou enviar um valor de item de dados para o servidor emitindo o [**WM \_ DDE \_**](wm-dde-poke.md)enviar.</span><span class="sxs-lookup"><span data-stu-id="de79d-152">Once a DDE conversation has been established, the client can either retrieve the value of a data item from the server by issuing the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or submit a data-item value to the server by issuing [**WM\_DDE\_POKE**](wm-dde-poke.md).</span></span>

-   [<span data-ttu-id="de79d-153">Recuperando um item do servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-153">Retrieving an Item from the Server</span></span>](#retrieving-an-item-from-the-server)
-   [<span data-ttu-id="de79d-154">Enviando um item para o servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-154">Submitting an Item to the Server</span></span>](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a><span data-ttu-id="de79d-155">Recuperando um item do servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-155">Retrieving an Item from the Server</span></span>

<span data-ttu-id="de79d-156">Para recuperar um item do servidor, o cliente envia ao servidor uma mensagem [**de \_ \_ solicitação DDE do WM**](wm-dde-request.md) especificando o item e o formato a serem recuperados, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-156">To retrieve an item from the server, the client sends the server a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message specifying the item and format to retrieve, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_REQUEST, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_REQUEST, CF_TEXT, atomItem))) 
    {
        GlobalDeleteAtom(atomItem); 
    }
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="de79d-157">Neste exemplo, o cliente especifica o formato de área de transferência **\_ texto CF** como o formato preferencial para o item de dados solicitado.</span><span class="sxs-lookup"><span data-stu-id="de79d-157">In this example, the client specifies the clipboard format **CF\_TEXT** as the preferred format for the requested data item.</span></span>

<span data-ttu-id="de79d-158">O receptor (servidor) da mensagem [**de \_ \_ solicitação de DDE do WM**](wm-dde-request.md) normalmente deve excluir o Atom do item, mas se a chamada de [**mensagem**](/windows/desktop/api/winuser/nf-winuser-postmessagea) falhar, o cliente deverá excluir o Atom.</span><span class="sxs-lookup"><span data-stu-id="de79d-158">The receiver (server) of the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message typically must delete the item atom, but if the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) call fails, the client must delete the atom.</span></span>

<span data-ttu-id="de79d-159">Se o servidor tiver acesso ao item solicitado e puder renderizá-lo no formato solicitado, o servidor copiará o valor do item como um objeto de memória compartilhada e enviará ao cliente uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) , conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-159">If the server has access to the requested item and can render it in the requested format, the server copies the item value as a shared memory object and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as illustrated in the following example.</span></span>


```
// Allocate the size of the DDE data header, plus the data: a 
// string,<CR><LF><NULL>. The byte for the string's terminating 
// null character is counted by DDEDATA.Value[1].

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEDATA) + *pcch + 2)))  
{
    return; 
}
 
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData)))  
{
    GlobalFree(hData); 
    return; 
} 
 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpData->Value, *pcch +1, (LPCSTR) szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
} 
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItemName)) != 0) 
{ 
    lParam = PackDDElParam(WM_DDE_ACK, (UINT) hData, atomItem); 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            lParam)) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_ACK, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors.  
}
```



<span data-ttu-id="de79d-160">Neste exemplo, o aplicativo de servidor aloca um objeto de memória para conter o item de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-160">In this example, the server application allocates a memory object to contain the data item.</span></span> <span data-ttu-id="de79d-161">O objeto de dados é inicializado como uma estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="de79d-161">The data object is initialized as a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span>

<span data-ttu-id="de79d-162">Em seguida, o aplicativo de servidor define o membro **cfFormat** da estrutura como texto de CF \_ para informar ao aplicativo cliente que os dados estão em formato de texto.</span><span class="sxs-lookup"><span data-stu-id="de79d-162">The server application then sets the **cfFormat** member of the structure to CF\_TEXT to inform the client application that the data is in text format.</span></span> <span data-ttu-id="de79d-163">O cliente responde copiando o valor dos dados solicitados para o membro de **valor** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) .</span><span class="sxs-lookup"><span data-stu-id="de79d-163">The client responds by copying the value of the requested data into the **Value** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure.</span></span> <span data-ttu-id="de79d-164">Depois que o servidor preencher o objeto de dados, o servidor desbloqueará os dados e criará um átomo global que contém o nome do item de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-164">After the server has filled the data object, the server unlocks the data and creates a global atom containing the name of the data item.</span></span>

<span data-ttu-id="de79d-165">Por fim, o servidor emite a mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) chamando a [**mensagem**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span><span class="sxs-lookup"><span data-stu-id="de79d-165">Finally, the server issues the [**WM\_DDE\_DATA**](wm-dde-data.md) message by calling [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea).</span></span> <span data-ttu-id="de79d-166">O identificador para o objeto de dados e o Atom que contém o nome do item são incluídos no parâmetro *lParam* da mensagem pela função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) .</span><span class="sxs-lookup"><span data-stu-id="de79d-166">The handle to the data object and the atom containing the item name are packed into the *lParam* parameter of the message by the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function.</span></span>

<span data-ttu-id="de79d-167">Se a [**mensagem**](/windows/desktop/api/winuser/nf-winuser-postmessagea) falhar, o servidor deverá usar a função [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) para liberar o parâmetro *lParam* embalado.</span><span class="sxs-lookup"><span data-stu-id="de79d-167">If [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) fails, the server must use the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function to free the packed *lParam* parameter.</span></span> <span data-ttu-id="de79d-168">O servidor também deve liberar o parâmetro *lParam* embalado para a mensagem de [**\_ \_ solicitação DDE do WM**](wm-dde-request.md) recebido.</span><span class="sxs-lookup"><span data-stu-id="de79d-168">The server must also free the packed *lParam* parameter for the [**WM\_DDE\_REQUEST**](wm-dde-request.md) message it received.</span></span>

<span data-ttu-id="de79d-169">Se o servidor não puder atender à solicitação, ele enviará uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa para o cliente, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-169">If the server cannot satisfy the request, it sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the client, as shown in the following example.</span></span>


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



<span data-ttu-id="de79d-170">Após receber uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) , o cliente processa o valor do item de dados conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="de79d-170">Upon receiving a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the client processes the data-item value as appropriate.</span></span> <span data-ttu-id="de79d-171">Em seguida, se o membro **fAckReq** apontado na mensagem de **\_ \_ dados DDE do WM** for 1, o cliente deverá enviar ao servidor uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-171">Then, if the **fAckReq** member pointed to in the **WM\_DDE\_DATA** message is 1, the client must send the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message, as shown in the following example.</span></span>


```
UnpackDDElParam(WM_DDE_DATA, lParam, (PUINT) &hData, 
    (PUINT) &atomItem); 
if (!(lpDDEData = (DDEDATA FAR*) GlobalLock(hData)) 
        || (lpDDEData->cfFormat != CF_TEXT)) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // Negative ACK. 
} 
 
// Copy data from lpDDEData here. 
 
if (lpDDEData->fAckReq) 
{ 
    PostMessage(hwndServerDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_ACK, 0x8000, 
            atomItem)); // Positive ACK 
} 
 
bRelease = lpDDEData->fRelease; 
GlobalUnlock(hData); 
if (bRelease) 
    GlobalFree(hData);
```



<span data-ttu-id="de79d-172">Neste exemplo, o cliente examina o formato dos dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-172">In this example, the client examines the format of the data.</span></span> <span data-ttu-id="de79d-173">Se o formato não for **um \_ texto de CF** (ou se o cliente não puder bloquear a memória para os dados), o cliente enviará uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa para indicar que ele não pode processar os dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-173">If the format is not **CF\_TEXT** (or if the client cannot lock the memory for the data), the client sends a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message to indicate that it cannot process the data.</span></span> <span data-ttu-id="de79d-174">Se o cliente não puder bloquear um identificador de dados porque o identificador contém o membro **fAckReq** , o cliente não deverá enviar uma mensagem de **\_ \_ confirmação DDE do WM** negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-174">If the client cannot lock a data handle because the handle contains the **fAckReq** member, the client should not send a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="de79d-175">Em vez disso, o cliente deve encerrar a conversa.</span><span class="sxs-lookup"><span data-stu-id="de79d-175">Instead, the client should terminate the conversation.</span></span>

<span data-ttu-id="de79d-176">Se um cliente enviar uma confirmação negativa em resposta a uma mensagem [**de \_ \_ dados DDE do WM**](wm-dde-data.md) , o servidor será responsável por liberar a memória (mas não o parâmetro *lParam* ) referenciado pela mensagem de **\_ \_ dados DDE do WM** associada à confirmação negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-176">If a client sends a negative acknowledgment in response to a [**WM\_DDE\_DATA**](wm-dde-data.md) message, the server is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_DATA** message associated with the negative acknowledgment.</span></span>

<span data-ttu-id="de79d-177">Se ele puder processar os dados, o cliente examinará o membro **fAckReq** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) para determinar se o servidor solicitou que ele seja informado de que o cliente recebeu e processou os dados com êxito.</span><span class="sxs-lookup"><span data-stu-id="de79d-177">If it can process the data, the client examines the **fAckReq** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to determine whether the server requested that it be informed that the client received and processed the data successfully.</span></span> <span data-ttu-id="de79d-178">Se o servidor solicitou essas informações, o cliente envia ao servidor uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva.</span><span class="sxs-lookup"><span data-stu-id="de79d-178">If the server did request this information, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="de79d-179">Como o desbloqueio de dados invalida o ponteiro para os dados, o cliente salva o valor do membro **fRelease** antes de desbloquear o objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-179">Because unlocking data invalidates the pointer to the data, the client saves the value of the **fRelease** member before unlocking the data object.</span></span> <span data-ttu-id="de79d-180">Depois de salvar o valor, o cliente o examina para determinar se o aplicativo de servidor solicitou que o cliente liberasse a memória que contém os dados; o cliente age de acordo.</span><span class="sxs-lookup"><span data-stu-id="de79d-180">After saving the value, the client then examines it to determine whether the server application requested the client to free the memory containing the data; the client acts accordingly.</span></span>

<span data-ttu-id="de79d-181">Depois de receber uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa, o cliente pode solicitar o mesmo valor de item novamente, especificando um formato de área de transferência diferente.</span><span class="sxs-lookup"><span data-stu-id="de79d-181">Upon receiving a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the client can ask for the same item value again, specifying a different clipboard format.</span></span> <span data-ttu-id="de79d-182">Normalmente, um cliente primeiro solicitará o formato mais complexo ao qual ele pode dar suporte e, em seguida, fará uma busca detalhada, se necessário, por meio de formatos progressivamente mais simples até encontrar um que o servidor possa fornecer.</span><span class="sxs-lookup"><span data-stu-id="de79d-182">Typically, a client will first ask for the most complex format it can support, then step down if necessary through progressively simpler formats until it finds one the server can provide.</span></span>

<span data-ttu-id="de79d-183">Se o servidor oferecer suporte ao item de formatos do tópico System, o cliente poderá determinar quando os formatos de área de transferência são compatíveis com o servidor, em vez de predeterminar cada vez que o cliente solicita um item.</span><span class="sxs-lookup"><span data-stu-id="de79d-183">If the server supports the Formats item of the system topic, the client can determine once what clipboard formats the server supports, instead of determining them each time the client requests an item.</span></span>

### <a name="submitting-an-item-to-the-server"></a><span data-ttu-id="de79d-184">Enviando um item para o servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-184">Submitting an Item to the Server</span></span>

<span data-ttu-id="de79d-185">O cliente pode enviar um valor de item para o servidor usando a mensagem de envio de [**\_ \_ DDE do WM**](wm-dde-poke.md) .</span><span class="sxs-lookup"><span data-stu-id="de79d-185">The client may send an item value to the server by using the [**WM\_DDE\_POKE**](wm-dde-poke.md) message.</span></span> <span data-ttu-id="de79d-186">O cliente renderiza o item a ser enviado e envia a mensagem de envio de **\_ \_ DDE do WM** , conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-186">The client renders the item to be sent and sends the **WM\_DDE\_POKE** message, as illustrated in the following example.</span></span>


```
size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hPokeData = GlobalAlloc(GMEM_MOVEABLE,
  (LONG) sizeof(DDEPOKE) + *pcch + 2))) 
{
    return; 
}
 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData))) 
{ 
    GlobalFree(hPokeData); 
    return; 
} 
 
lpPokeData->fRelease = TRUE; 
lpPokeData->cfFormat = CF_TEXT;
hResult = StringCchCopy((LPSTR) lpPokeData->Value, *pcch +1, (LPCSTR) szValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
 
// Each line of CF_TEXT data is terminated by CR/LF. 
hResult = StringCchCat((LPSTR) lpPokeData->Value, *pcch + 3, (LPCSTR) "\r\n");
if (FAILED(hResult)
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hPokeData); 
if ((atomItem = GlobalAddAtom((LPSTR) szItem)) != 0) 
{ 
 
        if (!PostMessage(hwndServerDDE, 
                WM_DDE_POKE, 
                (WPARAM) hwndClientDDE, 
                PackDDElParam(WM_DDE_POKE, (UINT) hPokeData, 
                    atomItem))) 
        { 
            GlobalDeleteAtom(atomItem); 
            GlobalFree(hPokeData); 
        } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
} 
```



> [!Note]  
> <span data-ttu-id="de79d-187">O envio de dados por meio de uma mensagem do [**WM \_ DDE \_**](wm-dde-poke.md) enviar é essencialmente o mesmo que enviá-lo usando [**\_ \_ dados DDE do WM**](wm-dde-data.md), exceto pelo fato de que o **WM \_ DDE \_** enviar é enviado do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-187">Sending data by using a [**WM\_DDE\_POKE**](wm-dde-poke.md) message is essentially the same as sending it by using [**WM\_DDE\_DATA**](wm-dde-data.md), except that **WM\_DDE\_POKE** is sent from the client to the server.</span></span>

 

<span data-ttu-id="de79d-188">Se o servidor for capaz de aceitar o valor de item de dados no formato renderizado pelo cliente, o servidor processará o valor do item conforme apropriado e enviará ao cliente uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva.</span><span class="sxs-lookup"><span data-stu-id="de79d-188">If the server is able to accept the data-item value in the format rendered by the client, the server processes the item value as appropriate and sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="de79d-189">Se não for possível processar o valor do item, por causa de seu formato ou por outros motivos, o servidor enviará ao cliente uma mensagem de **\_ \_ ACK DDE do WM** negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-189">If it is unable to process the item value, because of its format or for other reasons, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>


```
UnpackDDElParam(WM_DDE_POKE, lParam, (PUINT) &hPokeData, 
    (PUINT) &atomItem); 
GlobalGetAtomName(atomItem, szItemName, ITEM_NAME_MAX_SIZE); 
if (!(lpPokeData = (DDEPOKE *) GlobalLock(hPokeData)) 
        || lpPokeData->cfFormat != CF_TEXT 
        || !IsItemSupportedByServer(szItemName)) 
{ 
    PostMessage(hwndClientDDE, 
        WM_DDE_ACK, 
        (WPARAM) hwndServerDDE, 
        PackDDElParam(WM_DDE_ACK, 0, atomItem)); // negative ACK  
}
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
} 
hResult = StringCchCopy(szItemValue, *pcch +1, lpPokeData->Value); // copies value 
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}  
bRelease = lpPokeData->fRelease; 
GlobalUnlock(hPokeData); 
if (bRelease) 
{ 
    GlobalFree(hPokeData); 
} 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 
         0x8000, atomItem));    // positive ACK.
```



<span data-ttu-id="de79d-190">Neste exemplo, o servidor chama [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar o nome do item que o cliente enviou.</span><span class="sxs-lookup"><span data-stu-id="de79d-190">In this example, the server calls [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) to retrieve the name of the item the client sent.</span></span> <span data-ttu-id="de79d-191">Em seguida, o servidor determina se ele dá suporte ao item e se o item é renderizado no formato correto (ou seja, o texto do CF \_ ).</span><span class="sxs-lookup"><span data-stu-id="de79d-191">The server then determines whether it supports the item and whether the item is rendered in the correct format (that is, CF\_TEXT).</span></span> <span data-ttu-id="de79d-192">Se o item não tiver suporte e não for renderizado no formato correto, ou se o servidor não puder bloquear a memória para os dados, o servidor enviará uma confirmação negativa de volta para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="de79d-192">If the item is not supported and not rendered in the correct format, or if the server cannot lock the memory for the data, the server sends a negative acknowledgment back to the client application.</span></span> <span data-ttu-id="de79d-193">Observe que, nesse caso, o envio de uma confirmação negativa está correto porque as mensagens do [**WM \_ \_ DDE**](wm-dde-poke.md) para enviar são sempre presumidas para ter o membro **fAckReq** definido.</span><span class="sxs-lookup"><span data-stu-id="de79d-193">Note that in this case, sending a negative acknowledgment is correct because [**WM\_DDE\_POKE**](wm-dde-poke.md) messages are always assumed to have the **fAckReq** member set.</span></span> <span data-ttu-id="de79d-194">O servidor deve ignorar o membro.</span><span class="sxs-lookup"><span data-stu-id="de79d-194">The server should ignore the member.</span></span>

<span data-ttu-id="de79d-195">Se um servidor enviar uma confirmação negativa em resposta a uma mensagem de envio de [**\_ DDE \_ do WM**](wm-dde-poke.md) , o cliente será responsável por liberar a memória (mas não o parâmetro *lParam* ) referenciado pela mensagem de envio de **\_ DDE \_ do WM** associada à confirmação negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-195">If a server sends a negative acknowledgment in response to a [**WM\_DDE\_POKE**](wm-dde-poke.md) message, the client is responsible for freeing the memory (but not the *lParam* parameter) referenced by the **WM\_DDE\_POKE** message associated with the negative acknowledgment.</span></span>

## <a name="establishing-a-permanent-data-link"></a><span data-ttu-id="de79d-196">Estabelecendo um link de dados permanente</span><span class="sxs-lookup"><span data-stu-id="de79d-196">Establishing a Permanent Data Link</span></span>

<span data-ttu-id="de79d-197">Um aplicativo cliente pode usar o DDE para estabelecer um link para um item em um aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-197">A client application can use DDE to establish a link to an item in a server application.</span></span> <span data-ttu-id="de79d-198">Depois que esse link é estabelecido, o servidor envia atualizações periódicas do item vinculado para o cliente, normalmente, sempre que o valor do item é alterado.</span><span class="sxs-lookup"><span data-stu-id="de79d-198">After such a link is established, the server sends periodic updates of the linked item to the client, typically, whenever the value of the item changes.</span></span> <span data-ttu-id="de79d-199">Portanto, um fluxo de dados permanente é estabelecido entre os dois aplicativos; Esse fluxo de dados permanece em vigor até que seja explicitamente desconectado.</span><span class="sxs-lookup"><span data-stu-id="de79d-199">Thus, a permanent data stream is established between the two applications; this data stream remains in place until it is explicitly disconnected.</span></span>

### <a name="initiating-a-data-link"></a><span data-ttu-id="de79d-200">Iniciando um link de dados</span><span class="sxs-lookup"><span data-stu-id="de79d-200">Initiating a Data Link</span></span>

<span data-ttu-id="de79d-201">O cliente inicia um link de dados postando uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-201">The client initiates a data link by posting a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, as shown in the following example.</span></span>


```
if (!(hOptions = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(DDEADVISE)))) 
    return; 
if (!(lpOptions = (DDEADVISE FAR*) GlobalLock(hOptions))) 
{ 
    GlobalFree(hOptions); 
    return; 
} 
 
lpOptions->cfFormat = CF_TEXT; 
lpOptions->fAckReq = TRUE; 
lpOptions->fDeferUpd = FALSE; 
GlobalUnlock(hOptions); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!(PostMessage(hwndServerDDE, 
            WM_DDE_ADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_ADVISE, (UINT) hOptions, 
                atomItem)))) 
    { 
        GlobalDeleteAtom(atomItem); 
        GlobalFree(hOptions); 
        FreeDDElParam(WM_DDE_ADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors 
 
}
```



<span data-ttu-id="de79d-202">Neste exemplo, o aplicativo cliente define o sinalizador **fDeferUpd** da mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) como **false**.</span><span class="sxs-lookup"><span data-stu-id="de79d-202">In this example, the client application sets the **fDeferUpd** flag of the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to **FALSE**.</span></span> <span data-ttu-id="de79d-203">Isso instrui o aplicativo de servidor a enviar os dados para o cliente sempre que os dados forem alterados.</span><span class="sxs-lookup"><span data-stu-id="de79d-203">This directs the server application to send the data to the client whenever the data changes.</span></span>

<span data-ttu-id="de79d-204">Se o servidor não puder atender à solicitação [**de \_ \_ aviso de DDE do WM**](wm-dde-advise.md) , ele enviará ao cliente uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-204">If the server is unable to service the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) request, it sends the client a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span> <span data-ttu-id="de79d-205">Mas se o servidor tiver acesso ao item e puder renderizá-lo no formato solicitado, o servidor notará o novo link (recuperando os sinalizadores especificados no parâmetro *hOptions* ) e enviará ao cliente uma mensagem de **\_ \_ ACK DDE do WM** positiva.</span><span class="sxs-lookup"><span data-stu-id="de79d-205">But if the server has access to the item and can render it in the requested format, the server notes the new link (recalling the flags specified in the *hOptions* parameter) and sends the client a positive **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="de79d-206">A partir do momento em diante, até que o cliente emita uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-unadvise.md) correspondente, o servidor envia os novos dados para o cliente sempre que o valor do item é alterado no servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-206">From then on, until the client issues a matching [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, the server sends the new data to the client every time the value of the item changes in the server.</span></span>

<span data-ttu-id="de79d-207">A mensagem de [**\_ \_ aviso do DDE do WM**](wm-dde-advise.md) estabelece o formato dos dados a serem trocados durante o link.</span><span class="sxs-lookup"><span data-stu-id="de79d-207">The [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message establishes the format of the data to be exchanged during the link.</span></span> <span data-ttu-id="de79d-208">Se o cliente tentar estabelecer outro link com o mesmo item, mas estiver usando um formato de dados diferente, o servidor poderá optar por rejeitar o segundo formato de dados ou tentar dar suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="de79d-208">If the client attempts to establish another link with the same item but is using a different data format, the server can choose to reject the second data format or attempt to support it.</span></span> <span data-ttu-id="de79d-209">Se um link quente tiver sido estabelecido para qualquer item de dados, o servidor poderá dar suporte a apenas um formato de dados de cada vez.</span><span class="sxs-lookup"><span data-stu-id="de79d-209">If a warm link has been established for any data item, the server can support only one data format at a time.</span></span> <span data-ttu-id="de79d-210">Isso ocorre porque a mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) para um link quente tem um identificador de dados **nulo** , que, de outra forma, contém as informações de formato.</span><span class="sxs-lookup"><span data-stu-id="de79d-210">This is because the [**WM\_DDE\_DATA**](wm-dde-data.md) message for a warm link has a **NULL** data handle, which otherwise contains the format information.</span></span> <span data-ttu-id="de79d-211">Portanto, um servidor deve rejeitar todos os links quentes de um item já vinculado e deve rejeitar todos os links para um item que tenha links quentes.</span><span class="sxs-lookup"><span data-stu-id="de79d-211">Thus, a server must reject all warm links for an item already linked, and must reject all links for an item that has warm links.</span></span> <span data-ttu-id="de79d-212">Outra interpretação pode ser que o servidor altere o formato e o estado quente ou quente de um link quando um segundo link é solicitado para o mesmo item de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-212">Another interpretation may be that the server changes the format and the hot or warm state of a link when a second link is requested for the same data item.</span></span>

<span data-ttu-id="de79d-213">Em geral, os aplicativos cliente não devem tentar estabelecer mais de um link por vez para um item de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-213">In general, client applications should not attempt to establish more than one link at a time for a data item.</span></span>

### <a name="initiating-a-data-link-with-the-paste-link-command"></a><span data-ttu-id="de79d-214">Iniciando um link de dados com o comando Colar vínculo</span><span class="sxs-lookup"><span data-stu-id="de79d-214">Initiating a Data Link with the Paste Link Command</span></span>

<span data-ttu-id="de79d-215">Os aplicativos que dão suporte a links de dados quentes ou quentes normalmente dão suporte a um formato de área de transferência registrado chamado link.</span><span class="sxs-lookup"><span data-stu-id="de79d-215">Applications that support hot or warm data links typically support a registered clipboard format named Link.</span></span> <span data-ttu-id="de79d-216">Quando associados aos comandos copiar e colar link do aplicativo, esse formato de área de transferência permite que o usuário estabeleça conversas DDE entre aplicativos simplesmente copiando um item de dados no aplicativo de servidor e colando-o no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="de79d-216">When associated with the application's Copy and Paste Link commands, this clipboard format enables the user to establish DDE conversations between applications simply by copying a data item in the server application and pasting it into the client application.</span></span>

<span data-ttu-id="de79d-217">Um aplicativo de servidor dá suporte ao formato de vínculo da área de transferência colocando na área de transferência uma cadeia de caracteres que contém o aplicativo, o tópico e os nomes de item quando o usuário escolhe o comando de **cópia** no menu **Editar** .</span><span class="sxs-lookup"><span data-stu-id="de79d-217">A server application supports the Link clipboard format by placing in the clipboard a string containing the application, topic, and item names when the user chooses the **Copy** command from the **Edit** menu.</span></span> <span data-ttu-id="de79d-218">A seguir está o formato de link padrão:</span><span class="sxs-lookup"><span data-stu-id="de79d-218">Following is the standard Link format:</span></span>

<span data-ttu-id="de79d-219">*Application ***\\ 0*** tópico ***\\ 0*** item \* \* \* \\ 0 \\ 0*\*</span><span class="sxs-lookup"><span data-stu-id="de79d-219">*application ***\\0*** topic ***\\0*** item\*\*\*\\0\\0*\*</span></span>

<span data-ttu-id="de79d-220">Um caractere nulo único separa os nomes e dois caracteres nulos encerram a cadeia de caracteres inteira.</span><span class="sxs-lookup"><span data-stu-id="de79d-220">A single null character separates the names, and two null characters terminate the entire string.</span></span>

<span data-ttu-id="de79d-221">Os aplicativos cliente e servidor devem registrar o formato da área de transferência do link, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="de79d-221">Both the client and server applications must register the Link clipboard format, as shown:</span></span>


```
cfLink = RegisterClipboardFormat("Link");
```



<span data-ttu-id="de79d-222">Um aplicativo cliente dá suporte ao formato de vínculo da área de transferência por meio de um comando colar link no menu Editar.</span><span class="sxs-lookup"><span data-stu-id="de79d-222">A client application supports the Link clipboard format by means of a Paste Link command on its Edit menu.</span></span> <span data-ttu-id="de79d-223">Quando o usuário escolhe esse comando, o aplicativo cliente analisa os nomes do aplicativo, do tópico e do item dos dados da área de transferência do formato de link.</span><span class="sxs-lookup"><span data-stu-id="de79d-223">When the user chooses this command, the client application parses the application, topic, and item names from the Link-format clipboard data.</span></span> <span data-ttu-id="de79d-224">Usando esses nomes, o aplicativo cliente inicia uma conversa para o aplicativo e o tópico, caso essa conversa ainda não exista.</span><span class="sxs-lookup"><span data-stu-id="de79d-224">Using these names, the client application initiates a conversation for the application and topic, if such a conversation does not already exist.</span></span> <span data-ttu-id="de79d-225">Em seguida, o aplicativo cliente envia uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) para o aplicativo de servidor, especificando o nome do item contido nos dados da área de transferência do formato de link.</span><span class="sxs-lookup"><span data-stu-id="de79d-225">The client application then sends a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server application, specifying the item name contained in the Link-format clipboard data.</span></span>

<span data-ttu-id="de79d-226">Veja a seguir um exemplo de resposta do aplicativo cliente quando o usuário escolhe o comando Colar vínculo.</span><span class="sxs-lookup"><span data-stu-id="de79d-226">Following is an example of a client application's response when the user chooses the Paste Link command.</span></span>


```
void DoPasteLink(hwndClientDDE) 
HWND hwndClientDDE; 
{ 
    HANDLE hData; 
    LPSTR lpData; 
    HWND hwndServerDDE; 
    CHAR szApplication[APP_MAX_SIZE + 1]; 
    CHAR szTopic[TOPIC_MAX_SIZE + 1]; 
    CHAR szItem[ITEM_MAX_SIZE + 1]; 
    size_t * nBufLen; 
 HRESULT hResult;
 
    if (OpenClipboard(hwndClientDDE)) 
    { 
        if (!(hData = GetClipboardData(cfLink)) || 
                !(lpData = GlobalLock(hData))) 
        { 
            CloseClipboard(); 
            return; 
        } 
 
        // Parse the clipboard data.
  hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
// TODO: Write error handler.
  return;
 }
 if (*nBufLen >= APP_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szApplication, APP_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
// TODO: Write error handler.
  return;
 }
        lpData += (*nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= TOPIC_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }
 hResult = StringCchCopy(szTopic, TOPIC_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 }
        lpData += (nBufLen + 1); // skips over null
 hResult = StringCchLength(lpData, STRSAFE_MAX_CCH, nBufLen);
 if (FAILED(hResult) || nBufLen == NULL)
 {
 // TODO: Write error handler.
  return;
 }
 if (*nBufLen >= ITEM_MAX_SIZE)
        { 
            CloseClipboard(); 
            GlobalUnlock(hData); 
            return; 
        }

 hResult = StringCchCopy(szItem, ITEM_MAX_SIZE +1, lpData);
 if (FAILED(hResult)
 {
 // TODO: Write error handler.
  return;
 } 
        GlobalUnlock(hData); 
        CloseClipboard(); 
 
        if (hwndServerDDE = 
                FindServerGivenAppTopic(szApplication, szTopic)) 
        { 
            // App/topic conversation is already started. 
 
            if (DoesAdviseAlreadyExist(hwndServerDDE, szItem)) 
            {
                MessageBox(hwndMain, 
                    "Advisory already established", 
                    "Client", MB_ICONEXCLAMATION | MB_OK); 
            }
            else SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
        } 
        else 
        { 
            // Client must initiate a new conversation first. 
            SendInitiate(szApplication, szTopic); 
            if (hwndServerDDE = 
                    FindServerGivenAppTopic(szApplication, 
                        szTopic)) 
            {
                SendAdvise(hwndClientDDE, hwndServerDDE, szItem); 
            }
        } 
    } 
    return; 
}
```



<span data-ttu-id="de79d-227">Neste exemplo, o aplicativo cliente abre a área de transferência e determina se ela contém dados no formato de link (ou seja, cfLink) que ele tinha registrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="de79d-227">In this example, the client application opens the clipboard and determines whether it contains data in the Link format (that is, cfLink) it had previously registered.</span></span> <span data-ttu-id="de79d-228">Caso contrário, ou se não puder bloquear os dados na área de transferência, o cliente retornará.</span><span class="sxs-lookup"><span data-stu-id="de79d-228">If not, or if it cannot lock the data in the clipboard, the client returns.</span></span>

<span data-ttu-id="de79d-229">Depois que o aplicativo cliente recupera um ponteiro para os dados da área de transferência, ele analisa os dados para extrair os nomes do aplicativo, do tópico e do item.</span><span class="sxs-lookup"><span data-stu-id="de79d-229">After the client application retrieves a pointer to the clipboard data, it parses the data to extract the application, topic, and item names.</span></span>

<span data-ttu-id="de79d-230">O aplicativo cliente determina se uma conversa no tópico já existe entre ela e o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-230">The client application determines whether a conversation on the topic already exists between it and the server application.</span></span> <span data-ttu-id="de79d-231">Se houver uma conversa, o cliente verificará se já existe um link para o item de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-231">If a conversation does exist, the client checks whether a link already exists for the data item.</span></span> <span data-ttu-id="de79d-232">Se esse link existir, o cliente exibirá uma caixa de mensagem para o usuário; caso contrário, ele chama sua própria função *SendAdvise* para enviar uma mensagem de [**aviso de \_ DDE \_ do WM**](wm-dde-advise.md) para o servidor para o item.</span><span class="sxs-lookup"><span data-stu-id="de79d-232">If such a link exists, the client displays a message box to the user; otherwise, it calls its own *SendAdvise* function to send a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message to the server for the item.</span></span>

<span data-ttu-id="de79d-233">Se uma conversa no tópico ainda não existir entre o cliente e o servidor, o cliente primeiro chama sua própria função *SendInitiate* para transmitir a mensagem de [**\_ \_ início do WM DDE**](wm-dde-initiate.md) para solicitar uma conversa e, segundo, chama sua própria função *FindServerGivenAppTopic* para estabelecer a conversa com a janela que responde em nome do aplicativo do servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-233">If a conversation on the topic does not already exist between the client and the server, the client first calls its own *SendInitiate* function to broadcast the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message to request a conversation and, second, calls its own *FindServerGivenAppTopic* function to establish the conversation with the window that responds on behalf of the server application.</span></span> <span data-ttu-id="de79d-234">Após o início da conversa, o aplicativo cliente chama *SendAdvise* para solicitar o link.</span><span class="sxs-lookup"><span data-stu-id="de79d-234">After the conversation has begun, the client application calls *SendAdvise* to request the link.</span></span>

### <a name="notifying-the-client-that-data-has-changed"></a><span data-ttu-id="de79d-235">Notificando o cliente que os dados foram alterados</span><span class="sxs-lookup"><span data-stu-id="de79d-235">Notifying the Client that Data Has Changed</span></span>

<span data-ttu-id="de79d-236">Quando o cliente estabelece um link usando a mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) , com o membro **fDeferUpd** não definido (ou seja, igual a zero) na estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) , o cliente solicitou que o servidor enviasse o item de dados sempre que o valor do item for alterado.</span><span class="sxs-lookup"><span data-stu-id="de79d-236">When the client establishes a link by using the [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, with the **fDeferUpd** member not set (that is, equal to zero) in the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure, the client has requested the server send the data item each time the item's value changes.</span></span> <span data-ttu-id="de79d-237">Nesses casos, o servidor renderiza o novo valor do item de dados no formato especificado anteriormente e envia ao cliente uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-237">In such cases, the server renders the new value of the data item in the previously specified format and sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message, as shown in the following example.</span></span>


```
// Allocate the size of a DDE data header, plus data (a string), 
// plus a <CR><LF><NULL> 

size_t* pcch;
HRESULT hResult;
 
hResult = StringCchLength(szItemValue,STRSAFE_MAX_CCH, pcch);
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
if (!(hData = GlobalAlloc(GMEM_MOVEABLE,
  sizeof(DDEDATA) + *pcch + 3))) 
{
    return; 
}
if (!(lpData = (DDEDATA FAR*) GlobalLock(hData))) 
{ 
    GlobalFree(hData); 
    return; 
} 
lpData->fAckReq = bAckRequest;       // as in original WM_DDE_ADVISE 
lpData->cfFormat = CF_TEXT;
hResult = StringCchCopy(lpData->Value, *pcch +1, szItemValue); // copies value to be sent
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
// add CR/LF for CF_TEXT format
hResult = StringCchCat(lpData->Value, *pcch + 3, "\r\n");
if (FAILED(hResult))
{
// TODO: Write error handler.
 return;
}
GlobalUnlock(hData); 
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndClientDDE, 
            WM_DDE_DATA, 
            (WPARAM) hwndServerDDE, 
            PackDDElParam(WM_DDE_DATA, (UINT) hData, atomItem))) 
    { 
        GlobalFree(hData); 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_DATA, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
 
}
```



<span data-ttu-id="de79d-238">Neste exemplo, o cliente processa o valor do item conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="de79d-238">In this example, the client processes the item value as appropriate.</span></span> <span data-ttu-id="de79d-239">Se o sinalizador **fAckReq** para o item for definido, o cliente envia ao servidor uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva.</span><span class="sxs-lookup"><span data-stu-id="de79d-239">If the **fAckReq** flag for the item is set, the client sends the server a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="de79d-240">Quando o cliente estabelece o link, com o conjunto de membros **fDeferUpd** (ou seja, igual a 1), o cliente solicitou que apenas uma notificação, não os dados em si, seja enviada sempre que os dados forem alterados.</span><span class="sxs-lookup"><span data-stu-id="de79d-240">When the client establishes the link, with the **fDeferUpd** member set (that is, equal to 1), the client has requested that only a notification, not the data itself, be sent each time the data changes.</span></span> <span data-ttu-id="de79d-241">Nesses casos, quando o valor do item é alterado, o servidor não processa o valor, mas simplesmente envia ao cliente uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) com um identificador de dados nulo, conforme ilustrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-241">In such cases, when the item value changes, the server does not render the value but simply sends the client a [**WM\_DDE\_DATA**](wm-dde-data.md) message with a null data handle, as illustrated in the following example.</span></span>


```
if (bDeferUpd)      // check whether flag was set in WM_DDE_ADVISE
{
    if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
    { 
        if (!PostMessage(hwndClientDDE, 
                WM_DDE_DATA, 
                (WPARAM) hwndServerDDE, 
                PackDDElParam(WM_DDE_DATA, 0, 
                    atomItem)))                  // NULL data
        {
            GlobalDeleteAtom(atomItem); 
            FreeDDElParam(WM_DDE_DATA, lParam); 
        } 
    } 
} 
 
if (atomItem == 0) 
{ 
     // Handle errors. 
} 
```



<span data-ttu-id="de79d-242">Conforme necessário, o cliente pode solicitar o valor mais recente do item de dados emitindo uma mensagem [**de \_ \_ solicitação DDE do WM**](wm-dde-request.md) normal ou pode simplesmente ignorar o aviso do servidor que os dados mudaram.</span><span class="sxs-lookup"><span data-stu-id="de79d-242">As necessary, the client can request the latest value of the data item by issuing a normal [**WM\_DDE\_REQUEST**](wm-dde-request.md) message, or it can simply ignore the notice from the server that the data has changed.</span></span> <span data-ttu-id="de79d-243">Em ambos os casos, se **fAckReq** for igual a 1, o cliente deverá enviar uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva para o servidor.</span><span class="sxs-lookup"><span data-stu-id="de79d-243">In either case, if **fAckReq** is equal to 1, the client is expected to send a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message to the server.</span></span>

### <a name="terminating-a-data-link"></a><span data-ttu-id="de79d-244">Encerrando um link de dados</span><span class="sxs-lookup"><span data-stu-id="de79d-244">Terminating a Data Link</span></span>

<span data-ttu-id="de79d-245">Se o cliente solicitar que um link de dados específico seja encerrado, o cliente enviará ao servidor uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-unadvise.md) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-245">If the client requests that a specific data link be terminated, the client sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message, as shown in the following example.</span></span>


```
if ((atomItem = GlobalAddAtom(szItemName)) != 0) 
{ 
    if (!PostMessage(hwndServerDDE, 
            WM_DDE_UNADVISE, 
            (WPARAM) hwndClientDDE, 
            PackDDElParam(WM_DDE_UNADVISE, 0, atomItem))) 
    { 
        GlobalDeleteAtom(atomItem); 
        FreeDDElParam(WM_DDE_UNADVISE, lParam); 
    } 
} 
 
if (atomItem == 0) 
{ 
    // Handle errors. 
}
```



<span data-ttu-id="de79d-246">O servidor verifica se o cliente atualmente tem um link para o item específico nesta conversa.</span><span class="sxs-lookup"><span data-stu-id="de79d-246">The server checks whether the client currently has a link to the specific item in this conversation.</span></span> <span data-ttu-id="de79d-247">Se houver um link, o servidor enviará ao cliente uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva; o servidor não será mais necessário para enviar atualizações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="de79d-247">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server is then no longer required to send updates about the item.</span></span> <span data-ttu-id="de79d-248">Se nenhum link existir, o servidor enviará ao cliente uma mensagem de **\_ \_ ACK DDE do WM** negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-248">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

<span data-ttu-id="de79d-249">A mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-unadvise.md) especifica um formato de dados.</span><span class="sxs-lookup"><span data-stu-id="de79d-249">The [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message specifies a data format.</span></span> <span data-ttu-id="de79d-250">Um formato de zero informa ao servidor para interromper todos os links para o item especificado, mesmo que vários links quentes sejam estabelecidos e cada um deles use um formato diferente.</span><span class="sxs-lookup"><span data-stu-id="de79d-250">A format of zero informs the server to stop all links for the specified item, even if several hot links are established and each uses a different format.</span></span>

<span data-ttu-id="de79d-251">Para encerrar todos os links de uma conversa, o aplicativo cliente envia ao servidor uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-unadvise.md) com um átomo de item nulo.</span><span class="sxs-lookup"><span data-stu-id="de79d-251">To terminate all links for a conversation, the client application sends the server a [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md) message with a null item atom.</span></span> <span data-ttu-id="de79d-252">O servidor determina se a conversa tem pelo menos um link estabelecido atualmente.</span><span class="sxs-lookup"><span data-stu-id="de79d-252">The server determines whether the conversation has at least one link currently established.</span></span> <span data-ttu-id="de79d-253">Se houver um link, o servidor enviará ao cliente uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva; o servidor não precisará mais enviar nenhuma atualização na conversa.</span><span class="sxs-lookup"><span data-stu-id="de79d-253">If a link exists, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; the server then no longer has to send any updates in the conversation.</span></span> <span data-ttu-id="de79d-254">Se nenhum link existir, o servidor enviará ao cliente uma mensagem de **\_ \_ ACK DDE do WM** negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-254">If no link exists, the server sends the client a negative **WM\_DDE\_ACK** message.</span></span>

## <a name="carrying-out-commands-in-a-server-application"></a><span data-ttu-id="de79d-255">Executando comandos em um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="de79d-255">Carrying Out Commands in a Server Application</span></span>

<span data-ttu-id="de79d-256">Os aplicativos podem usar a mensagem de [**\_ \_ execução do WM DDE**](wm-dde-execute.md) para fazer com que um determinado comando ou série de comandos sejam executados em outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de79d-256">Applications can use the [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message to cause a certain command or series of commands to be carried out in another application.</span></span> <span data-ttu-id="de79d-257">Para fazer isso, o cliente envia ao servidor uma mensagem de **\_ \_ execução DDE do WM** que contém um identificador para uma cadeia de caracteres de comando, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="de79d-257">To do this, the client sends the server a **WM\_DDE\_EXECUTE** message containing a handle to a command string, as shown in the following example.</span></span>


```
HRESULT hResult;
  
if (!(hCommand = GlobalAlloc(GMEM_MOVEABLE, 
        sizeof(szCommandString) + 1))) 
{
    return; 
}
if (!(lpCommand = GlobalLock(hCommand))) 
{ 
    GlobalFree(hCommand); 
    return; 
} 

hResult = StringCbCopy(lpCommand, sizeof(szCommandString), szCommandString);
if (hResult != S_OK)
{
// TODO: Write error handler.
 return;
}
 
GlobalUnlock(hCommand); 
if (!PostMessage(hwndServerDDE, 
        WM_DDE_EXECUTE, 
        (WPARAM) hwndClientDDE, 
        PackDDElParam(WM_DDE_EXECUTE, 0, (UINT) hCommand))) 
{ 
    GlobalFree(hCommand); 
    FreeDDElParam(WM_DDE_EXECUTE, lParam); 
}
```



<span data-ttu-id="de79d-258">Neste exemplo, o servidor tenta executar a cadeia de caracteres de comando especificada.</span><span class="sxs-lookup"><span data-stu-id="de79d-258">In this example, the server attempts to carry out the specified command string.</span></span> <span data-ttu-id="de79d-259">Se tiver sucesso, o servidor enviará ao cliente uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva; caso contrário, ele enviará uma mensagem de **\_ \_ ACK DDE do WM** negativa.</span><span class="sxs-lookup"><span data-stu-id="de79d-259">If it succeeds, the server sends the client a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message; otherwise, it sends a negative **WM\_DDE\_ACK** message.</span></span> <span data-ttu-id="de79d-260">Essa mensagem de **\_ \_ ACK de DDE do WM** reutiliza o identificador *hCommand* passado na mensagem de [**\_ \_ execução DDE do WM**](wm-dde-execute.md) original.</span><span class="sxs-lookup"><span data-stu-id="de79d-260">This **WM\_DDE\_ACK** message reuses the *hCommand* handle passed in the original [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message.</span></span>

<span data-ttu-id="de79d-261">Se a cadeia de caracteres de execução do comando do cliente solicitar que o servidor seja encerrado, o servidor deverá responder enviando uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) positiva e, em seguida, postar uma mensagem de [**encerramento de \_ DDE \_ do WM**](wm-dde-terminate.md) antes de encerrar.</span><span class="sxs-lookup"><span data-stu-id="de79d-261">If the client's command execution string requests that the server terminate, the server should respond by sending a positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message and then post a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message before terminating.</span></span> <span data-ttu-id="de79d-262">Todos os outros comandos enviados com uma mensagem de [**\_ \_ execução DDE do WM**](wm-dde-execute.md) devem ser executados de forma síncrona; ou seja, o servidor deve enviar uma mensagem de **\_ \_ ACK DDE do WM** somente após a conclusão bem-sucedida do comando.</span><span class="sxs-lookup"><span data-stu-id="de79d-262">All other commands sent with a [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message should be executed synchronously; that is, the server should send a **WM\_DDE\_ACK** message only after successfully completing the command.</span></span>

## <a name="terminating-a-conversation"></a><span data-ttu-id="de79d-263">Encerrando uma conversa</span><span class="sxs-lookup"><span data-stu-id="de79d-263">Terminating a Conversation</span></span>

<span data-ttu-id="de79d-264">O cliente ou o servidor pode emitir uma mensagem [**de \_ \_ encerramento de DDE do WM**](wm-dde-terminate.md) para encerrar uma conversa a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="de79d-264">Either the client or the server can issue a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to terminate a conversation at any time.</span></span> <span data-ttu-id="de79d-265">Da mesma forma, os aplicativos cliente e servidor devem estar preparados para receber essa mensagem a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="de79d-265">Similarly, both the client and server applications should be prepared to receive this message at any time.</span></span> <span data-ttu-id="de79d-266">Um aplicativo deve encerrar todas as suas conversas antes de desligar.</span><span class="sxs-lookup"><span data-stu-id="de79d-266">An application must terminate all of its conversations before shutting down.</span></span>

<span data-ttu-id="de79d-267">No exemplo a seguir, o aplicativo que está encerrando a conversa posta uma mensagem de [**\_ \_ encerramento do WM DDE**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="de79d-267">In the following example, the application terminating the conversation posts a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span>


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



<span data-ttu-id="de79d-268">Isso informa ao outro aplicativo que o aplicativo de envio não enviará mais mensagens e o destinatário pode fechar sua janela.</span><span class="sxs-lookup"><span data-stu-id="de79d-268">This informs the other application that the sending application will send no further messages and the recipient can close its window.</span></span> <span data-ttu-id="de79d-269">O destinatário é esperado em todos os casos para responder imediatamente enviando uma mensagem [**de \_ \_ encerramento de DDE do WM**](wm-dde-terminate.md) .</span><span class="sxs-lookup"><span data-stu-id="de79d-269">The recipient is expected in all cases to respond promptly by sending a [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message.</span></span> <span data-ttu-id="de79d-270">O destinatário não deve enviar uma mensagem de [**\_ \_ confirmação de DDE do WM**](wm-dde-ack.md) negativa, ocupada ou positiva.</span><span class="sxs-lookup"><span data-stu-id="de79d-270">The recipient must not send a negative, busy, or positive [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="de79d-271">Depois que um aplicativo enviou a mensagem de [**\_ \_ encerramento do WM DDE**](wm-dde-terminate.md) para o parceiro em uma conversa DDE, ele não deve responder às mensagens desse parceiro, pois o parceiro pode ter destruído a janela à qual a resposta seria enviada.</span><span class="sxs-lookup"><span data-stu-id="de79d-271">After an application has sent the [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) message to the partner in a DDE conversation, it must not respond to messages from that partner, since the partner might have destroyed the window to which the response would be sent.</span></span>

<span data-ttu-id="de79d-272">Se um aplicativo receber uma mensagem DDE diferente do [**WM \_ DDE \_ terminar**](wm-dde-terminate.md) após ter postado o **\_ \_ encerramento do WM DDE**, ele deverá liberar todos os objetos associados às mensagens recebidas, exceto os identificadores de dados para [**\_ \_ dados do WM DDE**](wm-dde-data.md) ou o [**WM \_ DDE \_**](wm-dde-poke.md) enviar mensagens que **não** têm o conjunto de membros **fRelease** .</span><span class="sxs-lookup"><span data-stu-id="de79d-272">If an application receives a DDE message other than [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) after it has posted **WM\_DDE\_TERMINATE**, it should free all objects associated with the received messages except the data handles for [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_POKE**](wm-dde-poke.md) messages that do **not** have the **fRelease** member set.</span></span>

<span data-ttu-id="de79d-273">Quando um aplicativo está prestes a terminar, ele deve encerrar todas as conversas DDE ativas antes de concluir o processamento da mensagem de [**\_ destruição do WM**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="de79d-273">When an application is about to terminate, it should end all active DDE conversations before completing processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="de79d-274">No entanto, se um aplicativo não encerrar suas conversas DDE ativas, o sistema encerrará todas as conversas DDE associadas a uma janela quando a janela for destruída.</span><span class="sxs-lookup"><span data-stu-id="de79d-274">However, if an application does not end its active DDE conversations, the system will terminate any DDE conversations associated with a window when the window is destroyed.</span></span> <span data-ttu-id="de79d-275">O exemplo a seguir mostra como um aplicativo de servidor encerra todas as conversas DDE.</span><span class="sxs-lookup"><span data-stu-id="de79d-275">The following example shows how a server application terminates all DDE conversations.</span></span>


```
void TerminateConversations(hwndServerDDE) 
HWND hwndServerDDE; 
{ 
    HWND hwndClientDDE; 
 
    // Terminate each active conversation. 
 
    while (hwndClientDDE = GetNextLink(hwndClientDDE)) 
    { 
        SendTerminate(hwndServerDDE, hwndClientDDE); 
    } 
    return; 
} 
 
BOOL AtLeastOneLinkActive(VOID) 
{ 
    return TRUE; 
} 
 
HWND GetNextLink(hwndDummy) 
    HWND hwndDummy; 
{ 
    return (HWND) 1; 
} 
 
VOID SendTerminate(HWND hwndServerDDE, HWND hwndClientDDE) 
{ 
    return; 
}
```



 

 