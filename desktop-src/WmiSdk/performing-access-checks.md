---
description: Uma verificação de acesso determina se um descritor de segurança concede um conjunto especificado de direitos de acesso ao cliente ou thread identificado por um token de acesso.
ms.assetid: d0259bb1-fd74-4440-ac2a-d6aa84a48d9b
ms.tgt_platform: multiple
title: Executando verificações de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9af65605b6e96a5ad8b820de876d553f8d19202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761089"
---
# <a name="performing-access-checks"></a><span data-ttu-id="17fdd-103">Executando verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="17fdd-103">Performing Access Checks</span></span>

<span data-ttu-id="17fdd-104">Uma verificação de acesso determina se um descritor de segurança concede um conjunto especificado de direitos de acesso ao cliente ou thread identificado por um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="17fdd-104">An access check determines whether a security descriptor grants a specified set of access rights to the client or thread identified by an access token.</span></span> <span data-ttu-id="17fdd-105">Você pode chamar a função de segurança [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) de aplicativos cliente WMI ou provedores escritos em C++ ou C#.</span><span class="sxs-lookup"><span data-stu-id="17fdd-105">You can call the security function [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) from WMI client applications or providers written in C++ or C#.</span></span> <span data-ttu-id="17fdd-106">Scripts e Visual Basic aplicativos não podem executar verificações de acesso usando o método descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="17fdd-106">Scripts and Visual Basic applications cannot perform access checks using the method described here.</span></span>

<span data-ttu-id="17fdd-107">Os aplicativos cliente devem fazer uma verificação de acesso para determinar a identidade do retorno de chamada ao retornar resultados para o coletor fornecido pela chamada assíncrona do cliente.</span><span class="sxs-lookup"><span data-stu-id="17fdd-107">Client applications should do an access check to determine the identity of the callback when returning results to the sink provided by the client asynchronous call.</span></span>

<span data-ttu-id="17fdd-108">Quando os provedores não podem representar o aplicativo cliente ou o script que está solicitando dados, eles devem executar verificações de acesso para as seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="17fdd-108">When providers cannot impersonate the client application or script that is requesting data, they should perform access checks for the following situations:</span></span>

-   <span data-ttu-id="17fdd-109">Ao acessar recursos que não são protegidos por listas de controle de acesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="17fdd-109">When accessing resources that are not protected by access control lists (ACL).</span></span>
-   <span data-ttu-id="17fdd-110">Quando o cliente se conectou no **nível do RPC \_ C, \_ \_ identifique** o nível de representação.</span><span class="sxs-lookup"><span data-stu-id="17fdd-110">When the client has connected at the **RPC\_C\_LEVEL\_IDENTIFY** impersonation level.</span></span>

> [!Note]  
> <span data-ttu-id="17fdd-111">Os aplicativos C++ e C# podem controlar se as verificações de acesso são executadas por um processo separado.</span><span class="sxs-lookup"><span data-stu-id="17fdd-111">C++ and C# applications can control whether access checks are performed by a separate process.</span></span> <span data-ttu-id="17fdd-112">Scripts e Visual Basic aplicativos podem ler ou alterar uma chave do registro para garantir que o WMI execute verificações de acesso.</span><span class="sxs-lookup"><span data-stu-id="17fdd-112">Scripts and Visual Basic applications can read or change a registry key to ensure that WMI performs access checks.</span></span> <span data-ttu-id="17fdd-113">Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="17fdd-113">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

 

