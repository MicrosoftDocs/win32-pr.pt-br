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
# <a name="specify-server-authentication-credentials-for-a-bits-transfer-job"></a><span data-ttu-id="1da52-103">Especificar credenciais de autenticação de servidor para um trabalho de transferência de BITS</span><span class="sxs-lookup"><span data-stu-id="1da52-103">Specify server authentication credentials for a BITS transfer job</span></span>

<span data-ttu-id="1da52-104">Você pode especificar esquemas de autenticação diferentes para um trabalho de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="1da52-104">You can specify different authentication schemes for a Background Intelligent Transfer Service (BITS) transfer job.</span></span>

<span data-ttu-id="1da52-105">O procedimento a seguir obtém um esquema de autenticação e cria uma estrutura de identidade de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1da52-105">The following procedure gets an authentication scheme and creates an authentication identity structure.</span></span> <span data-ttu-id="1da52-106">Em seguida, o aplicativo cria um trabalho de download de BITS e define as credenciais para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1da52-106">Then the application creates a BITS download job and sets the credentials for the job.</span></span> <span data-ttu-id="1da52-107">Depois que o trabalho é criado, o aplicativo obtém um ponteiro para uma interface de retorno de chamada e sonda o status do trabalho de transferência do BITS.</span><span class="sxs-lookup"><span data-stu-id="1da52-107">After the job is created, the application gets a pointer to a callback interface and polls for the status of the BITS transfer job.</span></span> <span data-ttu-id="1da52-108">Depois que o trabalho for concluído, ele será removido da fila.</span><span class="sxs-lookup"><span data-stu-id="1da52-108">After the job is complete, it is removed from the queue.</span></span>

