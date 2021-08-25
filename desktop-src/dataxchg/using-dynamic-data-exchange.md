---
title: Usando Dados Dinâmicos Exchange
description: Este tópico fornece exemplos de código relacionados à troca de dados dinâmica.
ms.assetid: 6d94403b-64b4-4763-868a-3b94431dab79
keywords:
- Dados Dinâmicos Exchange (DDE), conversas
- DDE (Dados Dinâmicos Exchange), conversas
- troca de dados, Dados Dinâmicos Exchange (DDE)
- Dados Dinâmicos Exchange (DDE), exemplos
- DDE (Dados Dinâmicos Exchange), exemplos
- Dados Dinâmicos Exchange (DDE), comandos em aplicativos de servidor
- DDE (Dados Dinâmicos Exchange), comandos em aplicativos de servidor
- Dados Dinâmicos Exchange (DDE), links de dados
- DDE (Dados Dinâmicos Exchange), links de dados
- Dados Dinâmicos Exchange (DDE), itens
- DDE (Dados Dinâmicos Exchange), itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3a279e02b65d5540e5494512a44eefdfecdb18607cb12731cf7daa0d8569de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953657"
---
# <a name="using-dynamic-data-exchange"></a>Usando Dados Dinâmicos Exchange

Esta seção tem exemplos de código nas seguintes tarefas:

