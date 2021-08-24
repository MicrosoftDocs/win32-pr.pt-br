---
title: Usando um Moniker de sessão
description: A ativação de sessão para sessão permite que um processo de cliente ative um processo de servidor local em uma sessão especificada.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fc5c65c3e2efd3e566a3fdde6982fefe5bb14fbefd98ca8abd335955b7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868846"
---
# <a name="using-a-session-moniker"></a>Usando um Moniker de sessão

A ativação de sessão para sessão permite que um processo de cliente ative um processo de servidor local em uma sessão especificada. Você pode fazer isso por sessão usando um moniker de sessão fornecido pelo sistema. Para obter mais informações sobre como criar um moniker de sessão, consulte Ativação de sessão para [sessão com um Moniker de sessão](session-to-session-activation-with-a-session-moniker.md).

O exemplo a seguir mostra como ativar um processo de servidor local com a ID de classe "10000013-0000-0000-0000-0000000001" na sessão com a ID da sessão 3.

Primeiro, o exemplo chama a [**função CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar a biblioteca COM. Em seguida, o exemplo [**chama CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) para recuperar um ponteiro para uma implementação da interface [**IBindCtx.**](/windows/win32/api/objidl/nn-objidl-ibindctx) Esse objeto armazena informações sobre operações de associação de moniker; o ponteiro é necessário para chamar métodos da interface [**IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker) Em seguida, o exemplo chama a [função MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) para criar o moniker de sessão composta e, em seguida, o método [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para ativar a conexão entre o cliente e o processo do servidor, usando o moniker de sessão recém-criado. Neste ponto, você pode usar o ponteiro de interface para executar as operações desejadas no objeto . Por fim, o exemplo libera o contexto de ligação e chama a [**função CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


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



Como "{id de classe da classe moniker}" também é uma maneira de nomear um moniker de classe, você pode usar a cadeia de caracteres a seguir para nomear o moniker composto (o moniker de sessão composto com o moniker de classe) em vez do modo de exibição no exemplo anterior.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Se o mesmo usuário estiver conectado a cada sessão durante uma ativação entre sessões, você poderá ativar com êxito qualquer processo de servidor configurado para ser executado no modo de ativação do Usuário Interativo RunAs. Se usuários diferentes estão conectados a cada sessão, o servidor deve chamar a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir os direitos de usuário apropriados antes que uma ativação e conexão bem-sucedidas possam ocorrer entre o cliente e o servidor. Uma maneira de fazer isso seria para o servidor implementar uma interface [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizada e passar a implementação para **CoInitializeSecurity**. Em qualquer caso, o usuário [](../com/launchpermission.md) cliente deve ter as permissões de início e [**acesso apropriadas especificadas**](../com/accesspermission.md) pelo aplicativo em execução no servidor. Para obter mais informações, [consulte Segurança em COM](../com/security-in-com.md).

 

Para obter mais informações sobre monikers e monikers fornecidos pelo sistema e modos de ativação, consulte [Monikers](../com/monikers.md), a interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) e [AppId Key](/windows/desktop/com/appid-key) na documentação com no SDK (Kit de Desenvolvimento de Software de Plataforma).

 

 