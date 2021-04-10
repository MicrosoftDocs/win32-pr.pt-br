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
# <a name="creating-a-group-chat-application"></a>Criando um aplicativo de chat de grupo

Este tópico fornece exemplos de código relevantes para as principais etapas do desenvolvimento de um aplicativo de chat com a API de agrupamento de pares, fornecendo um contexto para cada chamada à API. Os comportamentos da interface do usuário e a estrutura geral do aplicativo não estão incluídos.

> [!Note]  
> O aplicativo de exemplo de chat do grupo de pares completo é fornecido no SDK do par. Este tópico faz referência às funções fornecidas no exemplo.

 

## <a name="initializing-a-group"></a>Inicializando um grupo

A primeira etapa ao construir um aplicativo de chat é inicializar a infraestrutura de agrupamento de pares chamando [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) com a versão mais alta com suporte. Nesse caso, a **\_ \_ versão do grupo de pares** será definida no arquivo de cabeçalho do aplicativo. A versão realmente suportada pela infraestrutura é retornada em **peerVersion**.


```C++
    PEER_VERSION_DATA peerVersion;

    hr = PeerGroupStartup(PEER_GROUP_VERSION, &peerVersion);
    if (FAILED(hr))
    {
        return hr;
    }
```



## <a name="creating-a-group"></a>Criando um grupo

Um aplicativo de chat deve ser capaz de criar um grupo de pares se nenhum grupo estiver disponível para junção ou se o usuário do aplicativo quiser criar um novo. Para fazer isso, você deve criar uma estrutura de [**\_ \_ Propriedades de grupo par**](/windows/desktop/api/P2P/ns-p2p-peer_group_properties) e preenchê-la com as configurações iniciais para o grupo, incluindo o classificador para o grupo par, o nome amigável, o nome de par do criador e o tempo de vida da presença. Depois que essa estrutura tiver sido populada, passe-a para [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).


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



## <a name="issuing-invitations"></a>Emitindo convites

Ao emitir um convite, o GMCs dos convidados deve ser obtido. Eles podem ser obtidos chamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) no convite com seu nome de identidade. Se for bem-sucedido, as informações de identidade (o XML que contém o certificado codificado em base 64 com a chave pública RSA) serão gravadas em um local externo (um arquivo, neste exemplo) em que o emissor pode obtê-lo e usá-lo para criar um convite.

Neste ponto, deve-se estabelecer um mecanismo para a entrega do convite ao convidado. Esse pode ser um email ou outro método seguro de troca de arquivos. No exemplo a seguir, o convite é gravado em um arquivo que pode ser transferido para o computador do convidado.


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



Convites, como identidades, também são emitidos externamente. Neste exemplo, o convite é gravado em um arquivo com **fputws** , onde o convidado pode obtê-lo e usá-lo quando chama [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


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



## <a name="joining-a-peer-group"></a>Ingressando em um grupo de pares

Se o par estiver tentando ingressar em um grupo de pares criado por outro par, ele precisará de um convite desse ponto. Os convites são entregues por um processo ou aplicativo externo para o convidado e salvos em um arquivo local, especificado no exemplo abaixo como *pwzFileName*. O blob XML do convite é lido do arquivo para **wzInvitation** e passado para [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin).


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



## <a name="register-for-peer-events"></a>Registrar-se para eventos de pares

Antes de se conectar, você deve se registrar para cada evento de mesmo nível pertinente ao aplicativo. No exemplo abaixo, você se registra para os seguintes eventos:

-   registro de evento de grupo de pares \_ \_ \_ \_ alterado. Como os registros serão usados para conter mensagens de bate-papo públicas, o aplicativo deve ser notificado toda vez que um novo for adicionado. Quando esse evento de par é recebido, os dados de evento expõem o registro com a mensagem de chat. Os aplicativos devem ser registrados apenas para os tipos de registro que pretendem manipular diretamente.
-   membro de evento de grupo de pares \_ \_ \_ \_ alterado. O aplicativo deve ser notificado quando os membros ingressarem ou saírem do grupo par, de modo que a lista de participantes possa ser atualizada de acordo.
-   STATUS do evento do grupo de pares \_ \_ \_ \_ alterado. As alterações no status do grupo de pares devem ser transmitidas para o aplicativo. Um membro do grupo de pares só é considerado disponível dentro do grupo de pares quando seu status indica que ele está conectado ao grupo, sincronizado com o banco de dados de registro do grupo de pares e ouvindo ativamente as atualizações registradas.
-   \_conexão direta de evento de grupo de pares \_ \_ \_ . Mensagens privadas entre dois membros e trocas de dados devem ser realizadas em uma conexão direta, portanto, o aplicativo deve ser capaz de lidar com solicitações de conexão direta.
-   dados de entrada do evento do grupo de pares \_ \_ \_ \_ . Depois que uma conexão direta é iniciada, esse evento de mesmo nível alerta o aplicativo de que uma mensagem particular foi recebida.


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



## <a name="connecting-to-a-peer-group"></a>Conectando a um grupo de pares

Tendo criado ou Unido o grupo e registrado para os eventos apropriados, é hora de ficar online e iniciar uma sessão de bate-papo ativa. Para fazer isso, você chama [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) e passa o identificador de grupo obtido de [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) ou [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Depois de chamar isso, as mensagens de chat serão recebidas como eventos de alteração de registro de evento de grupo de pares \_ \_ \_ \_ .

## <a name="obtaining-a-list-of-peer-group-members"></a>Obtendo uma lista de membros do grupo de pares

A obtenção de uma lista de membros conectados ao grupo par é simples: chame [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) para recuperar a lista de membros do grupo e chame iterativamente [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) até que todos os membros sejam recuperados. Você deve chamar [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) depois de processar cada estrutura de membro e deve fechar a enumeração chamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) quando o processamento for concluído.


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



## <a name="sending-a-chat-message"></a>Enviando uma mensagem de chat

Neste exemplo, uma mensagem de chat é enviada colocando-a no campo de **dados** de uma estrutura de [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) . O registro é adicionado aos registros de grupo de pares chamando [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord), que irá publicá-lo e gerar o \_ evento de alteração de registro de evento de grupo par \_ \_ \_ em todos os pares que participam do grupo de pares.


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



## <a name="receiving-a-chat-message"></a>Recebendo uma mensagem de chat

Para receber a mensagem de chat, crie uma função de retorno de chamada para o \_ evento de alteração de registro de evento de grupo par \_ \_ \_ que chama uma função semelhante a uma abaixo. O registro é obtido chamando [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord) nos dados de evento recebidos por uma chamada anterior para [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) na função de retorno de chamada. A mensagem de chat é armazenada no campo de **dados** desse registro.


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



 

 



