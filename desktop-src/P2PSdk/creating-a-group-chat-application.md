---
description: Este tópico fornece exemplos de código relevantes para as principais etapas do desenvolvimento de um aplicativo de chat com a API de agrupamento de pares, fornecendo um contexto para cada chamada à API.
ms.assetid: 47bb8606-0b7b-4e71-9d6f-c400d6a82e43
title: Criando um aplicativo de chat de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676d4e9913934024df3131c0f965a5d85477d148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296757"
---
# <a name="creating-a-group-chat-application"></a><span data-ttu-id="ed497-103">Criando um aplicativo de chat de grupo</span><span class="sxs-lookup"><span data-stu-id="ed497-103">Creating a Group Chat Application</span></span>

<span data-ttu-id="ed497-104">Este tópico fornece exemplos de código relevantes para as principais etapas do desenvolvimento de um aplicativo de chat com a API de agrupamento de pares, fornecendo um contexto para cada chamada à API.</span><span class="sxs-lookup"><span data-stu-id="ed497-104">This topic provides relevant code samples for the major steps of developing a chat application with the Peer Grouping API, providing a context for each API call.</span></span> <span data-ttu-id="ed497-105">Os comportamentos da interface do usuário e a estrutura geral do aplicativo não estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="ed497-105">UI behaviors and overall application structure are not included.</span></span>

> [!Note]  
> <span data-ttu-id="ed497-106">O aplicativo de exemplo de chat do grupo de pares completo é fornecido no SDK do par.</span><span class="sxs-lookup"><span data-stu-id="ed497-106">The complete Peer Group Chat sample application is provided in the Peer SDK.</span></span> <span data-ttu-id="ed497-107">Este tópico faz referência às funções fornecidas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="ed497-107">This topic references functions provided within the sample.</span></span>

 

## <a name="initializing-a-group"></a><span data-ttu-id="ed497-108">Inicializando um grupo</span><span class="sxs-lookup"><span data-stu-id="ed497-108">Initializing a Group</span></span>

<span data-ttu-id="ed497-109">A primeira etapa ao construir um aplicativo de chat é inicializar a infraestrutura de agrupamento de pares chamando [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) com a versão mais alta com suporte.</span><span class="sxs-lookup"><span data-stu-id="ed497-109">The first step when constructing a chat application is to initialize the Peer Grouping Infrastructure by calling [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) with the highest supported version.</span></span> <span data-ttu-id="ed497-110">Nesse caso, a **\_ \_ versão do grupo de pares** será definida no arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed497-110">In this case, **PEER\_GROUP\_VERSION** will be defined in the application header file.</span></span> <span data-ttu-id="ed497-111">A versão realmente suportada pela infraestrutura é retornada em **peerVersion**.</span><span class="sxs-lookup"><span data-stu-id="ed497-111">The version actually supported by the infrastructure is returned in **peerVersion**.</span></span>


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a><span data-ttu-id="ed497-112">Criando um grupo</span><span class="sxs-lookup"><span data-stu-id="ed497-112">Creating a Group</span></span>