<span data-ttu-id="17fdd-114">O exemplo de código neste tópico requer as referências a seguir e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="17fdd-114">The code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#include <lmcons.h>
#define _WIN32_DCOM
#define SECURITY_WIN32
#include <wbemidl.h>
#include <security.h>
#include <safestr.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "Secur32.lib")
```



<span data-ttu-id="17fdd-115">O exemplo de código a seguir mostra como verificar se o token de segurança de um thread de aplicativo cliente contém permissões apropriadas para um descritor de segurança especificado.</span><span class="sxs-lookup"><span data-stu-id="17fdd-115">The following code example shows how to check that the security token of a client application thread contains permissions appropriate to a specified security descriptor.</span></span> <span data-ttu-id="17fdd-116">A função usa a cadeia de caracteres "domínio \\ User" e retorna o Sid.</span><span class="sxs-lookup"><span data-stu-id="17fdd-116">The function takes the string "domain\\user" and returns the SID.</span></span> <span data-ttu-id="17fdd-117">Se a chamada falhar, a função retornará **NULL**, caso contrário, o chamador deverá liberar o ponteiro retornado.</span><span class="sxs-lookup"><span data-stu-id="17fdd-117">If the call fails, the function returns **NULL**, otherwise the caller must free the returned pointer.</span></span>


```C++
BYTE * GetSid(LPWSTR pwcUserName)
{
    DWORD dwSidSize = 0, dwDomainSize = 0;
    SID_NAME_USE use;

    // first call is to get the size
    BOOL bRet = LookupAccountNameW(

      NULL,            // system name
      pwcUserName,     // account name
      NULL,            // security identifier
      &dwSidSize,      // size of security identifier
      NULL,            // domain name
      &dwDomainSize,   // size of domain name
      &use             // SID-type indicator
      );    

    if(bRet == FALSE && ERROR_INSUFFICIENT_BUFFER 
        != GetLastError())\
        return NULL;

    BYTE * buff = new BYTE[dwSidSize];

    if(buff == NULL)
        return NULL;

    WCHAR * pwcDomain = new WCHAR[dwDomainSize];

    if(pwcDomain == NULL)

    {
        delete [] buff;
        return FALSE;
    }

    // Call to LookupAccountNameW actually gets the SID
    bRet = LookupAccountNameW(

      NULL,           // system name
      pwcUserName,    // account name
      buff,           // security identifier
      &dwSidSize,     // size of security identifier
      pwcDomain,      // domain name
      &dwDomainSize,  // size of domain name
      &use            // SID-type indicator
      );    

    delete [] pwcDomain;

    if(bRet == FALSE)
    {
        delete [] buff;
        return NULL;
    }

    return buff;
}

// This returns true if the caller is coming 
//   from the expected computer in the expected domain.

BOOL IsAllowed(LPWSTR pwsExpectedDomain, 
   LPWSTR pwsExpectedMachine)
{

    WCHAR wCallerName[UNLEN + 1];
    DWORD nSize = UNLEN + 1;

// Impersonate the caller and get its name

    HRESULT hr = CoImpersonateClient();
    if(FAILED(hr))

        return FALSE;

    BOOL bRet = GetUserNameExW(NameSamCompatible, 
       wCallerName, &nSize);

    CoRevertToSelf();

    if(bRet == FALSE)

        return FALSE;


    // take the expected domain and lan manager 
    //   style name and create a SID.  In actual
    // production code, it would be more efficient 
    //   to do this only when necessary

    WCHAR wExpectedName[UNLEN + 1];

    HRESULT hrCopyCat;
    hrCopyCat = StringCchCopy(wExpectedName,
        sizeof(pwsExpectedDomain)*sizeof(WCHAR)+1, 
        pwsExpectedDomain);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = 
        StringCchCat(wExpectedName,sizeof(wExpectedName)
        + 2*sizeof(WCHAR)+1, L"\\");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(pwsExpectedMachine)*sizeof(WCHAR)+1, 
        pwsExpectedMachine);
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
    hrCopyCat = StringCchCat(wExpectedName,sizeof(wExpectedName)
        + sizeof(WCHAR)+1, L"$");
    if (FAILED(hrCopyCat))
    {
        return FALSE;
    }
  

    // convert the two names to SIDs and compare.  
    // Note that SIDs are used since 
    //   the format of the names might vary.  

    BYTE * pCaller = GetSid(wCallerName);

    if(pCaller == NULL)

        return FALSE;

    BYTE * pExpected = GetSid(wExpectedName);

    if(pExpected == NULL)
    {
        delete [] pCaller;

        return FALSE;
    }

    bRet = EqualSid((PSID)pCaller, (PSID)pExpected);

    delete [] pCaller;
    delete [] pExpected;

    return bRet;
}
```



## <a name="related-topics"></a><span data-ttu-id="17fdd-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17fdd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17fdd-119">Escolhendo o registro correto</span><span class="sxs-lookup"><span data-stu-id="17fdd-119">Choosing Correct Registration</span></span>](choosing-correct-registration.md)
</dt> <dt>

[<span data-ttu-id="17fdd-120">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="17fdd-120">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="17fdd-121">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="17fdd-121">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> <dt>

[<span data-ttu-id="17fdd-122">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="17fdd-122">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
