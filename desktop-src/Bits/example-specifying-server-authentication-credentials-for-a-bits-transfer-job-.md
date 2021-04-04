---
title: Especificar credenciais de autenticação de servidor para um trabalho de transferência de BITS
description: Você pode especificar esquemas de autenticação diferentes para um trabalho de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS).
ms.assetid: 31db38f6-3639-4042-97f2-4f9d78942e15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c4373cdf0c8b4c8afe7dff367fda9387eec0b54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008348"
---
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a>Especificar credenciais de autenticação de servidor para um trabalho de transferência de BITS

Você pode especificar esquemas de autenticação diferentes para um trabalho de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS).

O procedimento a seguir obtém um esquema de autenticação e cria uma estrutura de identidade de autenticação. Em seguida, o aplicativo cria um trabalho de download de BITS e define as credenciais para o trabalho. Depois que o trabalho é criado, o aplicativo obtém um ponteiro para uma interface de retorno de chamada e sonda o status do trabalho de transferência do BITS. Depois que o trabalho for concluído, ele será removido da fila.

Este exemplo usa o cabeçalho e a implementação definidos no [exemplo: classes comuns](common-classes.md).

**Para especificar credenciais de autenticação de servidor para um trabalho de transferência de BITS**

1.  Crie uma estrutura de contêiner que mapeie os valores do [**\_ \_ esquema de autenticação BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) para nomes de esquema.

    ```C++
    struct
    {
        LPCWSTR        Name;
        BG_AUTH_SCHEME Scheme;
    }
    SchemeNames[] =
    {
        { L"basic",      BG_AUTH_SCHEME_BASIC },
        { L"digest",     BG_AUTH_SCHEME_DIGEST },
        { L"ntlm",       BG_AUTH_SCHEME_NTLM },
        { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
        { L"passport",   BG_AUTH_SCHEME_PASSPORT },

        { NULL,         BG_AUTH_SCHEME_BASIC }
    };
    ```

    

2.  Inicialize os parâmetros COM chamando a função CCoInitializer. Para obter mais informações sobre a função CCoInitializer, consulte [exemplo: classes comuns](common-classes.md).
3.  Prepare uma estrutura de [**\_ \_ credenciais de autenticação BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) . O exemplo usa a função [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) para limpar os locais de memória associados às informações confidenciais. A função [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) é definida em Winbase. h.
4.  Use a função getscheme para obter o esquema de autenticação a ser usado para se conectar ao servidor.

    ```C++
    bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
    {
        int i;

        i = 0;
        while (SchemeNames[i].Name != NULL)
        {
            if (0 == _wcsicmp( s, SchemeNames[i].Name ))
            {

                *scheme = SchemeNames[i].Scheme;
                return true;
            }

            ++i;
        }

        return false;
    }
    ```

    

