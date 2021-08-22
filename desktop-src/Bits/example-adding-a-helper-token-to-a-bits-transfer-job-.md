---
title: Exemplo de adição de um token auxiliar a um trabalho de transferência de BITS
description: Você pode configurar um trabalho de transferência Serviço de Transferência Inteligente em Segundo Plano (BITS) com um token de segurança adicional. O trabalho de transferência de BITS usa esse token auxiliar para autenticação e para acessar recursos.
ms.assetid: 08670c6d-e589-41be-842d-597f460d9c97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4adab6ca8cebeeca9b9883e89db28205dfdab1ea43e05c01fd119c14c26d374
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528816"
---
# <a name="example-adding-a-helper-token-to-a-bits-transfer-job"></a>Exemplo: Adicionando um token auxiliar a um trabalho de transferência de BITS

Você pode configurar um trabalho de transferência Serviço de Transferência Inteligente em Segundo Plano (BITS) com um token de segurança adicional. O trabalho de transferência de BITS usa esse token auxiliar para autenticação e para acessar recursos.

Para obter mais informações, consulte [Tokens auxiliares para trabalhos de transferência de BITS](helper-tokens-for-bits-transfer-jobs.md).

O procedimento a seguir cria um trabalho de transferência de BITS no contexto do usuário local, obtém credenciais de um segundo usuário, cria um token auxiliar com essas credenciais e define o token auxiliar no trabalho de transferência do BITS.

Este exemplo usa o header e a implementação definidos [em Example: Common Classes](common-classes.md).

**Para adicionar um token auxiliar a um trabalho de transferência de BITS**

1.  Inicialize parâmetros COM chamando a função CCoInitializer. Para obter mais informações sobre a função CCoInitializer, consulte [Example: Common Classes](common-classes.md).
2.  Obter um ponteiro para a interface [**IBackgroundCopyJob.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) Este exemplo usa a [Classe CComPtr para](/cpp/atl/reference/ccomptr-class?view=vs-2019) gerenciar ponteiros de interface COM.
3.  Inicialize a segurança do processo COM chamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requer pelo menos o nível IMPERSONATE de representação. BITS falhará com E \_ ACCESSDENIED se o nível de representação correto não estiver definido.
4.  Obtenha um ponteiro para a interface [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) e obtenha o localizador inicial para BITS chamando a [função CoCreateInstance.]( /windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
5.  Crie um trabalho de transferência de BITS chamando o [**método IBackgroundCopyManager::CreateJob.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob)
6.  Obter um ponteiro para a interface de retorno de chamada CNotifyInterface e chamar o método [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para receber a notificação de eventos relacionados ao trabalho. Para obter mais informações sobre CNotifyInterface, consulte [Example: Common Classes](common-classes.md).
7.  Chame o [**método IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) para definir os tipos de notificações a receber. Neste exemplo, os sinalizadores **BG \_ NOTIFY JOB \_ \_ TRANSFERRED** e **BG NOTIFY JOB \_ \_ \_ ERROR** são definidos.
8.  Obter um ponteiro para a interface [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) chamando o método **IBackgroundCopyJob::QueryInterface** com o identificador de interface adequado.
9.  Tente fazer logoff no usuário do token auxiliar. Crie um alça de representação e chame a [Função LogonUser]( /windows/win32/api/winbase/nf-winbase-logonusera) para preencher o alça de representação. Se for bem-sucedido, [chame a função ImpersonateLoggedOnUser](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser). Se não for bem-sucedido, o exemplo chamará a Função [RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para encerrar a representação do usuário conectado, um erro será lançado e o handle será fechado.
10. Chame o [**método IBitsTokenOptions::SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken) para representar o token do usuário conectado. Se esse método falhar, o exemplo chamará a [Função RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para encerrar a representação do usuário conectado, um erro será lançado e o handle será fechado.
    > [!Note]
    >
    > Nas versões com suporte do Windows antes do Windows 10, versão 1607, o proprietário do trabalho deve ter credenciais administrativas para chamar o método [**IBitsTokenOptions::SetHelperToken.**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken)
    >
    > Começando com Windows 10, versão 1607, os proprietários de trabalhos não administradores podem definir tokens auxiliares não administradores em trabalhos BITS que eles têm. Os proprietários de trabalho ainda devem ter credenciais administrativas para definir tokens auxiliares com privilégios de administrador.

     

11. Chame o [**método IBitsTokenOptions::SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) para especificar quais recursos acessar usando o contexto de segurança do token auxiliar.
12. Depois que a representação for concluída, o exemplo chamará a [Função RevertToSelf](/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself) para encerrar a representação do usuário conectado e o handle será fechado.
13. Adicione arquivos ao trabalho de transferência bits chamando [**IBackgroundCopyJob::AddFile**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile).
14. Depois que o arquivo for adicionado, chame [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para retomar o trabalho.
15. Configurar um loop while para aguardar a mensagem de sair da interface de retorno de chamada enquanto o trabalho está sendo transferido. O loop while usa a [função GetTickCount](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) para recuperar o número de milissegundos decorridos desde que o trabalho começou a ser transferido.
16. Depois que o trabalho de transferência do BITS for concluído, remova o trabalho da fila chamando [**IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)

O exemplo de código a seguir adiciona um token auxiliar a um trabalho de transferência de BITS.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tokens auxiliares para trabalhos de transferência de BITS](helper-tokens-for-bits-transfer-jobs.md)
</dt> <dt>

[**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
</dt> <dt>

[Exemplo: Classes comuns](common-classes.md)
</dt> </dl>

 

 