<span data-ttu-id="1da52-109">Este exemplo usa o cabeçalho e a implementação definidos no [exemplo: classes comuns](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1da52-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="1da52-110">**Para especificar credenciais de autenticação de servidor para um trabalho de transferência de BITS**</span><span class="sxs-lookup"><span data-stu-id="1da52-110">**To specify server authentication credentials for a BITS transfer job**</span></span>

1.  <span data-ttu-id="1da52-111">Crie uma estrutura de contêiner que mapeie os valores do [**\_ \_ esquema de autenticação BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) para nomes de esquema.</span><span class="sxs-lookup"><span data-stu-id="1da52-111">Create a container structure that maps [**BG\_AUTH\_SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme) values to scheme names.</span></span>

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

    

2.  <span data-ttu-id="1da52-112">Inicialize os parâmetros COM chamando a função CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="1da52-112">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="1da52-113">Para obter mais informações sobre a função CCoInitializer, consulte [exemplo: classes comuns](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1da52-113">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
3.  <span data-ttu-id="1da52-114">Prepare uma estrutura de [**\_ \_ credenciais de autenticação BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) .</span><span class="sxs-lookup"><span data-stu-id="1da52-114">Prepare a [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure.</span></span> <span data-ttu-id="1da52-115">O exemplo usa a função [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) para limpar os locais de memória associados às informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="1da52-115">The example uses the [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function to clear the memory locations associated with the sensitive information.</span></span> <span data-ttu-id="1da52-116">A função [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) é definida em Winbase. h.</span><span class="sxs-lookup"><span data-stu-id="1da52-116">The [SecureZeroMemory]( /previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function is defined in WinBase.h.</span></span>
4.  <span data-ttu-id="1da52-117">Use a função getscheme para obter o esquema de autenticação a ser usado para se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="1da52-117">Use the GetScheme function to get the authentication scheme to use to connect to the server.</span></span>

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

    

5.  <span data-ttu-id="1da52-118">Preencha a estrutura de [**\_ \_ credenciais de autenticação BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) com o esquema de autenticação retornado pela função getscheme e o nome de usuário e a senha que foram passados para a função autenticação.</span><span class="sxs-lookup"><span data-stu-id="1da52-118">Populate the [**BG\_AUTH\_CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_auth_credentials) structure with the authentication scheme returned by the GetScheme function and the user name and password that were passed into the ServerAuthentication function.</span></span>
6.  <span data-ttu-id="1da52-119">Obtenha um ponteiro para a interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) (pJob).</span><span class="sxs-lookup"><span data-stu-id="1da52-119">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface (pJob).</span></span>
7.  <span data-ttu-id="1da52-120">Inicialize a segurança do processo COM chamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="1da52-120">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="1da52-121">O BITS requer pelo menos o nível de representação representada.</span><span class="sxs-lookup"><span data-stu-id="1da52-121">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="1da52-122">BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="1da52-122">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
8.  <span data-ttu-id="1da52-123">Obtenha um ponteiro para a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e obtenha o localizador inicial para o bits chamando a função [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="1da52-123">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
9.  <span data-ttu-id="1da52-124">Crie um trabalho de transferência de BITS chamando o método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="1da52-124">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
10. <span data-ttu-id="1da52-125">Obtenha um ponteiro para a interface de retorno de chamada CNotifyInterface e chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para receber a notificação de eventos relacionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="1da52-125">Get a pointer to the CNotifyInterface callback interface and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="1da52-126">Para obter mais informações sobre CNotifyInterface, consulte [exemplo: classes comuns](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1da52-126">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
11. <span data-ttu-id="1da52-127">Chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para definir os tipos de notificações a serem recebidas.</span><span class="sxs-lookup"><span data-stu-id="1da52-127">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="1da52-128">Neste exemplo, os sinalizadores de erro de trabalho de **\_ notificação BG \_ \_ transferidos** e **BG \_ \_ \_ notificam** são definidos.</span><span class="sxs-lookup"><span data-stu-id="1da52-128">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
12. <span data-ttu-id="1da52-129">Obtenha um ponteiro para a interface [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) .</span><span class="sxs-lookup"><span data-stu-id="1da52-129">Get a pointer to the [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) interface.</span></span> <span data-ttu-id="1da52-130">Use o ponteiro **IBackgroundCopyJob2** para definir propriedades adicionais no trabalho.</span><span class="sxs-lookup"><span data-stu-id="1da52-130">Use the **IBackgroundCopyJob2** pointer to set additional properties on the job.</span></span> <span data-ttu-id="1da52-131">Este programa usa o método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para definir as credenciais para o trabalho de transferência de bits.</span><span class="sxs-lookup"><span data-stu-id="1da52-131">This program uses the [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) method to set the credentials for the BITS transfer job.</span></span>
13. <span data-ttu-id="1da52-132">Adicione arquivos ao trabalho de transferência BITS chamando [**método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="1da52-132">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span> <span data-ttu-id="1da52-133">Neste exemplo, o método **método ibackgroundcopyjob:: AddFile** usa as variáveis remotefile e LocalFile que foram passadas para a função autenticação.</span><span class="sxs-lookup"><span data-stu-id="1da52-133">In this example, the **IBackgroundCopyJob::AddFile** method uses the remoteFile and localFile variables that were passed into the ServerAuthentication function.</span></span>
14. <span data-ttu-id="1da52-134">Depois que o arquivo for adicionado, chame [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para retomar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="1da52-134">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="1da52-135">Configure um loop while para aguardar a mensagem sair da interface de retorno de chamada enquanto o trabalho está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="1da52-135">Set up a while loop to wait for Quit Message from the callback interface while the job is transferring.</span></span>

    > [!Note]  
    > <span data-ttu-id="1da52-136">Esta etapa será necessária apenas se o apartamento COM for um apartamento de thread único.</span><span class="sxs-lookup"><span data-stu-id="1da52-136">This step is necessary only if the COM apartment is a single-threaded apartment.</span></span> <span data-ttu-id="1da52-137">Para obter mais informações, consulte [Apartments de thread único](../com/single-threaded-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="1da52-137">For more information, see [Single-Threaded Apartments](../com/single-threaded-apartments.md).</span></span>

     

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

    

    <span data-ttu-id="1da52-138">O loop anterior usa a função [ObterContagemMarcaEscala](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar o número de milissegundos decorridos desde que o trabalho começou a ser transferido.</span><span class="sxs-lookup"><span data-stu-id="1da52-138">The preceding loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>

16. <span data-ttu-id="1da52-139">Depois que o trabalho de transferência do BITS for concluído, remova o trabalho da fila chamando [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="1da52-139">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="1da52-140">O exemplo de código a seguir especifica as credenciais de autenticação de servidor para um trabalho de transferência de BITS.</span><span class="sxs-lookup"><span data-stu-id="1da52-140">The following code example specifies server authentication credentials for a BITS transfer job.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1da52-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1da52-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1da52-142">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="1da52-142">**IBackgroundCopyManager**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[<span data-ttu-id="1da52-143">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="1da52-143">**IBackgroundCopyJob**</span></span>](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[<span data-ttu-id="1da52-144">**IBackgroundCopyJob2**</span><span class="sxs-lookup"><span data-stu-id="1da52-144">**IBackgroundCopyJob2**</span></span>](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[<span data-ttu-id="1da52-145">Exemplo: classes comuns</span><span class="sxs-lookup"><span data-stu-id="1da52-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 