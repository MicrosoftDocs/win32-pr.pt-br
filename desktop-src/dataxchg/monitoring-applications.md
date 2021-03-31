---
title: Monitorando aplicativos
description: Este tópico discute como os elementos da biblioteca de gerenciamento de troca dinâmica de dados podem ser usados para criar um aplicativo que monitora a atividade de troca de dados dinâmicos no sistema.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), monitoramento de aplicativos
- DDE (troca dinâmica de dados), monitorando aplicativos
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), aplicativos de monitoramento
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), aplicativos de monitoramento
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005261"
---
# <a name="monitoring-applications"></a><span data-ttu-id="450e6-111">Monitorando aplicativos</span><span class="sxs-lookup"><span data-stu-id="450e6-111">Monitoring Applications</span></span>

<span data-ttu-id="450e6-112">Os elementos de API da biblioteca de gerenciamento de troca dinâmica de dados (DDEML) podem ser usados para criar um aplicativo que monitora a atividade de troca dinâmica de dados (DDE) no sistema.</span><span class="sxs-lookup"><span data-stu-id="450e6-112">The API elements of the Dynamic Data Exchange Management Library (DDEML) can be used to create an application that monitors Dynamic Data Exchange (DDE) activity in the system.</span></span> <span data-ttu-id="450e6-113">Como qualquer aplicativo de DDEML, um aplicativo de monitoramento de DDE contém uma função de retorno de chamada DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-113">Like any DDEML application, a DDE monitoring application contains a DDE callback function.</span></span> <span data-ttu-id="450e6-114">O DDEML notifica uma função de retorno de chamada DDE do aplicativo de monitoramento sempre que um evento DDE ocorrer, passando informações sobre o evento para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="450e6-114">The DDEML notifies a monitoring application's DDE callback function whenever a DDE event occurs, passing information about the event to the callback function.</span></span> <span data-ttu-id="450e6-115">O aplicativo normalmente exibe as informações em uma janela ou grava-as em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="450e6-115">The application typically displays the information in a window or writes it to a file.</span></span>

<span data-ttu-id="450e6-116">Para receber notificações do DDEML, um aplicativo deve ter sido registrado como um monitor DDE, especificando o \_ sinalizador do monitor APPCLASS em uma chamada para a função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="450e6-116">To receive notifications from the DDEML, an application must have registered as a DDE monitor by specifying the APPCLASS\_MONITOR flag in a call to the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span> <span data-ttu-id="450e6-117">Nesta mesma chamada, o aplicativo pode especificar um ou mais sinalizadores de monitor para indicar os tipos de eventos para os quais o DDEML é notificar a função de retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="450e6-117">In this same call, the application can specify one or more monitor flags to indicate the types of events for which the DDEML is to notify the application's callback function.</span></span> <span data-ttu-id="450e6-118">Os sinalizadores de monitor a seguir podem ser especificados por um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="450e6-118">The following monitor flags can be specified by an application:</span></span>



| <span data-ttu-id="450e6-119">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="450e6-119">Flag</span></span>          | <span data-ttu-id="450e6-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="450e6-120">Description</span></span>                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="450e6-121">\_retornos de chamada MF</span><span class="sxs-lookup"><span data-stu-id="450e6-121">MF\_CALLBACKS</span></span> | <span data-ttu-id="450e6-122">Notifica a função de retorno de chamada sempre que uma transação é enviada para qualquer função de retorno de chamada DDE no sistema.</span><span class="sxs-lookup"><span data-stu-id="450e6-122">Notifies the callback function whenever a transaction is sent to any DDE callback function in the system.</span></span>                                                                                                                                           |
| <span data-ttu-id="450e6-123">CONV de MF \_</span><span class="sxs-lookup"><span data-stu-id="450e6-123">MF\_CONV</span></span>      | <span data-ttu-id="450e6-124">Notifica a função de retorno de chamada sempre que uma conversa é estabelecida ou terminada.</span><span class="sxs-lookup"><span data-stu-id="450e6-124">Notifies the callback function whenever a conversation is established or terminated.</span></span>                                                                                                                                                                |
| <span data-ttu-id="450e6-125">erros de MF \_</span><span class="sxs-lookup"><span data-stu-id="450e6-125">MF\_ERRORS</span></span>    | <span data-ttu-id="450e6-126">Notifica a função de retorno de chamada sempre que ocorrer um erro DDEML.</span><span class="sxs-lookup"><span data-stu-id="450e6-126">Notifies the callback function whenever a DDEML error occurs.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="450e6-127">\_informações de HSZ MF \_</span><span class="sxs-lookup"><span data-stu-id="450e6-127">MF\_HSZ\_INFO</span></span> | <span data-ttu-id="450e6-128">Notifica a função de retorno de chamada sempre que um aplicativo DDEML cria, libera ou incrementa a contagem de uso de um identificador de cadeia de caracteres ou sempre que um identificador de cadeia de caracteres é liberado como resultado de uma chamada para a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="450e6-128">Notifies the callback function whenever a DDEML application creates, frees, or increments the usage count of a string handle or whenever a string handle is freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> |
| <span data-ttu-id="450e6-129">\_links MF</span><span class="sxs-lookup"><span data-stu-id="450e6-129">MF\_LINKS</span></span>     | <span data-ttu-id="450e6-130">Notifica a função de retorno de chamada sempre que um loop de aviso é iniciado ou encerrado.</span><span class="sxs-lookup"><span data-stu-id="450e6-130">Notifies the callback function whenever an advise loop is started or ended.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="450e6-131">MENSAGENS de MF \_</span><span class="sxs-lookup"><span data-stu-id="450e6-131">MF\_POSTMSGS</span></span>  | <span data-ttu-id="450e6-132">Notifica a função de retorno de chamada sempre que o sistema ou um aplicativo postar uma mensagem DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-132">Notifies the callback function whenever the system or an application posts a DDE message.</span></span>                                                                                                                                                           |
| <span data-ttu-id="450e6-133">\_SENDMSGS MF</span><span class="sxs-lookup"><span data-stu-id="450e6-133">MF\_SENDMSGS</span></span>  | <span data-ttu-id="450e6-134">Notifica a função de retorno de chamada sempre que o sistema ou um aplicativo envia uma mensagem DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-134">Notifies the callback function whenever the system or an application sends a DDE message.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="450e6-135">O exemplo a seguir mostra como registrar um aplicativo de monitoramento de DDE para que sua função de retorno de chamada DDE receba notificações de todos os eventos DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-135">The following example shows how to register a DDE monitoring application so that its DDE callback function receives notifications of all DDE events.</span></span>


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



