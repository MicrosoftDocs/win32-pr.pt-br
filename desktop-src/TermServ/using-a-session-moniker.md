---
title: Usando um moniker de sessão
description: A ativação de sessão para sessão permite que um processo de cliente ative um processo de servidor local em uma sessão especificada.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294409"
---
# <a name="using-a-session-moniker"></a><span data-ttu-id="f9037-103">Usando um moniker de sessão</span><span class="sxs-lookup"><span data-stu-id="f9037-103">Using a Session Moniker</span></span>

<span data-ttu-id="f9037-104">A ativação de sessão para sessão permite que um processo de cliente ative um processo de servidor local em uma sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="f9037-104">Session-to-session activation allows a client process to activate a local server process on a specified session.</span></span> <span data-ttu-id="f9037-105">Você pode fazer isso por sessão usando um moniker de sessão fornecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f9037-105">You can do this on a per-session basis by using a system-supplied session moniker.</span></span> <span data-ttu-id="f9037-106">Para obter mais informações sobre como criar um moniker de sessão, consulte [ativação de sessão para sessão com um moniker de sessão](session-to-session-activation-with-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="f9037-106">For more information about creating a session moniker, see [Session-to-Session Activation with a Session Moniker](session-to-session-activation-with-a-session-moniker.md).</span></span>

<span data-ttu-id="f9037-107">O exemplo a seguir mostra como ativar um processo de servidor local com a ID de classe "10000013-0000-0000-0000-000000000001" na sessão com a ID de sessão 3.</span><span class="sxs-lookup"><span data-stu-id="f9037-107">The following example shows how to activate a local server process with the class ID "10000013-0000-0000-0000-000000000001" on the session with the session ID 3.</span></span>

<span data-ttu-id="f9037-108">Primeiro, o exemplo chama a função [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com.</span><span class="sxs-lookup"><span data-stu-id="f9037-108">First, the sample calls the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function to initialize the COM library.</span></span> <span data-ttu-id="f9037-109">Em seguida, o exemplo chama [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) para recuperar um ponteiro para uma implementação da interface [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) .</span><span class="sxs-lookup"><span data-stu-id="f9037-109">Then the sample calls [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) to retrieve a pointer to an implementation of the [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) interface.</span></span> <span data-ttu-id="f9037-110">Esse objeto armazena informações sobre as operações de associação de moniker; o ponteiro é necessário para chamar métodos da interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="f9037-110">This object stores information about moniker-binding operations; the pointer is required to call methods of the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface.</span></span> <span data-ttu-id="f9037-111">Em seguida, o exemplo chama a função [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) para criar o moniker da sessão composta e, em seguida, o método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para ativar a conexão entre o cliente e o processo do servidor, usando o moniker da sessão recém-criada.</span><span class="sxs-lookup"><span data-stu-id="f9037-111">Next the sample calls the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function to create the composite session moniker and then the [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) method to activate the connection between the client and the server process, using the newly created session moniker.</span></span> <span data-ttu-id="f9037-112">Neste ponto, você pode usar o ponteiro de interface para executar as operações desejadas no objeto.</span><span class="sxs-lookup"><span data-stu-id="f9037-112">At this point you can use the interface pointer to perform the desired operations on the object.</span></span> <span data-ttu-id="f9037-113">Por fim, o exemplo libera o contexto de ligação e chama a função [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="f9037-113">Finally, the sample releases the bind context and calls the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



<span data-ttu-id="f9037-114">Como "{ID da classe da classe moniker}" também é uma maneira de nomear um moniker de classe, você pode usar a cadeia de caracteres a seguir para nomear o moniker composto (o moniker da sessão composto com o moniker da classe) em vez da maneira mostrada no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="f9037-114">Because "{class id of the class moniker}" is also a way to name a class moniker, you can use the following string to name the composite moniker (the session moniker composed with the class moniker) instead of the way show in the preceding example.</span></span>

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> <span data-ttu-id="f9037-115">Se o mesmo usuário estiver conectado a cada sessão durante uma ativação entre sessões, você poderá ativar com êxito qualquer processo de servidor configurado para ser executado no modo de ativação interativa do usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="f9037-115">If the same user is logged on to each session during a cross-session activation, you can successfully activate any server process configured to run in the RunAs Interactive User activation mode.</span></span> <span data-ttu-id="f9037-116">Se usuários diferentes fizerem logon em cada sessão, o servidor deverá chamar a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir os direitos de usuário apropriados antes que uma ativação e conexão com êxito ocorra entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="f9037-116">If different users are logged on to each session, the server must call the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function to set the appropriate user rights before a successful activation and connection can occur between the client and the server.</span></span> <span data-ttu-id="f9037-117">Uma maneira de fazer isso seria para o servidor implementar uma interface [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizada e passar a implementação para **CoInitializeSecurity**.</span><span class="sxs-lookup"><span data-stu-id="f9037-117">One way to accomplish this would be for the server to implement a custom [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) interface and pass the implementation to **CoInitializeSecurity**.</span></span> <span data-ttu-id="f9037-118">Em qualquer caso, o usuário do cliente deve ter as permissões de [**inicialização**](../com/launchpermission.md) e [**acesso**](../com/accesspermission.md) apropriadas que são especificadas pelo aplicativo em execução no servidor.</span><span class="sxs-lookup"><span data-stu-id="f9037-118">In any case, the client user must have the appropriate [**Launch**](../com/launchpermission.md) and [**Access Permissions**](../com/accesspermission.md) that are specified by the application running on the server.</span></span> <span data-ttu-id="f9037-119">Para obter mais informações, consulte [segurança em com](../com/security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f9037-119">For more information see [Security in COM](../com/security-in-com.md).</span></span>

 

<span data-ttu-id="f9037-120">Para obter mais informações sobre monikers e modos de ativação fornecidos pelo sistema, consulte [monikers](../com/monikers.md), a interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) e a [chave AppID](/windows/desktop/com/appid-key) na documentação com do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="f9037-120">For more information about system-supplied monikers and monikers and activation modes, see [Monikers](../com/monikers.md), the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface, and [AppId Key](/windows/desktop/com/appid-key) in the COM documentation in the Platform Software Development Kit (SDK).</span></span>

 

 