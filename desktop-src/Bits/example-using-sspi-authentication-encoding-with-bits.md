---
title: Exemplo de como usar a codificação de autenticação SSPI com BITS
description: Você pode usar a Autenticação do SSPI (Security Support Provider Interface) e os métodos Serviço de Transferência Inteligente em Segundo Plano (BITS) para obter as credenciais de um usuário, codificar as credenciais e definir as credenciais codificadas em um trabalho de transferência de BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13abe9b0bb6d8d4252575f70738f7b2f1a5c42b4cae1a4f042725c7bae15ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528796"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Exemplo: Usando a codificação de autenticação SSPI com BITS

Você pode usar a Autenticação do SSPI (Security Support Provider Interface) e os métodos Serviço de Transferência Inteligente em Segundo Plano (BITS) para obter as credenciais de um usuário, codificar as credenciais e definir as credenciais codificadas em um trabalho de transferência de BITS. A codificação é necessária para converter a estrutura de credenciais em cadeias de caracteres que podem ser passadas para um trabalho de transferência de BITS.

Para obter mais informações sobre métodos e autenticação SSPI, consulte [SSPI](../secauthn/sspi.md).

O procedimento a seguir solicita credenciais do usuário usando o pacote de segurança Negotiate. O programa cria uma estrutura de identidade de autenticação e popula a estrutura com as cadeias de caracteres codificadas que representam o nome de usuário, o domínio e a senha do usuário. Em seguida, o programa cria um trabalho de download do BITS e define o nome de usuário codificado e a senha como as credenciais para o trabalho. O programa libera a estrutura de identidade de autenticação depois que ela não é mais necessária.

Este exemplo usa o header e a implementação definidos [em Example: Common Classes](common-classes.md).

**Para usar a codificação de autenticação SSPI com trabalhos de transferência de BITS**