<span data-ttu-id="ed497-113">Um aplicativo de chat deve ser capaz de criar um grupo de pares se nenhum grupo estiver disponível para junção ou se o usuário do aplicativo quiser criar um novo.</span><span class="sxs-lookup"><span data-stu-id="ed497-113">A chat application must be able to create a peer group if no group is available to join, or if the application user wants to create a new one.</span></span> <span data-ttu-id="ed497-114">Para fazer isso, você deve criar uma estrutura de [**\_ \_ Propriedades de grupo par**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) e preenchê-la com as configurações iniciais para o grupo, incluindo o classificador para o grupo par, o nome amigável, o nome de par do criador e o tempo de vida da presença.</span><span class="sxs-lookup"><span data-stu-id="ed497-114">To do this, you must create a [**PEER\_GROUP\_PROPERTIES**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) structure and populate it with the initial settings for the group, including the classifier for the peer group, the friendly name, the creator's peer name, and the presence lifetime.</span></span> <span data-ttu-id="ed497-115">Depois que essa estrutura tiver sido populada, passe-a para [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span><span class="sxs-lookup"><span data-stu-id="ed497-115">Once this structure has been populated, you pass it to [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: CreateGroup
//
// Purpose:  Creates a new group with the friendly name.
//
// Returns:  HRESULT
//
HRESULT CreateGroup(PCWSTR pwzName, PCWSTR pwzIdentity)
{
    HRESULT hr = S_OK;
    PEER_GROUP_PROPERTIES props = {0};

    if (SUCCEEDED(hr))
    {
        if ((NULL == pwzName) || (0 == *pwzName))
        {
            hr = E_INVALIDARG;
            DisplayHrError(L"Please enter a group name.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        CleanupGroup( );

        props.dwSize = sizeof(props);
        props.pwzClassifier = L"SampleChatGroup";
        props.pwzFriendlyName = (PWSTR) pwzName;
        props.pwzCreatorPeerName = (PWSTR) pwzIdentity;

        hr = PeerGroupCreate(&props, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create a new group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="issuing-invitations"></a><span data-ttu-id="ed497-116">Emitindo convites</span><span class="sxs-lookup"><span data-stu-id="ed497-116">Issuing Invitations</span></span>

<span data-ttu-id="ed497-117">Ao emitir um convite, o GMCs dos convidados deve ser obtido.</span><span class="sxs-lookup"><span data-stu-id="ed497-117">When issuing an invitation, the GMCs of the invitees must be obtained.</span></span> <span data-ttu-id="ed497-118">Eles podem ser obtidos chamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) no convite com seu nome de identidade.</span><span class="sxs-lookup"><span data-stu-id="ed497-118">These can obtained by calling [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) on the invitee with their identity name.</span></span> <span data-ttu-id="ed497-119">Se for bem-sucedido, as informações de identidade (o XML que contém o certificado codificado em base 64 com a chave pública RSA) serão gravadas em um local externo (um arquivo, neste exemplo) em que o emissor pode obtê-lo e usá-lo para criar um convite.</span><span class="sxs-lookup"><span data-stu-id="ed497-119">If successful, the identity information (the XML that contains the base-64 encoded certificate with the RSA public key) is written to an external location (a file, in this sample) where the inviter can obtain it and use it to create an invitation.</span></span>

<span data-ttu-id="ed497-120">Neste ponto, deve-se estabelecer um mecanismo para a entrega do convite ao convidado.</span><span class="sxs-lookup"><span data-stu-id="ed497-120">At this point, a mechanism for the delivery of the invitation to the invitee must be established.</span></span> <span data-ttu-id="ed497-121">Esse pode ser um email ou outro método seguro de troca de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ed497-121">This can be email or another secure method of file exchange.</span></span> <span data-ttu-id="ed497-122">No exemplo a seguir, o convite é gravado em um arquivo que pode ser transferido para o computador do convidado.</span><span class="sxs-lookup"><span data-stu-id="ed497-122">In the sample below, the invitation is written to a file which can then be transferred to the invitee's computer.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: SaveIdentityInfo
//
// Purpose:  Saves the information for an identity to a file.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT SaveIdentityInfo(PCWSTR pwzIdentity, PCWSTR pwzFile)
{
    PWSTR pwzXML = NULL;
    HRESULT hr = PeerIdentityGetXML(pwzIdentity, &pwzXML);

    if (FAILED(hr))
    {
        DisplayHrError(L"Unable to retrieve the XML data for the identity.", hr);
    }
    else
    {
        FILE *fp = NULL;
        errno_t err = 0;

        err = _wfopen_s(&fp, pwzFile, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path", hr);
        }
        else
        {
            if (fputws(pwzXML, fp) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(fp);
        }

        PeerFreeData(pwzXML);
    }

    return hr;
}
```



<span data-ttu-id="ed497-123">Convites, como identidades, também são emitidos externamente.</span><span class="sxs-lookup"><span data-stu-id="ed497-123">Invitations, like identities, are also issued externally.</span></span> <span data-ttu-id="ed497-124">Neste exemplo, o convite é gravado em um arquivo com **fputws** , onde o convidado pode obtê-lo e usá-lo quando chama [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="ed497-124">In this example, the invitation is written to a file with **fputws** where the invitee can obtain it and use it when it calls [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: CreateInvitation
//
// Purpose:  Creates an invitation file for an identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT CreateInvitation(PCWSTR wzIdentityInfoPath, PCWSTR wzInvitationPath)
{
    HRESULT hr = S_OK;
    WCHAR wzIdentityInfo[MAX_INVITATION] = {0};
    PWSTR pwzInvitation = NULL;
    errno_t  err  = 0;
    FILE *file = NULL;
        
    err = _wfopen_s(&file, wzIdentityInfoPath, L"rb");
    if (err != 0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Please choose a valid path to the identity information file.", hr);
    }
    else
    {
        fread(wzIdentityInfo, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);
    }

    if (SUCCEEDED(hr))
    {
        ULONGLONG ulExpire; // adjust time using this structure
        GetSystemTimeAsFileTime((FILETIME *)&ulExpire);

        // 15days in 100 nanoseconds resolution
        ulExpire += ((ULONGLONG) (60 * 60 * 24 * 15)) * ((ULONGLONG)1000*1000*10);

        hr = PeerGroupCreateInvitation(g_hGroup, wzIdentityInfo, (FILETIME*)&ulExpire, 1, (PEER_ROLE_ID*) &PEER_GROUP_ROLE_MEMBER, &pwzInvitation);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to create the invitation.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        err = _wfopen_s(&file, wzInvitationPath, L"wb");
        if (err != 0)
        {
            hr = E_FAIL;
            DisplayHrError(L"Please choose a valid path to the invitation file.", hr);
        }
        else
        {
            if (fputws(pwzInvitation, file) == WEOF)
            {
                hr = E_FAIL;
                DisplayHrError(L"End of file error.", hr);
            }
            fclose(file);
        }
    }

    PeerFreeData(pwzInvitation);
    return hr;
}
```



## <a name="joining-a-peer-group"></a><span data-ttu-id="ed497-125">Ingressando em um grupo de pares</span><span class="sxs-lookup"><span data-stu-id="ed497-125">Joining a Peer Group</span></span>

<span data-ttu-id="ed497-126">Se o par estiver tentando ingressar em um grupo de pares criado por outro par, ele precisará de um convite desse ponto.</span><span class="sxs-lookup"><span data-stu-id="ed497-126">If the peer is attempting to join a peer group created by another peer, it will need an invitation from that peer.</span></span> <span data-ttu-id="ed497-127">Os convites são entregues por um processo ou aplicativo externo para o convidado e salvos em um arquivo local, especificado no exemplo abaixo como *pwzFileName*.</span><span class="sxs-lookup"><span data-stu-id="ed497-127">Invitations are delivered by an external process or application to the invitee and saved to a local file, specified in the sample below as *pwzFileName*.</span></span> <span data-ttu-id="ed497-128">O blob XML do convite é lido do arquivo para **wzInvitation** e passado para [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="ed497-128">The invitation XML blob is read from the file into **wzInvitation** and passed to [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: JoinGroup
//
// Purpose:  Uses the invitation to join a group with a specific identity.
//           Displays a message if there was an error.
//
// Returns:  HRESULT
//
HRESULT JoinGroup(PCWSTR pwzIdentity, PCWSTR pwzFileName)
{
    HRESULT hr = S_OK;
    WCHAR wzInvitation[MAX_INVITATION] = {0};
    FILE        *file = NULL;
    errno_t     err;

    err = _wfopen_s(&file, pwzFileName, L"rb");
    if (err !=  0)
    {
        hr = E_FAIL;
        DisplayHrError(L"Error opening group invitation file", hr);
        return hr;
    }
    else
    {
        fread(wzInvitation, sizeof(WCHAR), MAX_INVITATION, file);
        if (ferror(file))
        {
            hr = E_FAIL;
            DisplayHrError(L"File read error occurred.", hr);
        }
        fclose(file);

        hr = PeerGroupJoin(pwzIdentity, wzInvitation, NULL, &g_hGroup);
        if (FAILED(hr))
        {
            DisplayHrError(L"Failed to join group.", hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = PrepareToChat( );
    }

    return hr;
}
```



## <a name="register-for-peer-events"></a><span data-ttu-id="ed497-129">Registrar-se para eventos de pares</span><span class="sxs-lookup"><span data-stu-id="ed497-129">Register for Peer Events</span></span>

<span data-ttu-id="ed497-130">Antes de se conectar, você deve se registrar para cada evento de mesmo nível pertinente ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed497-130">Before connecting, you should register for every peer event pertinent to the application.</span></span> <span data-ttu-id="ed497-131">No exemplo abaixo, você se registra para os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="ed497-131">In the example below, you register for the following events:</span></span>

-   <span data-ttu-id="ed497-132">registro de evento de grupo de pares \_ \_ \_ \_ alterado.</span><span class="sxs-lookup"><span data-stu-id="ed497-132">PEER\_GROUP\_EVENT\_RECORD\_CHANGED.</span></span> <span data-ttu-id="ed497-133">Como os registros serão usados para conter mensagens de bate-papo públicas, o aplicativo deve ser notificado toda vez que um novo for adicionado.</span><span class="sxs-lookup"><span data-stu-id="ed497-133">Since records will be used to contain public chat messages, the application must be notified every time a new one is added.</span></span> <span data-ttu-id="ed497-134">Quando esse evento de par é recebido, os dados de evento expõem o registro com a mensagem de chat.</span><span class="sxs-lookup"><span data-stu-id="ed497-134">When this peer event is received, the event data exposes the record with the chat message.</span></span> <span data-ttu-id="ed497-135">Os aplicativos devem ser registrados apenas para os tipos de registro que pretendem manipular diretamente.</span><span class="sxs-lookup"><span data-stu-id="ed497-135">Applications should only register for those record types they intend to handle directly.</span></span>
-   <span data-ttu-id="ed497-136">membro de evento de grupo de pares \_ \_ \_ \_ alterado.</span><span class="sxs-lookup"><span data-stu-id="ed497-136">PEER\_GROUP\_EVENT\_MEMBER\_CHANGED.</span></span> <span data-ttu-id="ed497-137">O aplicativo deve ser notificado quando os membros ingressarem ou saírem do grupo par, de modo que a lista de participantes possa ser atualizada de acordo.</span><span class="sxs-lookup"><span data-stu-id="ed497-137">The application must be notified when members join or leave the peer group so the list of participants can be updated accordingly.</span></span>
-   <span data-ttu-id="ed497-138">STATUS do evento do grupo de pares \_ \_ \_ \_ alterado.</span><span class="sxs-lookup"><span data-stu-id="ed497-138">PEER\_GROUP\_EVENT\_STATUS\_CHANGED.</span></span> <span data-ttu-id="ed497-139">As alterações no status do grupo de pares devem ser transmitidas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed497-139">Changes to the peer group status must be conveyed to the application.</span></span> <span data-ttu-id="ed497-140">Um membro do grupo de pares só é considerado disponível dentro do grupo de pares quando seu status indica que ele está conectado ao grupo, sincronizado com o banco de dados de registro do grupo de pares e ouvindo ativamente as atualizações registradas.</span><span class="sxs-lookup"><span data-stu-id="ed497-140">A peer group member is only considered to be available within the peer group when its status indicates that it is connected to the group, synchronized with the peer group record database, and actively listening to record updates.</span></span>
-   <span data-ttu-id="ed497-141">\_conexão direta de evento de grupo de pares \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ed497-141">PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION.</span></span> <span data-ttu-id="ed497-142">Mensagens privadas entre dois membros e trocas de dados devem ser realizadas em uma conexão direta, portanto, o aplicativo deve ser capaz de lidar com solicitações de conexão direta.</span><span class="sxs-lookup"><span data-stu-id="ed497-142">Private messages between two members and exchanges of data must be conducted over a direct connection, so the application must be able to handle direct connection requests.</span></span>
-   <span data-ttu-id="ed497-143">dados de entrada do evento do grupo de pares \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ed497-143">PEER\_GROUP\_EVENT\_INCOMING\_DATA.</span></span> <span data-ttu-id="ed497-144">Depois que uma conexão direta é iniciada, esse evento de mesmo nível alerta o aplicativo de que uma mensagem particular foi recebida.</span><span class="sxs-lookup"><span data-stu-id="ed497-144">After a direct connection is initiated, this peer event alerts the application that a private message has been received.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it will be called for only
//           those events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents(void)
{
    HRESULT hr = S_OK;
    PEER_GROUP_EVENT_REGISTRATION regs[] = {
        { PEER_GROUP_EVENT_RECORD_CHANGED, &RECORD_TYPE_CHAT_MESSAGE },
        { PEER_GROUP_EVENT_MEMBER_CHANGED, 0 },
        { PEER_GROUP_EVENT_STATUS_CHANGED, 0 },
        { PEER_GROUP_EVENT_DIRECT_CONNECTION, &DATA_TYPE_WHISPER_MESSAGE },
        { PEER_GROUP_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    else
    {
        hr = PeerGroupRegisterEvent(g_hGroup, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = E_UNEXPECTED;
        }
    }

    return hr;
}
```



## <a name="connecting-to-a-peer-group"></a><span data-ttu-id="ed497-145">Conectando a um grupo de pares</span><span class="sxs-lookup"><span data-stu-id="ed497-145">Connecting to a Peer Group</span></span>

<span data-ttu-id="ed497-146">Tendo criado ou Unido o grupo e registrado para os eventos apropriados, é hora de ficar online e iniciar uma sessão de bate-papo ativa.</span><span class="sxs-lookup"><span data-stu-id="ed497-146">Having either created or joined the group and registered for the appropriate events, it's time to go online and begin an active chat session.</span></span> <span data-ttu-id="ed497-147">Para fazer isso, você chama [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) e passa o identificador de grupo obtido de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) ou [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span><span class="sxs-lookup"><span data-stu-id="ed497-147">To do this, you call [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) and pass in the group handle obtained from [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) or [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).</span></span> <span data-ttu-id="ed497-148">Depois de chamar isso, as mensagens de chat serão recebidas como eventos de alteração de registro de evento de grupo de pares \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ed497-148">After calling this, chat messages will be received as PEER\_GROUP\_EVENT\_RECORD\_CHANGED events.</span></span>

## <a name="obtaining-a-list-of-peer-group-members"></a><span data-ttu-id="ed497-149">Obtendo uma lista de membros do grupo de pares</span><span class="sxs-lookup"><span data-stu-id="ed497-149">Obtaining a List of Peer Group Members</span></span>

<span data-ttu-id="ed497-150">A obtenção de uma lista de membros conectados ao grupo par é simples: chame [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) para recuperar a lista de membros do grupo e chame iterativamente [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) até que todos os membros sejam recuperados.</span><span class="sxs-lookup"><span data-stu-id="ed497-150">Obtaining a list of members connected to the peer group is simple: call [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) to retrieve the list of group members, and then iteratively call [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) until all members are retrieved.</span></span> <span data-ttu-id="ed497-151">Você deve chamar [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) depois de processar cada estrutura de membro e deve fechar a enumeração chamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) quando o processamento for concluído.</span><span class="sxs-lookup"><span data-stu-id="ed497-151">You should call [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) after you process each member structure, and you must close the enumeration by calling [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) when processing is complete.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: UpdateParticipantList
//
// Purpose:  Update the list of partipants.
//
// Returns:  nothing
//
void UpdateParticipantList(void)
{
    HRESULT          hr = S_OK;
    HPEERENUM        hPeerEnum = NULL;
    PEER_MEMBER   ** ppMember = NULL;

    ClearParticipantList( );
    if (NULL == g_hGroup)
    {
        return;
    }

    // Retrieve only the members currently present in the group.
    hr = PeerGroupEnumMembers(g_hGroup, PEER_MEMBER_PRESENT, NULL, &hPeerEnum);
    if (SUCCEEDED(hr))
    {
        while (SUCCEEDED(hr))
        {
            ULONG cItem = 1;
            hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID **) &ppMember);
            if (SUCCEEDED(hr))
            {
                if (0 == cItem)
                {
                    PeerFreeData(ppMember);
                    break;
                }
            }

            if (SUCCEEDED(hr))
            {
                if (0 != ((*ppMember)->dwFlags & PEER_MEMBER_PRESENT))
                {
                    AddParticipantName((*ppMember)->pwzIdentity, (*ppMember)->pCredentialInfo->pwzFriendlyName);
                }
                PeerFreeData(ppMember);
            }
        }

        PeerEndEnumeration(hPeerEnum);
    }
}
```



## <a name="sending-a-chat-message"></a><span data-ttu-id="ed497-152">Enviando uma mensagem de chat</span><span class="sxs-lookup"><span data-stu-id="ed497-152">Sending a Chat Message</span></span>

<span data-ttu-id="ed497-153">Neste exemplo, uma mensagem de chat é enviada colocando-a no campo de **dados** de uma estrutura de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="ed497-153">In this example, a chat message is sent by placing it in the **data** field of a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="ed497-154">O registro é adicionado aos registros de grupo de pares chamando [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), que irá publicá-lo e gerar o \_ evento de alteração de registro de evento de grupo par \_ \_ \_ em todos os pares que participam do grupo de pares.</span><span class="sxs-lookup"><span data-stu-id="ed497-154">The record is added to the peer group records by calling [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), which will publish it and raise the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event on all peers participating in the peer group.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: AddChatRecord
//
// Purpose:  This adds a new chat message record to the group.
//
// Returns:  HRESULT
//
HRESULT AddChatRecord(PCWSTR pwzMessage)
{
    HRESULT     hr = S_OK;
    PEER_RECORD record = {0};
    GUID        idRecord;
    ULONGLONG   ulExpire;
    ULONG cch = (ULONG) wcslen(pwzMessage);

    GetSystemTimeAsFileTime((FILETIME *) &ulExpire);

    // Calculate a 2 minute expiration time in 100 nanosecond resolution
    ulExpire += ((ULONGLONG) 60 * 2) * ((ULONGLONG)1000*1000*10);

    // Set up the record
    record.dwSize = sizeof(record);
    record.data.cbData = (cch+1) * sizeof(WCHAR);
    record.data.pbData = (PBYTE) pwzMessage;
    memcpy(&record.ftExpiration, &ulExpire, sizeof(ulExpire));

    PeerGroupUniversalTimeToPeerTime(g_hGroup, &record.ftExpiration, &record.ftExpiration);

    // Set the record type GUID
    record.type = RECORD_TYPE_CHAT_MESSAGE;

    // Add the record to the database
    hr = PeerGroupAddRecord(g_hGroup, &record, &idRecord);
    if (FAILED(hr))
    {
        DisplayHrError(L"Failed to add a chat record to the group.", hr);
    }

    return hr;
}
```



## <a name="receiving-a-chat-message"></a><span data-ttu-id="ed497-155">Recebendo uma mensagem de chat</span><span class="sxs-lookup"><span data-stu-id="ed497-155">Receiving a Chat Message</span></span>

<span data-ttu-id="ed497-156">Para receber a mensagem de chat, crie uma função de retorno de chamada para o \_ evento de alteração de registro de evento de grupo par \_ \_ \_ que chama uma função semelhante a uma abaixo.</span><span class="sxs-lookup"><span data-stu-id="ed497-156">To receive the chat message, create a callback function for the PEER\_GROUP\_EVENT\_RECORD\_CHANGED event that calls a function similar to one below.</span></span> <span data-ttu-id="ed497-157">O registro é obtido chamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) nos dados de evento recebidos por uma chamada anterior para [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) na função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed497-157">The record is obtained by calling [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) on the event data received by a previous call to [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) in the callback function.</span></span> <span data-ttu-id="ed497-158">A mensagem de chat é armazenada no campo de **dados** desse registro.</span><span class="sxs-lookup"><span data-stu-id="ed497-158">The chat message is stored in the **data** field of this record.</span></span>


```C++
//-----------------------------------------------------------------------------
// Function: ProcessRecordChanged
//
// Purpose:  Processes the PEER_GROUP_EVENT_RECORD_CHANGED event.
//
// Returns:  nothing
//
void ProcessRecordChanged(PEER_EVENT_RECORD_CHANGE_DATA * pData)
{
    switch (pData->changeType)
    {
        case PEER_RECORD_ADDED:
            if (IsEqualGUID(&pData->recordType, &RECORD_TYPE_CHAT_MESSAGE))
            {
                PEER_RECORD * pRecord = {0};
                HRESULT hr = PeerGroupGetRecord(g_hGroup, &pData->recordId, &pRecord);
                if (SUCCEEDED(hr))
                {
                    DisplayChatMessage(pRecord->pwzCreatorId, (PCWSTR) pRecord->data.pbData);
                    PeerFreeData(pRecord);
                }
            }
            break;

        case PEER_RECORD_UPDATED:
        case PEER_RECORD_DELETED:
        case PEER_RECORD_EXPIRED:
            break;

        default:
            break;
    }
}
```



 

 



