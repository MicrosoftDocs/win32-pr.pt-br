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
# <a name="using-a-session-moniker"></a>Usando um moniker de sessão

A ativação de sessão para sessão permite que um processo de cliente ative um processo de servidor local em uma sessão especificada. Você pode fazer isso por sessão usando um moniker de sessão fornecido pelo sistema. Para obter mais informações sobre como criar um moniker de sessão, consulte [ativação de sessão para sessão com um moniker de sessão](session-to-session-activation-with-a-session-moniker.md).

O exemplo a seguir mostra como ativar um processo de servidor local com a ID de classe "10000013-0000-0000-0000-000000000001" na sessão com a ID de sessão 3.

Primeiro, o exemplo chama a função [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca com. Em seguida, o exemplo chama [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) para recuperar um ponteiro para uma implementação da interface [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) . Esse objeto armazena informações sobre as operações de associação de moniker; o ponteiro é necessário para chamar métodos da interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) . Em seguida, o exemplo chama a função [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) para criar o moniker da sessão composta e, em seguida, o método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para ativar a conexão entre o cliente e o processo do servidor, usando o moniker da sessão recém-criada. Neste ponto, você pode usar o ponteiro de interface para executar as operações desejadas no objeto. Por fim, o exemplo libera o contexto de ligação e chama a função [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


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



Como "{ID da classe da classe moniker}" também é uma maneira de nomear um moniker de classe, você pode usar a cadeia de caracteres a seguir para nomear o moniker composto (o moniker da sessão composto com o moniker da classe) em vez da maneira mostrada no exemplo anterior.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Se o mesmo usuário estiver conectado a cada sessão durante uma ativação entre sessões, você poderá ativar com êxito qualquer processo de servidor configurado para ser executado no modo de ativação interativa do usuário interativo. Se usuários diferentes fizerem logon em cada sessão, o servidor deverá chamar a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir os direitos de usuário apropriados antes que uma ativação e conexão com êxito ocorra entre o cliente e o servidor. Uma maneira de fazer isso seria para o servidor implementar uma interface [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizada e passar a implementação para **CoInitializeSecurity**. Em qualquer caso, o usuário do cliente deve ter as permissões de [**inicialização**](../com/launchpermission.md) e [**acesso**](../com/accesspermission.md) apropriadas que são especificadas pelo aplicativo em execução no servidor. Para obter mais informações, consulte [segurança em com](../com/security-in-com.md).

 

Para obter mais informações sobre monikers e modos de ativação fornecidos pelo sistema, consulte [monikers](../com/monikers.md), a interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) e a [chave AppID](/windows/desktop/com/appid-key) na documentação com do SDK (Software Development Kit) da plataforma.

 

 