1.  Inicialize parâmetros COM chamando a função CCoInitializer. Para obter mais informações sobre a função CCoInitializer, consulte [Example: Common Classes](common-classes.md).
2.  Obter ponteiros para as interfaces [**IBackgroundCopyManager,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) [**IBackgroundCopyJob,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) [**IBackgroundCopyJob2.**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) Este exemplo usa a [Classe CComPtr para](/cpp/atl/reference/ccomptr-class?view=vs-2019) gerenciar ponteiros de interface COM.
3.  Crie uma [estrutura CREDUI \_ INFO](/windows/win32/api/wincred/ns-wincred-credui_infoa) que contém informações para personalizar a aparência da caixa de diálogo para a [função SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa). Em seguida, solicitar credenciais do usuário. Para obter mais informações, consulte a [função SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).
4.  Codifique a estrutura de credenciais como cadeias de caracteres que podem ser passadas para um trabalho de transferência bits usando a [função SspiEncodeAuthIdentityAsStrings.](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings)
5.  Preparar uma [**estrutura BG \_ AUTH \_ CREDENTIALS.**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials)
6.  Inicialize a segurança do processo COM chamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). BITS requer pelo menos o nível IMPERSONATE de representação. BITS falhará **com E \_ ACCESSDENIED se** o nível de representação correto não estiver definido.
7.  Obtenha o localizador inicial para BITS chamando a [função CoCreateInstance.](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
8.  Crie um trabalho de transferência de BITS chamando o [**método IBackgroundCopyManager::CreateJob.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob)
9.  Obter o identificador da interface [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) e chamar o **método IBackgroundCopyJob::QueryInterface.**
10. Preencha a estrutura [**BG \_ AUTH \_ CREDENTIALS**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) com o nome de usuário codificado e as cadeias de caracteres de senha e de definir o esquema de autenticação como Negotiate (**BG \_ AUTH \_ SCHEME \_ NEGOTIATE**).
11. Use o [**ponteiro IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) para fazer solicitações para BITS. Este programa usa o [**método IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para definir as credenciais para o trabalho de transferência de BITS.
12. Adicione arquivos, modifique propriedades ou retome o trabalho de transferência bits.
13. Depois que o trabalho de transferência do BITS for concluído, remova o trabalho da fila chamando [**IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
14. Por fim, livre a estrutura de identidade de autenticação chamando a [função SspiFreeAuthIdentity.](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity)

O exemplo de código a seguir demonstra como usar a Codificação de Autenticação SSPI com trabalhos de transferência de BITS.


```C++
#define SECURITY_WIN32
#define _SEC_WINNT_AUTH_TYPES

#include <windows.h>
#include <ntsecapi.h>
#include <bits.h>
#include <sspi.h>
#include <wincred.h>
#include <iostream>
#include <atlbase.h>
#include "CommonCode.h"

void PromptForCredentials(PWSTR pwTargetName)
{
    HRESULT hr;
    
    // If CoInitializeEx fails, the exception is unhandled and the program terminates
    CCoInitializer coInitializer(COINIT_APARTMENTTHREADED);
    
    CComPtr<IBackgroundCopyManager> pQueueMgr;
    CComPtr<IBackgroundCopyJob> pJob;
    CComPtr<IBackgroundCopyJob2> pJob2;

    PSEC_WINNT_AUTH_IDENTITY_OPAQUE pAuthIdentityEx2 = NULL;
    DWORD dwFlags = 0;
    BOOL fSave = FALSE;
    BOOL bReturn = TRUE;

    CREDUI_INFO creduiInfo = { 0 };
    creduiInfo.cbSize = sizeof(creduiInfo);
    // Change the message text and caption to the actual text for your dialog.
    creduiInfo.pszMessageText = pwTargetName;
    creduiInfo.pszCaptionText = L"SSPIPFC title for the dialog box";

    try {
        // Prompt for credentials from user using Negotiate security package.
        DWORD dwRet = SspiPromptForCredentials(
            pwTargetName,
            &creduiInfo,
            0,
            L"Negotiate", 
            NULL,
            &pAuthIdentityEx2,
            &fSave,
            dwFlags
            );

        if (SEC_E_OK != dwRet) 
        {
            // Prompt for credentials failed.
            throw MyException(dwRet, L"SspiPromptForCredentials");
        }

        if (NULL != pAuthIdentityEx2) 
        {
            GUID guidJob;
            BG_AUTH_CREDENTIALS authCreds;

            PCWSTR pwUserName = NULL;
            PCWSTR pwDomainName = NULL;
            PCWSTR pwPassword = NULL;

            // Encode credential structure as strings that can
            // be passed to a BITS job.
            SECURITY_STATUS secStatus = SspiEncodeAuthIdentityAsStrings(
                pAuthIdentityEx2,
                &pwUserName,
                &pwDomainName,
                &pwPassword
                );

            if(SEC_E_OK != secStatus) 
            {
                // Encode authentication identity as strings.
                throw MyException(secStatus, L"SspiEncodeAuthIdentityAsStrings");   
            }

            // Show the encoded user name and domain name.
            wprintf(
                L"User Name: %s\nDomain Name: %s",
                pwUserName,
                pwDomainName
                );

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
            hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                CLSCTX_LOCAL_SERVER,
                __uuidof(IBackgroundCopyManager),
                (void**) &pQueueMgr);

            if (FAILED(hr))
            {
                // Failed to connect.
                throw MyException(hr, L"CoCreateInstance");
            }

            // Create a job.
            hr = pQueueMgr->CreateJob(
                L"EncodeSample", 
                BG_JOB_TYPE_DOWNLOAD, 
                &guidJob, 
                &pJob
                );

            if(FAILED(hr))
            {   
                // Failed to create a BITS job.
                throw MyException(hr, L"CreateJob");
            }

            // Get IBackgroundCopyJob2 interface.
            hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
            if (FAILED(hr)) 
            {
                // Failed to get a reference to the IBackgroundCopyJob2 interface.
                throw MyException(hr, L"QueryInterface(IBackgroundCopyJob2)");
            }

            // Create a BITS authentication structure from the encoded strings.
            authCreds.Target = BG_AUTH_TARGET_SERVER;
            authCreds.Scheme = BG_AUTH_SCHEME_NEGOTIATE;
            authCreds.Credentials.Basic.UserName = (LPWSTR)pwUserName;
            authCreds.Credentials.Basic.Password = (LPWSTR)pwPassword;

            // Set the credentials for the job.
            hr = pJob2->SetCredentials(&authCreds);
            if (FAILED(hr)) 
            {
                // Failed to set credentials.
                throw MyException(hr, L"SetCredentials");
            }

            // Modify the job's property values.
            // Add files to the job.
            // Activate (resume) the job in the transfer queue.

            // Remove the job from the transfer queue.
            hr = pJob->Complete();
            if (FAILED(hr)) 
            {
                // Failed to complete the job.
                throw MyException(hr, L"Complete");
            }
        }
    }
    catch(std::bad_alloc &)
    {
        wprintf(L"Memory allocation failed");
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }
    catch(MyException &ex)
    {
        wprintf(L"Error %x occurred during operation", ex.Error);
        if (pJob != NULL)
        {
            pJob->Cancel();
        }
    }

    // Free the auth identity structure.
    if (NULL != pAuthIdentityEx2)
    {
        SspiFreeAuthIdentity(pAuthIdentityEx2);
        pAuthIdentityEx2 = NULL;
    }

    return;
}

void _cdecl _tmain(int argc, LPWSTR* argv)
{
    PromptForCredentials(L"Target");
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[SSPI](../secauthn/sspi.md)
</dt> <dt>

[**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager)
</dt> <dt>

[**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Exemplo: Classes comuns](common-classes.md)
</dt> </dl>

 

 