5.  Preencha a estrutura de [**\_ \_ credenciais de autenticação BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) com o esquema de autenticação retornado pela função getscheme e o nome de usuário e a senha que foram passados para a função autenticação.
6.  Obtenha um ponteiro para a interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).
7.  Inicialize a segurança do processo COM chamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). O BITS requer pelo menos o nível de representação representada. BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido.
8.  Obtenha um ponteiro para a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e obtenha o localizador inicial para o bits chamando a função [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
9.  Crie um trabalho de transferência de BITS chamando o método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
10. Obtenha um ponteiro para a interface de retorno de chamada CNotifyInterface e chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para receber a notificação de eventos relacionados ao trabalho. Para obter mais informações sobre CNotifyInterface, consulte [exemplo: classes comuns](common-classes.md).
11. Chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para definir os tipos de notificações a serem recebidas. Neste exemplo, os sinalizadores de erro de trabalho de **\_ notificação BG \_ \_ transferidos** e **BG \_ \_ \_ notificam** são definidos.
12. Obtenha um ponteiro para a interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Use o ponteiro **IBackgroundCopyJob2** para definir propriedades adicionais no trabalho. Este programa usa o método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para definir as credenciais para o trabalho de transferência de bits.
13. Adicione arquivos ao trabalho de transferência BITS chamando [**método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile). Neste exemplo, o método **método ibackgroundcopyjob:: AddFile** usa as variáveis remotefile e LocalFile que foram passadas para a função autenticação.
14. Depois que o arquivo for adicionado, chame [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para retomar o trabalho.
15. Configure um loop while para aguardar a mensagem sair da interface de retorno de chamada enquanto o trabalho está sendo transferido.

    > [!Note]  
    > Esta etapa será necessária apenas se o apartamento COM for um apartamento de thread único. Para obter mais informações, consulte [Apartments de thread único](../com/single-threaded-apartments.md).

     

    ```C++
    // Wait for QuitMessage from CallBack
        DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
        while (dwLimit > GetTickCount())
        {
            MSG msg;

            while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                // If it is a quit message, exit.
                if (msg.message == WM_QUIT) 
                {
                    return;
                }

                // Otherwise, dispatch the message.
                DispatchMessage(&msg); 
            } // End of PeekMessage while loop
        }
    ```

    

    O loop anterior usa a função [ObterContagemMarcaEscala](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar o número de milissegundos decorridos desde que o trabalho começou a ser transferido.

16. Depois que o trabalho de transferência do BITS for concluído, remova o trabalho da fila chamando [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).

O exemplo de código a seguir especifica as credenciais de autenticação de servidor para um trabalho de transferência de BITS.


```C++
#include <bits.h>
#include <bits4_0.h>
#include <stdio.h>
#include <tchar.h>
#include <lm.h>
#include <iostream>
#include <exception>
#include <string>
#include <atlbase.h>
#include <memory>
#include <new>
#include "CommonCode.h"

//
// Retrieve BG_AUTH_SCHEME from scheme name.
//
//
struct
{
    LPCWSTR        Name;
    BG_AUTH_SCHEME Scheme;
}
SchemeNames[] =
{
    { L"basic",      BG_AUTH_SCHEME_BASIC },
    { L"digest",     BG_AUTH_SCHEME_DIGEST },
    { L"ntlm",       BG_AUTH_SCHEME_NTLM },
    { L"negotiate",  BG_AUTH_SCHEME_NEGOTIATE },
    { L"passport",   BG_AUTH_SCHEME_PASSPORT },

    { NULL,         BG_AUTH_SCHEME_BASIC }
};

bool GetScheme( LPCWSTR s, BG_AUTH_SCHEME *scheme )
{
    int i;

    i = 0;
    while (SchemeNames[i].Name != NULL)
    {
        if (0 == _wcsicmp( s, SchemeNames[i].Name ))
        {

            *scheme = SchemeNames[i].Scheme;
            return true;
        }

        ++i;
    }

    return false;
}

void ServerAuthentication(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &scheme, const LPWSTR &username, const LPWSTR &password)
{

 // If CoInitializeEx fails, the exception is unhandled and the program terminates  
 CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    // Prepare the credentials structure.
    BG_AUTH_CREDENTIALS cred;
    ZeroMemory(&cred, sizeof(cred));
    if (!GetScheme(scheme,&cred.Scheme))
    {
        wprintf(L"Invalid authentication scheme specified\n");
        return;
    }

    cred.Target = BG_AUTH_TARGET_SERVER;
    cred.Credentials.Basic.UserName = username;
    if (0 == _wcsicmp(cred.Credentials.Basic.UserName, L"NULL"))
    {
        cred.Credentials.Basic.UserName = NULL;
    }

    cred.Credentials.Basic.Password = password;
    if (0 == _wcsicmp(cred.Credentials.Basic.Password, L"NULL"))
    {
        cred.Credentials.Basic.Password = NULL;
    }

    CComPtr<IBackgroundCopyJob> pJob;
    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(NULL, 
            -1, 
            NULL, 
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL, 
            EOAC_DYNAMIC_CLOAKING, 
            0);
        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void**)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"BitsAuthSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetNotifyFlags");
        }

        // Set credentials.
        CComPtr<IBackgroundCopyJob2> job2;
        hr = pJob.QueryInterface(&job2);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"QueryInterface");
        }

        hr = job2->SetCredentials(&cred);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"SetCredentials");
        }

        // Add a file.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile, localFile);
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"Resume");
        }
    }
    catch(const std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }
    catch(const MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

    // Wait for QuitMessage from CallBack.
    DWORD dwLimit = GetTickCount() + (15 * 60 * 1000);  // set 15 minute limit
    while (dwLimit > GetTickCount())
    {
        MSG msg;

        while (PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
        { 
            // If it is a quit message, exit.
            if (msg.message == WM_QUIT) 
            {
                return;
            }

            // Otherwise, dispatch the message.
            DispatchMessage(&msg); 
        } // End of PeekMessage while loop
    }

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s", argv[0]);
        wprintf(L" [remote name] [local name] [server authentication scheme =\"NTLM\"|\"NEGOTIATE\"|\"BASIC\"|\"DIGEST\"] [username] [password]\n");
        return;
    }

    ServerAuthentication(argv[1], argv[2], argv[3], argv[4], argv[5]); 

}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**Método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Exemplo: classes comuns](common-classes.md)
</dt> </dl>

 

 