---
title: Exemplo de adição de um token auxiliar a um trabalho de transferência de BITS
description: Você pode configurar um trabalho de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS) com um token de segurança adicional. O trabalho de transferência de BITS usa esse token auxiliar para autenticação e para acessar recursos.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab12fe93ae54d91d02bef5e59e99d267571413e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008096"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a><span data-ttu-id="11504-104">Exemplo: adicionando um token auxiliar a um trabalho de transferência de BITS</span><span class="sxs-lookup"><span data-stu-id="11504-104">Example: Adding a Helper Token to a BITS Transfer Job</span></span>

<span data-ttu-id="11504-105">Você pode configurar um trabalho de transferência de Serviço de Transferência Inteligente em Segundo Plano (BITS) com um token de segurança adicional.</span><span class="sxs-lookup"><span data-stu-id="11504-105">You can configure a Background Intelligent Transfer Service (BITS) transfer job with an additional security token.</span></span> <span data-ttu-id="11504-106">O trabalho de transferência de BITS usa esse token auxiliar para autenticação e para acessar recursos.</span><span class="sxs-lookup"><span data-stu-id="11504-106">The BITS transfer job uses this helper token for authentication and to access resources.</span></span>

<span data-ttu-id="11504-107">Para obter mais informações, consulte [tokens auxiliares para trabalhos de transferência do bits](helper-tokens-for-bits-transfer-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="11504-107">For more information, see [Helper tokens for BITS transfer jobs](helper-tokens-for-bits-transfer-jobs.md).</span></span>

<span data-ttu-id="11504-108">O procedimento a seguir cria um trabalho de transferência de BITS no contexto do usuário local, obtém as credenciais de um segundo usuário, cria um token auxiliar com essas credenciais e, em seguida, define o token auxiliar no trabalho de transferência BITS.</span><span class="sxs-lookup"><span data-stu-id="11504-108">The following procedure creates a BITS transfer job in the context of the local user, gets credentials of a second user, creates a helper token with these credentials, and then sets the helper token on the BITS transfer job.</span></span>

<span data-ttu-id="11504-109">Este exemplo usa o cabeçalho e a implementação definidos no [exemplo: classes comuns](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="11504-109">This example uses the header and implementation defined in [Example: Common Classes](common-classes.md).</span></span>

<span data-ttu-id="11504-110">**Para adicionar um token auxiliar a um trabalho de transferência de BITS**</span><span class="sxs-lookup"><span data-stu-id="11504-110">**To add a helper token to a BITS transfer job**</span></span>

1.  <span data-ttu-id="11504-111">Inicialize os parâmetros COM chamando a função CCoInitializer.</span><span class="sxs-lookup"><span data-stu-id="11504-111">Initialize COM parameters by calling the CCoInitializer function.</span></span> <span data-ttu-id="11504-112">Para obter mais informações sobre a função CCoInitializer, consulte [exemplo: classes comuns](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="11504-112">For more information about the CCoInitializer function, see [Example: Common Classes](common-classes.md).</span></span>
2.  <span data-ttu-id="11504-113">Obtenha um ponteiro para a interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) .</span><span class="sxs-lookup"><span data-stu-id="11504-113">Get a pointer to the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface.</span></span> <span data-ttu-id="11504-114">Este exemplo usa a [Classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) para gerenciar ponteiros de interface com.</span><span class="sxs-lookup"><span data-stu-id="11504-114">This example uses the [CComPtr Class](/cpp/atl/reference/ccomptr-class?view=vs-2019) to manage COM interface pointers.</span></span>
3.  <span data-ttu-id="11504-115">Inicialize a segurança do processo COM chamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="11504-115">Initialize COM process security by calling [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="11504-116">O BITS requer pelo menos o nível de representação representada.</span><span class="sxs-lookup"><span data-stu-id="11504-116">BITS requires at least the IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="11504-117">BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="11504-117">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span>
4.  <span data-ttu-id="11504-118">Obtenha um ponteiro para a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e obtenha o localizador inicial para o bits chamando a função [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="11504-118">Get a pointer to the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface, and obtain the initial locator to BITS by calling the [CoCreateInstance]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>
5.  <span data-ttu-id="11504-119">Crie um trabalho de transferência de BITS chamando o método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .</span><span class="sxs-lookup"><span data-stu-id="11504-119">Create a BITS transfer job by calling the [**IBackgroundCopyManager::CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) method.</span></span>
6.  <span data-ttu-id="11504-120">Obtenha um ponteiro para a interface de retorno de chamada CNotifyInterface e chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para receber a notificação de eventos relacionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="11504-120">Get a pointer to the CNotifyInterface callback interface, and call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to receive notification of job-related events.</span></span> <span data-ttu-id="11504-121">Para obter mais informações sobre CNotifyInterface, consulte [exemplo: classes comuns](common-classes.md).</span><span class="sxs-lookup"><span data-stu-id="11504-121">For more information about CNotifyInterface, see [Example: Common Classes](common-classes.md).</span></span>
7.  <span data-ttu-id="11504-122">Chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para definir os tipos de notificações a serem recebidas.</span><span class="sxs-lookup"><span data-stu-id="11504-122">Call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method to set the types of notifications to receive.</span></span> <span data-ttu-id="11504-123">Neste exemplo, os sinalizadores de erro de trabalho de **\_ notificação BG \_ \_ transferidos** e **BG \_ \_ \_ notificam** são definidos.</span><span class="sxs-lookup"><span data-stu-id="11504-123">In this example, the **BG\_NOTIFY\_JOB\_TRANSFERRED** and **BG\_NOTIFY\_JOB\_ERROR** flags are set.</span></span>
8.  <span data-ttu-id="11504-124">Obtenha um ponteiro para a interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) chamando o método **método ibackgroundcopyjob:: QueryInterface** com o identificador de interface apropriado.</span><span class="sxs-lookup"><span data-stu-id="11504-124">Get a pointer to the [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) interface by calling the **IBackgroundCopyJob::QueryInterface** method with the proper interface identifier.</span></span>
9.  <span data-ttu-id="11504-125">Tentativa de fazer logon no usuário do token auxiliar.</span><span class="sxs-lookup"><span data-stu-id="11504-125">Attempt to log on the user of the helper token.</span></span> <span data-ttu-id="11504-126">Crie um identificador de representação e chame a [função LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) para popular a alça de representação.</span><span class="sxs-lookup"><span data-stu-id="11504-126">Create an impersonation handle, and call the [LogonUser Function]( /windows/win32/api/winbase/nf-winbase-logonusera) to populate the impersonation handle.</span></span> <span data-ttu-id="11504-127">Se for bem-sucedido, chame a [função ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span><span class="sxs-lookup"><span data-stu-id="11504-127">If successful, call the [ImpersonateLoggedOnUser Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser).</span></span> <span data-ttu-id="11504-128">Se não for bem-sucedida, o exemplo chamará a [função RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para encerrar a representação do usuário conectado, um erro será gerado e o identificador será fechado.</span><span class="sxs-lookup"><span data-stu-id="11504-128">If unsuccessful, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
10. <span data-ttu-id="11504-129">Chame o método [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para representar o token do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="11504-129">Call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method to impersonate the token of the logged-on user.</span></span> <span data-ttu-id="11504-130">Se esse método falhar, o exemplo chamará a [função RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para encerrar a representação do usuário conectado, um erro será gerado e o identificador será fechado.</span><span class="sxs-lookup"><span data-stu-id="11504-130">If this method fails, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of the logged-on user, an error is thrown, and the handle is closed.</span></span>
    > [!Note]
    >
    > <span data-ttu-id="11504-131">Nas versões com suporte do Windows anteriores ao Windows 10, versão 1607, o proprietário do trabalho deve ter credenciais administrativas para chamar o método [**IBitsTokenOptions:: SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) .</span><span class="sxs-lookup"><span data-stu-id="11504-131">In supported versions of Windows before Windows 10, version 1607, the job owner must have administrative credentials to call the [**IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) method.</span></span>
    >
    > <span data-ttu-id="11504-132">A partir do Windows 10, versão 1607, os proprietários de trabalho de não-administrador podem definir tokens auxiliares não administradores em trabalhos BITS que eles possuem.</span><span class="sxs-lookup"><span data-stu-id="11504-132">Starting with Windows 10, version 1607, non-administrator job owners can set non-administrator helper tokens on BITS jobs they own.</span></span> <span data-ttu-id="11504-133">Os proprietários do trabalho ainda devem ter credenciais administrativas para definir tokens auxiliares com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="11504-133">Job owners must still have administrative credentials to set helper tokens with administrator privileges.</span></span>

     

11. <span data-ttu-id="11504-134">Chame o método [**IBitsTokenOptions:: SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) para especificar quais recursos acessar usando o contexto de segurança do token auxiliar.</span><span class="sxs-lookup"><span data-stu-id="11504-134">Call the [**IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) method to specify which resources to access using the helper token's security context.</span></span>
12. <span data-ttu-id="11504-135">Após a conclusão da representação, o exemplo chama a [função RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para encerrar a representação do usuário conectado e o identificador é fechado.</span><span class="sxs-lookup"><span data-stu-id="11504-135">After the impersonation is complete, the example calls the [RevertToSelf Function](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) to terminate the impersonation of logged on user, and the handle is closed.</span></span>
13. <span data-ttu-id="11504-136">Adicione arquivos ao trabalho de transferência BITS chamando [**método ibackgroundcopyjob:: AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span><span class="sxs-lookup"><span data-stu-id="11504-136">Add files to the BITS transfer job by calling [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).</span></span>
14. <span data-ttu-id="11504-137">Depois que o arquivo for adicionado, chame [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para retomar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="11504-137">After the file is added, call [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) to resume the job.</span></span>
15. <span data-ttu-id="11504-138">Configure um loop while para aguardar a mensagem de encerramento da interface de retorno de chamada enquanto o trabalho está sendo transferido.</span><span class="sxs-lookup"><span data-stu-id="11504-138">Set up a while loop to wait for the quit message from the callback interface while the job is transferring.</span></span> <span data-ttu-id="11504-139">O loop while usa a função [ObterContagemMarcaEscala](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar o número de milissegundos decorridos desde que o trabalho começou a ser transferido.</span><span class="sxs-lookup"><span data-stu-id="11504-139">The while loop uses the [GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) function to retrieve the number of milliseconds that have elapsed since the job started transferring.</span></span>
16. <span data-ttu-id="11504-140">Depois que o trabalho de transferência do BITS for concluído, remova o trabalho da fila chamando [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span><span class="sxs-lookup"><span data-stu-id="11504-140">After the BITS transfer job is complete, remove the job from the queue by calling [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).</span></span>

<span data-ttu-id="11504-141">O exemplo de código a seguir adiciona um token auxiliar a um trabalho de transferência de BITS.</span><span class="sxs-lookup"><span data-stu-id="11504-141">The following code example adds a helper token to a BITS transfer job.</span></span>


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


void HelperToken(const LPWSTR &remoteFile, const LPWSTR &localFile, const LPWSTR &domain, const LPWSTR &username, const LPWSTR &password)
{
// If CoInitializeEx fails, the exception is unhandled and the program terminates   
CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);

CComPtr<IBackgroundCopyJob> pJob; 

    try
    {
        //The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
        HRESULT hr = CoInitializeSecurity(
            NULL,
            -1,
            NULL,
            NULL,
            RPC_C_AUTHN_LEVEL_CONNECT,
            RPC_C_IMP_LEVEL_IMPERSONATE,
            NULL,
            EOAC_DYNAMIC_CLOAKING,
            0
            );

        if (FAILED(hr))
        {
            throw MyException(hr, L"CoInitializeSecurity");
        }

        // Connect to BITS.
        CComPtr<IBackgroundCopyManager> pQueueMgr;
        hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
            CLSCTX_LOCAL_SERVER,
            __uuidof(IBackgroundCopyManager),
            (void **)&pQueueMgr);

        if (FAILED(hr))
        {
            // Failed to connect.
            throw MyException(hr, L"CoCreateInstance");
        }

        // Create a job.
        wprintf(L"Creating Job...\n");

        GUID guidJob;
        hr = pQueueMgr->CreateJob(L"HelperTokenSample",
            BG_JOB_TYPE_DOWNLOAD,
            &guidJob,
            &pJob);


        if(FAILED(hr))
        {   
            // Failed to create job.
            throw MyException(hr, L"CreateJob");
        }

        // Set the File Completed call.
        CComPtr<CNotifyInterface> pNotify;    
        pNotify = new CNotifyInterface();
        hr = pJob->SetNotifyInterface(pNotify);
        if (FAILED(hr))
        {
            // Failed to SetNotifyInterface.
            throw MyException(hr, L"SetNotifyInterface");
        }
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
            BG_NOTIFY_JOB_ERROR);

        if (FAILED(hr))
        {
            // Failed to SetNotifyFlags.
            throw MyException(hr, L"SetNotifyFlags");
        }

        //Retrieve the IBitsTokenOptions interface pointer from the BITS transfer job.
        CComPtr<IBitsTokenOptions> pTokenOptions;
        hr = pJob->QueryInterface(__uuidof(IBitsTokenOptions), (void** ) &pTokenOptions);

        if (FAILED(hr))
        {
            // Failed to QueryInterface.
            throw MyException(hr, L"QueryInterface");
        }

        // Log on user of the helper token.
        wprintf(L"Credentials for helper token %s\\%s %s\n", domain, username, password);

        HANDLE hImpersonation = INVALID_HANDLE_VALUE;
        if(LogonUser(username, domain, password, LOGON32_LOGON_INTERACTIVE, LOGON32_PROVIDER_DEFAULT, &hImpersonation))
        {
            // Impersonate the logged-on user.
            if(ImpersonateLoggedOnUser(hImpersonation))
            {
                // Configure the impersonated logged-on user's token as the helper token.
                hr = pTokenOptions->SetHelperToken();        
                if (FAILED(hr))
                {
                    //Failed to set helper token.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperToken");
                }

                hr = pTokenOptions->SetHelperTokenFlags(BG_TOKEN_LOCAL_FILE);
                if (FAILED(hr))
                {
                    //Failed to set helper token flags.
                    CloseHandle(hImpersonation);
                    RevertToSelf();
                    throw MyException(hr, L"SetHelperTokenFlags");
                }

                RevertToSelf();
            }               
            CloseHandle(hImpersonation);
        }

        // Add a file.
        // Replace parameters with variables that contain valid paths.
        wprintf(L"Adding File to Job\n");
        hr = pJob->AddFile(remoteFile,localFile);

        if(FAILED(hr))
        {   
            //Failed to add file to job.
            throw MyException(hr, L"AddFile");
        }

        //Resume the job.
        wprintf(L"Resuming Job...\n");
        hr = pJob->Resume();
        if (FAILED(hr))
        {
            // Resume failed.                   
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
        wprintf(L"Error 0x%x occurred during operation", ex.Error);
        if (pJob)
        {
            pJob->Cancel();
        }

        return;
    }

    wprintf(L"Transferring file and waiting for callback.\n");

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

    pJob->Cancel();
    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{   
    if (argc != 6)
    {
        wprintf(L"Usage:");
        wprintf(L"%s ", argv[0]);
        wprintf(L"[remote name] [local name] [helpertoken domain] [helpertoken userrname] [helpertoken password]\n");
        return;
    }

    HelperToken(argv[1],argv[2],argv[3],argv[4],argv[5]);

}
```



## <a name="related-topics"></a><span data-ttu-id="11504-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11504-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11504-143">Tokens auxiliares para trabalhos de transferência de BITS</span><span class="sxs-lookup"><span data-stu-id="11504-143">Helper tokens for BITS transfer jobs</span></span>](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[<span data-ttu-id="11504-144">**IBitsTokenOptions**</span><span class="sxs-lookup"><span data-stu-id="11504-144">**IBitsTokenOptions**</span></span>](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[<span data-ttu-id="11504-145">Exemplo: classes comuns</span><span class="sxs-lookup"><span data-stu-id="11504-145">Example: Common Classes</span></span>](common-classes.md)
</dt> </dl>

 

 