-   [Iniciando uma conversa](#initiating-a-conversation)
-   [Transferindo um único item](#transferring-a-single-item)
    -   [Recuperando um item do servidor](#retrieving-an-item-from-the-server)
    -   [Enviando um item para o servidor](#submitting-an-item-to-the-server)
-   [Estabelecendo um link de dados permanente](#establishing-a-permanent-data-link)
    -   [Iniciando um link de dados](#initiating-a-data-link)
    -   [Iniciando um link de dados com o comando Colar Link](#initiating-a-data-link-with-the-paste-link-command)
    -   [Notificando o cliente de que os dados foram alterados](#notifying-the-client-that-data-has-changed)
    -   [Encerrando um link de dados](#terminating-a-data-link)
-   [Realizando comandos em um aplicativo de servidor](#carrying-out-commands-in-a-server-application)
-   [Encerrando uma conversa](#terminating-a-conversation)

## <a name="initiating-a-conversation"></a>Iniciando uma conversa

Para iniciar uma conversa Dados Dinâmicos Exchange (DDE), o cliente envia uma mensagem [**WM \_ DDE \_ INITIATE.**](wm-dde-initiate.md) Normalmente, o cliente transmite essa mensagem chamando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage), com –1 como o primeiro parâmetro. Se o aplicativo já tiver o alça de janela para o aplicativo de servidor, ele poderá enviar a mensagem diretamente para essa janela. O cliente prepara os átomos para o nome do aplicativo e o nome do tópico chamando [**GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) O cliente pode solicitar conversas com qualquer aplicativo de servidor em potencial e para qualquer possível tópico fornecendo **átomos NULL** (curinga) para o aplicativo e o tópico.

O exemplo a seguir ilustra como o cliente inicia uma conversa, em que o aplicativo e o tópico são especificados.


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
> Se seu aplicativo usar **átomos NULL,** você não precisará usar as funções [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) e [**GlobalDeleteAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaldeleteatom) Neste exemplo, o aplicativo cliente cria dois átomos globais que contêm o nome do servidor e o nome do tópico, respectivamente.

 

O aplicativo cliente envia uma [**mensagem WM \_ DDE \_ INITIATE**](wm-dde-initiate.md) com esses dois átomos no *parâmetro lParam* da mensagem. Na chamada para a [**função SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) a alça de janela especial –1 direciona o sistema a enviar essa mensagem para todos os outros aplicativos ativos. **O SendMessage** não retorna ao aplicativo cliente até que todos os aplicativos que recebem a mensagem tenham, por sua vez, retornado o controle para o sistema. Isso significa que todas as mensagens WM [**\_ DDE \_ ACK**](wm-dde-ack.md) enviadas em resposta pelos aplicativos de servidor têm garantia de que foram processadas pelo cliente quando a **chamada SendMessage** tiver retornado.

Depois [**que SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retorna, o aplicativo cliente exclui os átomos globais.

Os aplicativos de servidor respondem de acordo com a lógica ilustrada no diagrama a seguir.

![lógica de resposta do aplicativo de servidor](images/csdde-01.png)

Para reconhecer um ou mais tópicos, o servidor deve criar átomos para cada conversa (exigindo átomos de nome de aplicativo duplicados se houver vários tópicos) e enviar uma mensagem [**WM \_ DDE \_ ACK**](wm-dde-ack.md) para cada conversa, conforme ilustrado no exemplo a seguir.


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



Quando um servidor responde com uma mensagem [**WM \_ DDE \_ ACK,**](wm-dde-ack.md) o aplicativo cliente deve salvar um handle na janela do servidor. O cliente que recebe o identificador como o parâmetro *wParam* da mensagem **WM \_ DDE \_ ACK** envia todas as mensagens DDE subsequentes para a janela do servidor que esse identificador identifica.

Se o aplicativo cliente usar um **atom NULL** para o nome do aplicativo ou o nome do tópico, espere que o aplicativo receba confirmações de mais de um aplicativo de servidor. Várias confirmações também podem vir de várias instâncias de um servidor DDE, mesmo que seu aplicativo cliente não **use** átomos null. Um servidor sempre deve usar uma janela exclusiva para cada conversa. O procedimento de janela no aplicativo cliente pode usar um handle para a janela do servidor (fornecido como o parâmetro *lParam* do [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)) para acompanhar várias conversas. Isso permite que uma única janela de cliente processe várias conversas sem a necessidade de encerrar e reconectar-se a uma nova janela de cliente para cada conversa.

## <a name="transferring-a-single-item"></a>Transferindo um único item

Depois que uma conversa de DDE for estabelecida, o cliente poderá recuperar o valor de um item de dados do servidor emito a mensagem DE SOLICITAÇÃO [**\_ de DDE \_**](wm-dde-request.md) wm ou enviar um valor de item de dados para o servidor emindo WM [**\_ DDE \_ WM.**](wm-dde-poke.md)

-   [Recuperando um item do servidor](#retrieving-an-item-from-the-server)
-   [Enviando um item para o servidor](#submitting-an-item-to-the-server)

### <a name="retrieving-an-item-from-the-server"></a>Recuperando um item do servidor

Para recuperar um item do servidor, o cliente envia ao servidor uma mensagem [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) especificando o item e o formato a recuperar, conforme mostrado no exemplo a seguir.


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



Neste exemplo, o cliente especifica o formato **CF \_ TEXT** da área de transferência como o formato preferencial para o item de dados solicitado.

O receptor (servidor) da mensagem [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) normalmente deve excluir o atom do item, mas se a chamada [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) falhar, o cliente deverá excluir o atom.

Se o servidor tiver acesso ao item solicitado e puder renderizar no formato solicitado, o servidor copia o valor do item como um objeto de memória compartilhada e envia ao cliente uma mensagem [**WM \_ DDE \_ DATA,**](wm-dde-data.md) conforme ilustrado no exemplo a seguir.


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



Neste exemplo, o aplicativo de servidor aloca um objeto de memória para conter o item de dados. O objeto de dados é inicializado como uma [**estrutura DDEDATA.**](/windows/desktop/api/Dde/ns-dde-ddedata)

Em seguida, o aplicativo de servidor define o **membro cfFormat** da estrutura como CF TEXT para informar ao aplicativo cliente que os \_ dados estão no formato de texto. O cliente responde copiando o valor dos dados solicitados para o membro **Value** da [**estrutura DDEDATA.**](/windows/desktop/api/Dde/ns-dde-ddedata) Depois que o servidor preencher o objeto de dados, o servidor desbloqueará os dados e criará um atom global que contém o nome do item de dados.

Por fim, o servidor emite [**a mensagem WM \_ DDE \_ DATA**](wm-dde-data.md) chamando [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). O identificador para o objeto de dados e o atom que contém o nome do item são empacotados no parâmetro *lParam* da mensagem pela [**função PackDDElParam.**](/windows/desktop/api/Dde/nf-dde-packddelparam)

Se [**o PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) falhar, o servidor deverá usar a [**função FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) para liberar o *parâmetro lParam* empacotado. O servidor também deve liberar o parâmetro *lParam* empacotado para a mensagem [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) recebida.

Se o servidor não puder atender à solicitação, ele enviará uma mensagem [**\_ \_ ACK negativa**](wm-dde-ack.md) do WM DDE para o cliente, conforme mostrado no exemplo a seguir.


```
// Negative acknowledgment. 
 
PostMessage(hwndClientDDE, 
    WM_DDE_ACK, 
    (WPARAM) hwndServerDDE, 
    PackDDElParam(WM_DDE_ACK, 0, atomItem));
```



Ao receber uma [**mensagem WM \_ DDE \_ DATA,**](wm-dde-data.md) o cliente processa o valor do item de dados conforme apropriado. Em seguida, se o membro **fAckReq** apontado na mensagem **WM \_ DDE \_ DATA** for 1, o cliente deverá enviar ao servidor uma mensagem ACK positiva do [**WM \_ DDE, \_**](wm-dde-ack.md) conforme mostrado no exemplo a seguir.


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



Neste exemplo, o cliente examina o formato dos dados. Se o formato não for **CF \_ TEXT** (ou se o cliente não puder bloquear a memória dos dados), o cliente enviará uma mensagem [**\_ \_ ACK**](wm-dde-ack.md) negativa do WM DDE para indicar que ele não pode processar os dados. Se o cliente não puder bloquear um handle de dados porque o handle contém o membro **fAckReq,** o cliente não deverá enviar uma mensagem **\_ \_ ACK** de WM DDE negativa. Em vez disso, o cliente deve encerrar a conversa.

Se um cliente enviar uma confirmação negativa em resposta a uma mensagem [**WM \_ DDE \_ DATA,**](wm-dde-data.md) o servidor será responsável por liberar a memória (mas não o parâmetro *lParam)* referenciada pela mensagem **WM \_ DDE \_ DATA** associada à confirmação negativa.

Se ele puder processar os dados, o cliente examinará o membro **fAckReq** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) para determinar se o servidor solicitou que ele fosse informado de que o cliente recebeu e processou os dados com êxito. Se o servidor solicitou essas informações, o cliente envia ao servidor uma mensagem [**\_ \_ ACK do WM DDE**](wm-dde-ack.md) positiva.

Como o desbloqueio de dados invalida o ponteiro para os dados, o cliente salva o valor do membro **fRelease** antes de desbloquear o objeto de dados. Depois de salvar o valor, o cliente o examina para determinar se o aplicativo de servidor solicitou ao cliente para liberar a memória que contém os dados; o cliente age de acordo.

Ao receber uma mensagem [**\_ \_ ACK negativa do WM DDE,**](wm-dde-ack.md) o cliente pode solicitar o mesmo valor de item novamente, especificando um formato de área de transferência diferente. Normalmente, um cliente primeiro solicitará o formato mais complexo ao qual ele pode dar suporte e, em seguida, se necessário, será necessário por meio de formatos progressivamente mais simples até encontrar um que o servidor possa fornecer.

Se o servidor for compatível com o item Formatos do tópico do sistema, o cliente poderá determinar uma vez quais formatos de área de transferência o servidor dá suporte, em vez de determiná-los sempre que o cliente solicitar um item.

### <a name="submitting-an-item-to-the-server"></a>Enviando um item para o servidor

O cliente pode enviar um valor de item para o servidor usando a mensagem [**WM \_ DDE \_ ADM.**](wm-dde-poke.md) O cliente renderiza o item a ser enviado e envia a mensagem **WM \_ DDE \_ TAMBÉM,** conforme ilustrado no exemplo a seguir.


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
> O envio de dados usando uma mensagem [**WM \_ DDE \_ MESSAGE é**](wm-dde-poke.md) essencialmente o mesmo que enviá-los usando DADOS [**\_ DDE \_ WM**](wm-dde-data.md), exceto que **WM \_ DDE WM É enviado \_ do** cliente para o servidor.

 

Se o servidor for capaz de aceitar o valor do item de dados no formato renderizado pelo cliente, o servidor processa o valor do item conforme apropriado e envia ao cliente uma mensagem [**positiva do WM \_ DDE \_ ACK.**](wm-dde-ack.md) Se não for possível processar o valor do item, por causa de seu formato ou por outros motivos, o servidor enviará ao cliente uma mensagem negativa do **WM \_ DDE \_ ACK.**


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



Neste exemplo, o servidor chama [**GlobalGetAtomName**](/windows/desktop/api/Winbase/nf-winbase-globalgetatomnamea) para recuperar o nome do item enviado pelo cliente. Em seguida, o servidor determina se ele dá suporte ao item e se o item é renderizado no formato correto (ou seja, CF \_ TEXT). Se o item não tiver suporte e não for renderizado no formato correto ou se o servidor não puder bloquear a memória dos dados, o servidor enviará uma confirmação negativa de volta para o aplicativo cliente. Observe que, nesse caso, o envio de uma confirmação negativa está correto porque as mensagens [**WM \_ DDE \_ HACK**](wm-dde-poke.md) sempre são presumidas como ter o **membro fAckReq** definido. O servidor deve ignorar o membro.

Se um servidor enviar uma confirmação negativa em resposta a uma mensagem [**WM \_ DDE WM DDE \_ WM, o**](wm-dde-poke.md) cliente será responsável por liberar a memória (mas não o parâmetro *lParam)* referenciada pela mensagem **WM \_ DDE DNS \_ associada** à confirmação negativa.

## <a name="establishing-a-permanent-data-link"></a>Estabelecendo um link de dados permanente

Um aplicativo cliente pode usar o DDE para estabelecer um link para um item em um aplicativo de servidor. Depois que esse link é estabelecido, o servidor envia atualizações periódicas do item vinculado para o cliente, normalmente, sempre que o valor do item muda. Portanto, um fluxo de dados permanente é estabelecido entre os dois aplicativos; esse fluxo de dados permanece em local até que seja explicitamente desconectado.

### <a name="initiating-a-data-link"></a>Iniciando um link de dados

O cliente inicia um link de dados postando uma mensagem [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) conforme mostrado no exemplo a seguir.


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



Neste exemplo, o aplicativo cliente define o **sinalizador fDeferUpd** da mensagem [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) como **FALSE.** Isso direciona o aplicativo de servidor para enviar os dados para o cliente sempre que os dados mudarem.

Se o servidor não puder fazer o serviço da solicitação [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) ele enviará ao cliente uma mensagem [**negativa do WM \_ DDE \_ ACK.**](wm-dde-ack.md) Mas se o servidor tiver acesso ao item e puder renderizar no formato solicitado, o servidor anotará o novo link (lembrando os sinalizadores especificados no parâmetro *hOptions)* e enviará ao cliente uma mensagem **\_ \_ ACK do WM DDE** positiva. A partir daí, até que o cliente emite uma mensagem [**\_ \_ UNADVISE do WM DDE**](wm-dde-unadvise.md) correspondente, o servidor envia os novos dados para o cliente sempre que o valor do item muda no servidor.

A [**mensagem WM \_ DDE \_ ADVISE**](wm-dde-advise.md) estabelece o formato dos dados a serem trocados durante o link. Se o cliente tentar estabelecer outro link com o mesmo item, mas estiver usando um formato de dados diferente, o servidor poderá optar por rejeitar o segundo formato de dados ou tentar dar suporte a ele. Se um link warm tiver sido estabelecido para qualquer item de dados, o servidor poderá dar suporte a apenas um formato de dados por vez. Isso porque a mensagem [**WM \_ DDE \_ DATA**](wm-dde-data.md) para um link warm tem um alça de dados **NULL,** que, caso contrário, contém as informações de formato. Portanto, um servidor deve rejeitar todos os links quentes para um item já vinculado e deve rejeitar todos os links para um item que tenha links quentes. Outra interpretação pode ser que o servidor altera o formato e o estado quente ou quente de um link quando um segundo link é solicitado para o mesmo item de dados.

Em geral, os aplicativos cliente não devem tentar estabelecer mais de um link por vez para um item de dados.

### <a name="initiating-a-data-link-with-the-paste-link-command"></a>Iniciando um link de dados com o comando Colar Link

Aplicativos que suportam links de dados quentes ou quentes normalmente suportam um formato de área de transferência registrado chamado Link. Quando associado aos comandos Copiar e Colar Link do aplicativo, esse formato de área de transferência permite que o usuário estabeleça conversas de DDE entre aplicativos simplesmente copiando um item de dados no aplicativo de servidor e o copiando no aplicativo cliente.

Um aplicativo de servidor dá suporte ao formato de área de transferência **Link** colocando na área de  transferência uma cadeia de caracteres contendo os nomes de aplicativo, tópico e item quando o usuário escolhe o comando Copiar no menu Editar. A seguir está o formato de Link padrão:

*application***\\ 0**_tópico_*_\\ 0_*_item_*_\\ 0 \\ 0_*

Um único caractere nulo separa os nomes e dois caracteres nulos terminam toda a cadeia de caracteres.

Os aplicativos cliente e servidor devem registrar o formato da área de transferência link, conforme mostrado:


```
cfLink = RegisterClipboardFormat("Link");
```



Um aplicativo cliente dá suporte ao formato de área de transferência Link por meio de um comando Colar Link em seu menu Editar. Quando o usuário escolhe esse comando, o aplicativo cliente analisará os nomes de aplicativo, tópico e item dos dados da área de transferência formato de link. Usando esses nomes, o aplicativo cliente iniciará uma conversa para o aplicativo e o tópico, se essa conversa ainda não existir. Em seguida, o aplicativo cliente envia uma mensagem [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) para o aplicativo de servidor, especificando o nome do item contido nos dados da área de transferência formato de link.

A seguir está um exemplo de resposta de um aplicativo cliente quando o usuário escolhe o comando Colar Link.


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



Neste exemplo, o aplicativo cliente abre a área de transferência e determina se ele contém dados no formato link (ou seja, cfLink) que ele registrou anteriormente. Caso não seja, ou se não puder bloquear os dados na área de transferência, o cliente retornará.

Depois que o aplicativo cliente recuperar um ponteiro para os dados da área de transferência, ele analisará os dados para extrair os nomes de aplicativo, tópico e item.

O aplicativo cliente determina se uma conversa sobre o tópico já existe entre ele e o aplicativo de servidor. Se uma conversa existir, o cliente verificará se já existe um link para o item de dados. Se esse link existir, o cliente exibirá uma caixa de mensagem para o usuário; caso contrário, ele chama sua *própria função SendAdvise* para enviar uma mensagem [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) ao servidor para o item.

Se uma conversa sobre o tópico ainda não existir entre o cliente e o servidor, o cliente primeiro chamará sua própria função *SendInitiate* para transmitir a mensagem [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md) para solicitar uma conversa e, em segundo lugar, chamará sua própria função *FindServerGivenAppTopic* para estabelecer a conversa com a janela que responde em nome do aplicativo do servidor. Após o início da conversa, o aplicativo cliente *chama SendAdvise* para solicitar o link.

### <a name="notifying-the-client-that-data-has-changed"></a>Notificando o cliente de que os dados foram alterados

Quando o cliente estabelece um link usando a mensagem [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) com o membro **fDeferUpd** não definido (ou seja, igual a zero) na estrutura [**DDEDATA,**](/windows/desktop/api/Dde/ns-dde-ddedata) o cliente solicitou que o servidor enviasse o item de dados sempre que o valor do item for atualizado. Nesses casos, o servidor renderiza o novo valor do item de dados no formato especificado anteriormente e envia ao cliente uma mensagem [**WM \_ DDE \_ DATA,**](wm-dde-data.md) conforme mostrado no exemplo a seguir.


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



Neste exemplo, o cliente processa o valor do item conforme apropriado. Se o **sinalizador fAckReq** para o item estiver definido, o cliente enviará ao servidor uma mensagem [**\_ \_ ACK do WM DDE**](wm-dde-ack.md) positiva.

Quando o cliente estabelece o link, com o conjunto de membros **fDeferUpd** (ou seja, igual a 1), o cliente solicitou que apenas uma notificação, não os dados propriamente ditos, fosse enviada sempre que os dados mudarem. Nesses casos, quando o valor do item muda, o servidor não renderiza o valor, mas simplesmente envia ao cliente uma mensagem [**WM \_ DDE \_ DATA**](wm-dde-data.md) com um alça de dados nulo, conforme ilustrado no exemplo a seguir.


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



Conforme necessário, o cliente pode solicitar o valor mais recente do item de dados em emissão de uma mensagem de SOLICITAção [**\_ de DDE \_ wm**](wm-dde-request.md) normal ou simplesmente ignorar o aviso do servidor de que os dados foram alterados. Em ambos os casos, se **fAckReq** for igual a 1, espera-se que o cliente envie uma mensagem [**\_ \_ ACK do WM DDE**](wm-dde-ack.md) positiva para o servidor.

### <a name="terminating-a-data-link"></a>Encerrando um link de dados

Se o cliente solicitar que um link de dados específico seja encerrado, o cliente enviará ao servidor uma mensagem [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) conforme mostrado no exemplo a seguir.


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



O servidor verifica se o cliente atualmente tem um link para o item específico nesta conversa. Se houver um link, o servidor enviará ao cliente uma mensagem [**positiva do WM \_ DDE \_ ACK;**](wm-dde-ack.md) o servidor não será mais necessário para enviar atualizações sobre o item. Se não houver nenhum link, o servidor enviará ao cliente uma mensagem **\_ \_ ACK negativa do WM DDE.**

A [**mensagem WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) especifica um formato de dados. Um formato de zero informa ao servidor para interromper todos os links para o item especificado, mesmo que vários links a quente sejam estabelecidos e cada um use um formato diferente.

Para encerrar todos os links de uma conversa, o aplicativo cliente envia ao servidor uma mensagem [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md) com um atom de item nulo. O servidor determina se a conversa tem pelo menos um link estabelecido no momento. Se houver um link, o servidor enviará ao cliente uma mensagem [**positiva do WM \_ DDE \_ ACK;**](wm-dde-ack.md) o servidor não precisa mais enviar nenhuma atualização na conversa. Se não houver nenhum link, o servidor enviará ao cliente uma mensagem **\_ \_ ACK negativa do WM DDE.**

## <a name="carrying-out-commands-in-a-server-application"></a>Realizando comandos em um aplicativo de servidor

Os aplicativos podem usar a [**mensagem \_ WM DDE \_ EXECUTE**](wm-dde-execute.md) para fazer com que um determinado comando ou série de comandos seja executado em outro aplicativo. Para fazer isso, o cliente envia ao servidor uma mensagem **WM \_ DDE \_ EXECUTE** que contém um handle para uma cadeia de caracteres de comando, conforme mostrado no exemplo a seguir.


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



Neste exemplo, o servidor tenta executar a cadeia de caracteres de comando especificada. Se ele for bem-sucedido, o servidor enviará ao cliente uma mensagem [**\_ \_ ACK de WM DDE**](wm-dde-ack.md) positiva; caso contrário, ele enviará uma mensagem ACK negativa do **WM \_ DDE. \_** Essa **mensagem \_ WM DDE \_ ACK** reutiliza o handle *hCommand* passado na mensagem [**EXECUTE do WM \_ DDE \_**](wm-dde-execute.md) original.

Se a cadeia de caracteres de execução de comando do cliente solicitar que o servidor seja encerrado, o servidor deverá responder enviando uma mensagem [**\_ \_ ACK do WM DDE**](wm-dde-ack.md) positiva e, em seguida, postar uma mensagem [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) antes de encerrar. Todos os outros comandos enviados com uma mensagem [**EXECUTE do WM \_ DDE \_**](wm-dde-execute.md) devem ser executados de forma síncrona; ou seja, o servidor deve enviar uma mensagem WM **\_ DDE \_ ACK** somente depois de concluir o comando com êxito.

## <a name="terminating-a-conversation"></a>Encerrando uma conversa

O cliente ou o servidor pode emitir uma mensagem [**TERMINATE do WM \_ DDE \_**](wm-dde-terminate.md) para encerrar uma conversa a qualquer momento. Da mesma forma, os aplicativos cliente e servidor devem estar preparados para receber essa mensagem a qualquer momento. Um aplicativo deve encerrar todas as suas conversas antes de desligar.

No exemplo a seguir, o aplicativo que encerra a conversa posta uma mensagem [**WM \_ DDE \_ TERMINATE.**](wm-dde-terminate.md)


```
PostMessage(hwndServerDDE, WM_DDE_TERMINATE, 
    (WPARAM) hwndClientDDE, 0);
```



Isso informa ao outro aplicativo que o aplicativo de envio não enviará mais mensagens e o destinatário poderá fechar sua janela. O destinatário é esperado em todos os casos para responder imediatamente enviando uma mensagem [**WM \_ DDE \_ TERMINATE.**](wm-dde-terminate.md) O destinatário não deve enviar uma mensagem ACK negativa, ocupada ou [**positiva do WM \_ DDE. \_**](wm-dde-ack.md)

Depois que um aplicativo envia a mensagem [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) para o parceiro em uma conversa DDE, ele não deve responder às mensagens desse parceiro, pois o parceiro pode ter destruído a janela para a qual a resposta seria enviada.

Se um aplicativo receber  uma mensagem DDE diferente de WM DDE TERMINATE depois de ter postado WM [**\_ \_ DDE**](wm-dde-terminate.md) **\_ \_ TERMINATE**, ele deverá liberar todos os objetos associados às mensagens recebidas, exceto os alças de dados para mensagens [**WM \_ DDE \_ DATA**](wm-dde-data.md) ou [**WM \_ DDE WM QUE \_ não**](wm-dde-poke.md) têm o **membro fRelease** definido.

Quando um aplicativo está prestes a ser encerrado, ele deve encerrar todas as conversas de DDE ativas antes de concluir o processamento da [**mensagem WM \_ DESTROY.**](/windows/desktop/winmsg/wm-destroy) No entanto, se um aplicativo não encerrar suas conversas de DDE ativas, o sistema encerrará todas as conversas DDE associadas a uma janela quando a janela for destruída. O exemplo a seguir mostra como um aplicativo de servidor encerra todas as conversas DDE.


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



 

 