<span data-ttu-id="450e6-136">O DDEML informa um aplicativo de monitoramento de um evento DDE enviando uma transação de [**\_ Monitor de XTYP**](xtyp-monitor.md) para a função de retorno de chamada DDE do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="450e6-136">The DDEML informs a monitoring application of a DDE event by sending an [**XTYP\_MONITOR**](xtyp-monitor.md) transaction to the application's DDE callback function.</span></span> <span data-ttu-id="450e6-137">Durante essa transação, o DDEML passa um sinalizador de monitor que especifica o tipo de evento DDE que ocorreu e um identificador para um objeto DDE que contém informações detalhadas sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="450e6-137">During this transaction, the DDEML passes a monitor flag that specifies the type of DDE event that has occurred and a handle to a DDE object that contains detailed information about the event.</span></span> <span data-ttu-id="450e6-138">O DDEML fornece um conjunto de estruturas que o aplicativo pode usar para extrair as informações do objeto DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-138">The DDEML provides a set of structures that the application can use to extract the information from the DDE object.</span></span> <span data-ttu-id="450e6-139">Há uma estrutura correspondente para cada tipo de evento DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-139">There is a corresponding structure for each type of DDE event.</span></span>



| <span data-ttu-id="450e6-140">Estrutura</span><span class="sxs-lookup"><span data-stu-id="450e6-140">Structure</span></span>                                  | <span data-ttu-id="450e6-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="450e6-141">Description</span></span>                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="450e6-142">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="450e6-142">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | <span data-ttu-id="450e6-143">Contém informações sobre uma transação.</span><span class="sxs-lookup"><span data-stu-id="450e6-143">Contains information about a transaction.</span></span>                         |
| [<span data-ttu-id="450e6-144">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="450e6-144">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | <span data-ttu-id="450e6-145">Contém informações sobre uma conversa.</span><span class="sxs-lookup"><span data-stu-id="450e6-145">Contains information about a conversation.</span></span>                        |
| [<span data-ttu-id="450e6-146">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="450e6-146">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | <span data-ttu-id="450e6-147">Contém informações sobre o erro DDE mais recente.</span><span class="sxs-lookup"><span data-stu-id="450e6-147">Contains information about the latest DDE error.</span></span>                  |
| [<span data-ttu-id="450e6-148">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="450e6-148">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | <span data-ttu-id="450e6-149">Contém informações sobre um loop de aviso.</span><span class="sxs-lookup"><span data-stu-id="450e6-149">Contains information about an advise loop.</span></span>                        |
| [<span data-ttu-id="450e6-150">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="450e6-150">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | <span data-ttu-id="450e6-151">Contém informações sobre um identificador de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="450e6-151">Contains information about a string handle.</span></span>                       |
| [<span data-ttu-id="450e6-152">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="450e6-152">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | <span data-ttu-id="450e6-153">Contém informações sobre uma mensagem DDE que foi enviada ou postada.</span><span class="sxs-lookup"><span data-stu-id="450e6-153">Contains information about a DDE message that was sent or posted.</span></span> |



 

<span data-ttu-id="450e6-154">O exemplo a seguir mostra a função de retorno de chamada DDE de um aplicativo de monitoramento DDE que formata informações sobre cada evento de identificador de cadeia de caracteres e, em seguida, exibe as informações em uma janela.</span><span class="sxs-lookup"><span data-stu-id="450e6-154">The following example shows the DDE callback function of a DDE monitoring application that formats information about each string handle event and then displays the information in a window.</span></span> <span data-ttu-id="450e6-155">A função usa a estrutura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) para extrair as informações do objeto DDE.</span><span class="sxs-lookup"><span data-stu-id="450e6-155">The function uses the [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure to extract the information from the DDE object.</span></span>


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



 

 




