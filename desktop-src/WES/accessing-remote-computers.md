---
title: Acessando computadores remotos
description: Você pode usar a API do log de eventos do Windows para acessar dados no computador local ou em um computador remoto.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0063238560ddd7f1613e94b83ecc7f27900bb3
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104084406"
---
# <a name="accessing-remote-computers"></a><span data-ttu-id="4bf80-103">Acessando computadores remotos</span><span class="sxs-lookup"><span data-stu-id="4bf80-103">Accessing Remote Computers</span></span>

<span data-ttu-id="4bf80-104">Você pode usar a API do log de eventos do Windows para acessar dados no computador local ou em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="4bf80-104">You can use the Windows Event Log API to access data on the local computer or on a remote computer.</span></span> <span data-ttu-id="4bf80-105">Para acessar dados em um computador remoto, você precisa chamar a função [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) para criar um contexto de sessão remota.</span><span class="sxs-lookup"><span data-stu-id="4bf80-105">To access data on a remote computer, you need to call the [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) function to create a remote session context.</span></span> <span data-ttu-id="4bf80-106">Ao chamar essa função, você especifica o nome do computador remoto ao qual deseja se conectar, as credenciais do usuário a serem usadas para fazer a conexão e o tipo de autenticação a ser usado para autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="4bf80-106">When you call this function, you specify the name of the remote computer that you want to connect to, the user credentials to use to make the connection, and the type of authentication to use to authenticate the user.</span></span> <span data-ttu-id="4bf80-107">Para especificar o usuário atual, defina o domínio, o usuário e os membros da senha como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4bf80-107">To specify the current user, set the Domain, User, and Password members to **NULL**.</span></span>

<span data-ttu-id="4bf80-108">Ao chamar a API de log de eventos do Windows, você passa o identificador para o contexto de sessão remota que a função [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) retorna.</span><span class="sxs-lookup"><span data-stu-id="4bf80-108">When you call Windows Event Log API, you pass the handle to the remote session context that the [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) function returns.</span></span> <span data-ttu-id="4bf80-109">(Para acessar dados no computador local, passe **NULL** para especificar a sessão padrão.) Para acessar dados no computador remoto, o computador remoto deve habilitar a exceção "gerenciamento remoto do log de eventos" do firewall do Windows; caso contrário, quando você tentar usar o identificador de sessão, a chamada será um erro com o \_ servidor RPC S \_ \_ indisponível.</span><span class="sxs-lookup"><span data-stu-id="4bf80-109">(To access data on the local computer, pass **NULL** to specify the default session.) To access data on the remote computer, the remote computer must enable the "Remote Event Log Management" Windows Firewall exception; otherwise, when you try to use the session handle, the call will error with RPC\_S\_SERVER\_UNAVAILABLE.</span></span> <span data-ttu-id="4bf80-110">O computador ao qual você está se conectando deve estar executando o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4bf80-110">The computer to which you are connecting must be running Windows Vista or later.</span></span>

<span data-ttu-id="4bf80-111">O exemplo a seguir mostra como se conectar a um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="4bf80-111">The following example shows how to connect to a remote computer.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote);
void EnumProviders(EVT_HANDLE hRemote);

void main(void)
{
    EVT_HANDLE hRemote = NULL;
    LPWSTR pwsComputerName = L"<name of the remote computer goes here>";
    

    // Enumerate the registered providers on the local computer.
    wprintf(L"Registered providers on the local computer\n\n");
    EnumProviders(hRemote);

    hRemote = ConnectToRemote(pwsComputerName);
    if (NULL == hRemote)
    {
        wprintf(L"Failed to connect to remote computer. Error code is %d.\n", GetLastError());
        goto cleanup;
    }

    // Enumerate the registered providers on the remote computer.
    // To access a remote computer, the remote computer must enable 
    // Remote Event Log Management as an exception in the firewall;
    // otherwise, the remote call fails with RPC_S_SERVER_UNAVAILABLE.
    wprintf(L"\n\nRegistered providers on the remote computer\n\n");
    EnumProviders(hRemote);

cleanup:

    if (hRemote)
        EvtClose(hRemote);
}

// Create a session conext for the remote computer. Set the 
// Domain, User, and Password member to NULL to specify
// the current user.
EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote)
{
    EVT_HANDLE hRemote = NULL;
    EVT_RPC_LOGIN Credentials;

    RtlZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));
    Credentials.Server = lpwszRemote;
    Credentials.Domain = NULL; 
    Credentials.User = NULL; 
    Credentials.Password = NULL; 
    Credentials.Flags = EvtRpcLoginAuthNegotiate; 

    // This call creates a remote session context; it does not actually
    // create a connection to the remote computer. The connection to
    // the remote computer happens when you use the context.
    hRemote = EvtOpenSession(EvtRpcLogin, &Credentials, 0, 0);

    SecureZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));

    return hRemote;
}

// Enumerate the registered providers on the computer.
void EnumProviders(EVT_HANDLE hRemote)
{
    EVT_HANDLE hPublishers = NULL;
    WCHAR wszPublisherName[255 + 1];
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    hPublishers = EvtOpenPublisherEnum(hRemote, 0);
    if (NULL == hPublishers)
    {
        wprintf(L"EvtOpenPublisherEnum failed with %d\n", GetLastError());
        goto cleanup;
    }

    while (true)
    {
        if (EvtNextPublisherId(hPublishers, sizeof(wszPublisherName)/sizeof(WCHAR), wszPublisherName, &dwBufferUsed))
        {
            wprintf(L"%s\n", wszPublisherName);
        }
        else
        {
            status = GetLastError();
            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else
            {
                wprintf(L"EvtNextPublisherId failed with 0x%ud\n", GetLastError());
            }
        }
    }

cleanup:

    if (hPublishers)
        EvtClose(hPublishers);
}
```
