---
title: Associação com GetObject e ADsGetObject
description: As funções GetObject e ADsGetObject são usadas para associar a objetos de serviço de diretório sem autenticação.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associação com GetObject e ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917665"
---
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="0157b-104">Associação com GetObject e ADsGetObject</span><span class="sxs-lookup"><span data-stu-id="0157b-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="0157b-105">As funções **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) são usadas para associar a objetos de serviço de diretório sem autenticação.</span><span class="sxs-lookup"><span data-stu-id="0157b-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="0157b-106">O aplicativo não precisa fornecer credenciais ao acessar dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="0157b-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="0157b-107">A ADSI usa o contexto de segurança do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="0157b-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="0157b-108">No entanto, se a autenticação segura falhar, a ADSI tentará executar uma associação simples com um nome de usuário nulo e uma senha nula.</span><span class="sxs-lookup"><span data-stu-id="0157b-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="0157b-109">Se o vínculo simples for bem sucedido, o contexto do usuário para a associação será convidado.</span><span class="sxs-lookup"><span data-stu-id="0157b-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="0157b-110">Uma associação simples usa autenticação de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="0157b-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="0157b-111">Como nenhum nome de usuário ou senha é transmitido pela rede, isso não é um problema de segurança.</span><span class="sxs-lookup"><span data-stu-id="0157b-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="0157b-112">A função **GetObject** é usada para associar a objetos de serviço de diretório em idiomas que dão suporte à automação, como Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0157b-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="0157b-113">A função **GetObject** requer uma cadeia de caracteres do moniker.</span><span class="sxs-lookup"><span data-stu-id="0157b-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="0157b-114">Na ADSI, a cadeia de caracteres de associação é a cadeia de caracteres do moniker.</span><span class="sxs-lookup"><span data-stu-id="0157b-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="0157b-115">Em linguagens que não dão suporte diretamente à automação, como C ou C++, a ADSI fornece a função [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para associar a objetos de serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="0157b-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="0157b-116">Como alternativa, as funções [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) e [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) podem ser usadas para obter o mesmo resultado que **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="0157b-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="0157b-117">Para um serviço em execução na conta LocalSystem, o contexto de segurança usado pelo **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depende do computador no qual o serviço está em execução.</span><span class="sxs-lookup"><span data-stu-id="0157b-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="0157b-118">Se o serviço estiver sendo executado como LocalSystem em um controlador de domínio, o serviço terá acesso total no nível do sistema para Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0157b-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="0157b-119">Se o serviço não estiver em execução em um controlador de domínio, o serviço terá os direitos de acesso e os privilégios concedidos à conta do computador no qual o serviço está em execução; Isso é significativamente menos potente do que o acesso no nível do sistema.</span><span class="sxs-lookup"><span data-stu-id="0157b-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="0157b-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0157b-120">Examples</span></span>

<span data-ttu-id="0157b-121">O exemplo de código a seguir Visual Basic mostra como usar a função **GetObject** para associar a um objeto.</span><span class="sxs-lookup"><span data-stu-id="0157b-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="0157b-122">O exemplo de código C++ a seguir mostra como usar a função [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para associar a um objeto.</span><span class="sxs-lookup"><span data-stu-id="0157b-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 