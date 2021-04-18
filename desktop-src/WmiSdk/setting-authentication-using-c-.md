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
# <a name="setting-authentication-using-c"></a><span data-ttu-id="0f7ca-103">Configurando a autenticação usando C++</span><span class="sxs-lookup"><span data-stu-id="0f7ca-103">Setting Authentication Using C++</span></span>

<span data-ttu-id="0f7ca-104">Uma das principais tarefas de [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) para WMI é retornar um ponteiro para um proxy de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="0f7ca-104">One of the main tasks of [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) for WMI is returning a pointer to an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="0f7ca-105">Por meio do proxy de **IWbemServices** , você pode acessar os recursos da infraestrutura do WMI.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-105">Through the **IWbemServices** proxy, you can access the capabilities of the WMI infrastructure.</span></span> <span data-ttu-id="0f7ca-106">No entanto, o ponteiro para o proxy de **IWbemServices** tem a identidade do processo do aplicativo cliente e não a identidade do processo de **IWbemServices** .</span><span class="sxs-lookup"><span data-stu-id="0f7ca-106">However, the pointer to the **IWbemServices** proxy has the identity of the client application process and not the identity of the **IWbemServices** process.</span></span> <span data-ttu-id="0f7ca-107">Portanto, se você tentar acessar **IWbemServices** com o ponteiro, poderá receber um código com acesso negado, como **E \_ ACCESSDENIED**.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-107">Therefore, if you attempt to access **IWbemServices** with the pointer, you can receive an access-denied code such as **E\_ACCESSDENIED**.</span></span> <span data-ttu-id="0f7ca-108">Para evitar o erro de acesso negado, você deve definir a identidade do novo ponteiro com uma chamada para a interface [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="0f7ca-108">To avoid the access-denied error, you must set the identity of the new pointer with a call to the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) interface.</span></span>

<span data-ttu-id="0f7ca-109">Um provedor pode definir a segurança em um namespace para que nenhum dado seja retornado, a menos que você use a privacidade de pacote (**PktPrivacy**) em sua conexão com esse namespace.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-109">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (**PktPrivacy**) in your connection to that namespace.</span></span> <span data-ttu-id="0f7ca-110">Isso garante que os dados sejam criptografados enquanto atravessam a rede.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-110">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="0f7ca-111">Se você tentar definir um nível de autenticação inferior, receberá uma mensagem de acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-111">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="0f7ca-112">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="0f7ca-112">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="0f7ca-113">Para obter mais informações sobre como configurar a autenticação em scripts, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="0f7ca-113">For more information about setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

## <a name="setting-security-on-a-remote-iunknown-interface"></a><span data-ttu-id="0f7ca-114">Definindo a segurança em uma interface IUnknown remota</span><span class="sxs-lookup"><span data-stu-id="0f7ca-114">Setting Security on a Remote IUnknown Interface</span></span>

<span data-ttu-id="0f7ca-115">Em algumas situações, é necessário ter mais acesso a um servidor do que apenas um ponteiro para um proxy.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-115">In some situations, more access to a server than just a pointer to a proxy is required.</span></span> <span data-ttu-id="0f7ca-116">Às vezes, talvez seja necessário obter uma conexão segura com a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do proxy.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-116">At times, you may need to gain a secure connection to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy.</span></span> <span data-ttu-id="0f7ca-117">Usando **IUnknown**, você pode consultar o sistema remoto para obter interfaces e outras técnicas necessárias.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-117">Using **IUnknown**, you can query the remote system for interfaces and other necessary techniques.</span></span>

<span data-ttu-id="0f7ca-118">Quando um proxy está localizado em um computador remoto, o servidor delega todas as chamadas para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do proxy para a interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0f7ca-118">When a proxy is located on a remote computer, the server delegates all calls to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the proxy to the **IUnknown** interface.</span></span> <span data-ttu-id="0f7ca-119">Por exemplo, se você chamar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um proxy e a interface solicitada não for parte do proxy, o proxy enviará a chamada para o servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-119">For example, if you call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on a proxy and the requested interface was not part of the proxy, the proxy sends the call to the remote server.</span></span> <span data-ttu-id="0f7ca-120">Por sua vez, o servidor remoto verifica o suporte de interface apropriado.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-120">In turn, the remote server checks for the appropriate interface support.</span></span> <span data-ttu-id="0f7ca-121">Se o servidor oferecer suporte à interface, o COM realizará marshaling de um novo proxy para o cliente para que o aplicativo possa usar a nova interface.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-121">If the server does support the interface, COM marshals a new proxy back to the client so that the application can use the new interface.</span></span>

<span data-ttu-id="0f7ca-122">Ocorrerão problemas se o cliente não tiver permissões de acesso ao servidor remoto, mas estiver usando as credenciais de um usuário que o faz.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-122">Problems arise if the client does not have access permissions to the remote server, yet is using the credentials of a user that does.</span></span> <span data-ttu-id="0f7ca-123">Nessa situação, qualquer tentativa de acessar [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no servidor remoto falhará.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-123">In this situation, any attempt to access [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the remote server fails.</span></span> <span data-ttu-id="0f7ca-124">A versão final do proxy também falha, porque o usuário atual não tem acesso ao servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-124">The final release on the proxy fails as well, because the current user does not have access to the remote server.</span></span> <span data-ttu-id="0f7ca-125">Um sintoma disso é um atraso de um ou dois segundos antes que o aplicativo cliente falhe na versão final do proxy.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-125">A symptom of this is a one or two second lag before the client application fails the final proxy release.</span></span> <span data-ttu-id="0f7ca-126">A falha ocorre porque o COM tentou acessar o servidor remoto usando as configurações de segurança padrão do usuário atual, que não incluem as credenciais modificadas que permitiam acesso ao servidor em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-126">The failure occurs because COM attempted to access the remote server using the default security settings of the current user, which do not include the modified credentials that allowed access to the server in the first place.</span></span> <span data-ttu-id="0f7ca-127">Para obter mais informações, consulte [definindo a segurança em IWbemServices e outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="0f7ca-127">For more information, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="0f7ca-128">Para evitar a falha na conexão, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir explicitamente a autenticação de segurança no ponteiro retornado de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="0f7ca-128">To avoid the failed connection, use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to explicitly set the security authentication on the pointer returned from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="0f7ca-129">Usando o **CoSetProxyBlanket**, você pode garantir que o servidor remoto receba a identidade de autenticação correta.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-129">Using **CoSetProxyBlanket**, you can ensure that the remote server receives the correct authentication identity.</span></span>

<span data-ttu-id="0f7ca-130">O exemplo de código a seguir mostra como usar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para acessar uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) remota.</span><span class="sxs-lookup"><span data-stu-id="0f7ca-130">The following code example shows how to use [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to access a remote [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>


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
> <span data-ttu-id="0f7ca-131">Quando você define a segurança na interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) de um proxy, com cria uma cópia do proxy que não pode ser liberada até que você chame [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="0f7ca-131">When you set security on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of a proxy, COM creates a copy of the proxy that cannot be released until you call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0f7ca-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f7ca-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f7ca-133">Configurando a autenticação no WMI</span><span class="sxs-lookup"><span data-stu-id="0f7ca-133">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
</dt> </dl>

 

 
