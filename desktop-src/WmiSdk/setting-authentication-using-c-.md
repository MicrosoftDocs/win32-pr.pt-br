---
description: 'Uma das principais tarefas de IWbemLocator:: ConnectServer para WMI é retornar um ponteiro para um proxy de IWbemServices.'
ms.assetid: bbff43b7-79f8-4c7b-a772-d3d962cf3859
ms.tgt_platform: multiple
title: Configurando a autenticação usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293d317ac521d36bf7ff616a0340f86c364ce885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814140"
---
# <a name="setting-authentication-using-c"></a>Configurando a autenticação usando C++

Uma das principais tarefas de [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para WMI é retornar um ponteiro para um proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Por meio do proxy de **IWbemServices** , você pode acessar os recursos da infraestrutura do WMI. No entanto, o ponteiro para o proxy de **IWbemServices** tem a identidade do processo do aplicativo cliente e não a identidade do processo de **IWbemServices** . Portanto, se você tentar acessar **IWbemServices** com o ponteiro, poderá receber um código com acesso negado, como **E \_ ACCESSDENIED**. Para evitar o erro de acesso negado, você deve definir a identidade do novo ponteiro com uma chamada para a interface [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .

Um provedor pode definir a segurança em um namespace para que nenhum dado seja retornado, a menos que você use a privacidade de pacote (**PktPrivacy**) em sua conexão com esse namespace. Isso garante que os dados sejam criptografados enquanto atravessam a rede. Se você tentar definir um nível de autenticação inferior, receberá uma mensagem de acesso negado. Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).

Para obter mais informações sobre como configurar a autenticação em scripts, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="setting-security-on-a-remote-iunknown-interface"></a>Definindo a segurança em uma interface IUnknown remota

Em algumas situações, é necessário ter mais acesso a um servidor do que apenas um ponteiro para um proxy. Às vezes, talvez seja necessário obter uma conexão segura com a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do proxy. Usando **IUnknown**, você pode consultar o sistema remoto para obter interfaces e outras técnicas necessárias.

Quando um proxy está localizado em um computador remoto, o servidor delega todas as chamadas para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do proxy para a interface **IUnknown** . Por exemplo, se você chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um proxy e a interface solicitada não for parte do proxy, o proxy enviará a chamada para o servidor remoto. Por sua vez, o servidor remoto verifica o suporte de interface apropriado. Se o servidor oferecer suporte à interface, o COM realizará marshaling de um novo proxy para o cliente para que o aplicativo possa usar a nova interface.

Ocorrerão problemas se o cliente não tiver permissões de acesso ao servidor remoto, mas estiver usando as credenciais de um usuário que o faz. Nessa situação, qualquer tentativa de acessar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no servidor remoto falhará. A versão final do proxy também falha, porque o usuário atual não tem acesso ao servidor remoto. Um sintoma disso é um atraso de um ou dois segundos antes que o aplicativo cliente falhe na versão final do proxy. A falha ocorre porque o COM tentou acessar o servidor remoto usando as configurações de segurança padrão do usuário atual, que não incluem as credenciais modificadas que permitiam acesso ao servidor em primeiro lugar. Para obter mais informações, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

Para evitar a falha na conexão, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir explicitamente a autenticação de segurança no ponteiro retornado de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown). Usando o **CoSetProxyBlanket**, você pode garantir que o servidor remoto receba a identidade de autenticação correta.

O exemplo de código a seguir mostra como usar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para acessar uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.


```C++
SEC_WINNT_AUTH_IDENTITY_W* pAuthIdentity = 
   new SEC_WINNT_AUTH_IDENTITY_W;
ZeroMemory(pAuthIdentity, sizeof(SEC_WINNT_AUTH_IDENTITY_W));

pAuthIdentity->User = new WCHAR[32];
StringCbCopyW(pAuthIdentity->User,sizeof(L"MyUser"),L"MyUser");
pAuthIdentity->UserLength = wcslen(pAuthIdentity->User);

pAuthIdentity->Domain = new WCHAR[32];
StringCbCopyW(pAuthIdentity->Domain,sizeof(L"MyDomain"),L"MyDomain");
pAuthIdentity->DomainLength = wcslen(pAuthIdentity->Domain);

pAuthIdentity->Password = new WCHAR[32];
pAuthIdentity->Password[0] = NULL;
pAuthIdentity->PasswordLength = wcslen( pAuthIdentity->Password);

pAuthIdentity->Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

IWbemServices* pWbemServices = 0;

// Set proxy security
hr = CoSetProxyBlanket(pWbemServices, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pWbemServices->Release();
   return 1;
}

// Set IUnknown security
IUnknown*    pUnk = NULL;
pWbemServices->QueryInterface(IID_IUnknown, (void**) &pUnk);

hr = CoSetProxyBlanket(pUnk, 
                       RPC_C_AUTHN_DEFAULT, 
                       RPC_C_AUTHZ_NONE, 
                       COLE_DEFAULT_PRINCIPAL, 
                       RPC_C_AUTHN_LEVEL_DEFAULT, 
                       RPC_C_IMP_LEVEL_IMPERSONATE, 
                       pAuthIdentity, 
                       EOAC_NONE 
);
if (FAILED(hr))
{
   cout << "Count not set proxy blanket. Error code = 0x"
        << hex << hr << endl;
   pUnk->Release();
   pWbemServices->Release();
   delete [] pAuthIdentity->User;
   delete [] pAuthIdentity->Domain;
   delete [] pAuthIdentity->Password;
   delete pAuthIdentity;   
   return 1;
}

// cleanup IUnknown
pUnk->Release();

//
// Perform a bunch of operations
//

// Cleanup
pWbemServices->Release();

delete [] pAuthIdentity->User;
delete [] pAuthIdentity->Domain;
delete [] pAuthIdentity->Password;

delete pAuthIdentity;
```



> [!Note]  
> Quando você define a segurança na interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de um proxy, com cria uma cópia do proxy que não pode ser liberada até que você chame [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a autenticação no WMI](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
