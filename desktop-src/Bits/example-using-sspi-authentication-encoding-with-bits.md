---
title: Exemplo usando a codificação de autenticação SSPI com BITS
description: Você pode usar a autenticação SSPI (Security Support Provider interface) e os métodos de Serviço de Transferência Inteligente em Segundo Plano (BITS) para obter as credenciais de um usuário, codificar as credenciais e definir as credenciais codificadas em um trabalho de transferência de BITS.
ms.assetid: 5c8a6df7-0056-463e-8d73-1695dc75e023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b86248c4782789010a817755d9bc27b3e5373b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641815"
---
# <a name="example-using-sspi-authentication-encoding-with-bits"></a>Exemplo: usando a codificação de autenticação SSPI com BITS

Você pode usar a autenticação SSPI (Security Support Provider interface) e os métodos de Serviço de Transferência Inteligente em Segundo Plano (BITS) para obter as credenciais de um usuário, codificar as credenciais e definir as credenciais codificadas em um trabalho de transferência de BITS. A codificação é necessária para converter a estrutura de credenciais em cadeias de caracteres que podem ser passadas para um trabalho de transferência de BITS.

Para obter mais informações sobre a autenticação e os métodos SSPI, consulte [SSPI](../secauthn/sspi.md).

O procedimento a seguir solicita as credenciais do usuário usando o pacote de segurança Negotiate. O programa cria uma estrutura de identidade de autenticação e popula a estrutura com as cadeias de caracteres codificadas que representam o nome de usuário, o domínio e a senha do usuário. Em seguida, o programa cria um trabalho de download do BITS e define o nome de usuário e a senha codificados como as credenciais para o trabalho. O programa libera a estrutura de identidade de autenticação depois que ela não é mais necessária.

Este exemplo usa o cabeçalho e a implementação definidos no [exemplo: classes comuns](common-classes.md).

**Para usar a codificação de autenticação SSPI com trabalhos de transferência de BITS**

1.  Inicialize os parâmetros COM chamando a função CCoInitializer. Para obter mais informações sobre a função CCoInitializer, consulte [exemplo: classes comuns](common-classes.md).
2.  Obtenha ponteiros para as interfaces [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager), [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)e [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) . Este exemplo usa a [Classe CComPtr](/cpp/atl/reference/ccomptr-class?view=vs-2019) para gerenciar ponteiros de interface com.
3.  Crie uma estrutura de [ \_ informações do CREDUI](/windows/win32/api/wincred/ns-wincred-credui_infoa) que contenha informações para personalizar a aparência da caixa de diálogo da [função SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa). Em seguida, solicite as credenciais do usuário. Para obter mais informações, consulte a [função SspiPromptForCredentials](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa).
4.  Codifique a estrutura de credenciais como cadeias de caracteres que podem ser passadas para um trabalho de transferência de BITS usando a função [SspiEncodeAuthIdentityAsStrings](/windows/win32/api/sspi/nf-sspi-sspiencodeauthidentityasstrings) .
5.  Prepare uma estrutura de [**\_ \_ credenciais de autenticação BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) .
6.  Inicialize a segurança do processo COM chamando [CoInitializeSecurity](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). O BITS requer pelo menos o nível de representação representada. BITS falhará com **E \_ ACCESSDENIED** se o nível de representação correto não estiver definido.
7.  Obtenha o localizador inicial para BITS chamando a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .
8.  Crie um trabalho de transferência de BITS chamando o método [**IBackgroundCopyManager:: CreateJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) .
9.  Obtenha o identificador para a interface [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) e chame o método **método ibackgroundcopyjob:: QueryInterface** .
10. Preencha a estrutura de [**\_ \_ credenciais de autenticação BG**](/windows/desktop/api/bits1_5/ns-bits1_5-bg_auth_credentials) com as cadeias de caracteres de nome de usuário e senha codificadas e defina o esquema de autenticação como Negotiate (**BG \_ auth \_ Scheme \_ Negotiate**).
11. Use o ponteiro [**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2) para fazer solicitações para bits. Este programa usa o método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) para definir as credenciais para o trabalho de transferência de bits.
12. Adicionar arquivos, modificar propriedades ou retomar o trabalho de transferência do BITS.
13. Depois que o trabalho de transferência do BITS for concluído, remova o trabalho da fila chamando [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete).
14. Por fim, libere a estrutura de identidade de autenticação chamando a função [SspiFreeAuthIdentity](/windows/win32/api/sspi/nf-sspi-sspifreeauthidentity) .

O exemplo de código a seguir demonstra como usar a codificação de autenticação SSPI com trabalhos de transferência de BITS.


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

[**Método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob)
</dt> <dt>

[**IBackgroundCopyJob2**](/windows/desktop/api/bits1_5/nn-bits1_5-ibackgroundcopyjob2)
</dt> <dt>

[Exemplo: classes comuns](common-classes.md)
</dt> </dl>

 

 