---
title: Associação com GetObject e ADsGetObject
description: As funções GetObject e ADsGetObject são usadas para associar a objetos de serviço de diretório sem autenticação.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associação com GetObject e ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fe3f64368f6bbecf390d07f5258c11b6752badbf701e1f248439ca81428749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082750"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Associação com GetObject e ADsGetObject

As funções **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) são usadas para associar a objetos de serviço de diretório sem autenticação. O aplicativo não precisa fornecer credenciais ao acessar dados do serviço de diretório. A ADSI usa o contexto de segurança do thread de chamada. No entanto, se a autenticação segura falhar, a ADSI tentará executar uma associação simples com um nome de usuário nulo e uma senha nula. Se o vínculo simples for bem sucedido, o contexto do usuário para a associação será convidado. Uma associação simples usa autenticação de texto sem formatação. Como nenhum nome de usuário ou senha é transmitido pela rede, isso não é um problema de segurança.

A função **GetObject** é usada para associar a objetos de serviço de diretório em idiomas que dão suporte à automação, como Visual Basic. A função **GetObject** requer uma cadeia de caracteres do moniker. Na ADSI, a cadeia de caracteres de associação é a cadeia de caracteres do moniker.

Em linguagens que não dão suporte diretamente à automação, como C ou C++, a ADSI fornece a função [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para associar a objetos de serviço de diretório. Como alternativa, as funções [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) e [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) podem ser usadas para obter o mesmo resultado que **GetObject**.

Para um serviço em execução na conta LocalSystem, o contexto de segurança usado pelo **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depende do computador no qual o serviço está em execução. Se o serviço estiver sendo executado como LocalSystem em um controlador de domínio, o serviço terá acesso total no nível do sistema para Active Directory. Se o serviço não estiver em execução em um controlador de domínio, o serviço terá os direitos de acesso e os privilégios concedidos à conta do computador no qual o serviço está em execução; Isso é significativamente menos potente do que o acesso no nível do sistema.

## <a name="examples"></a>Exemplos

o exemplo de código a seguir Visual Basic mostra como usar a função **getobject** para associar a um objeto.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



O exemplo de código C++ a seguir mostra como usar a função [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) para associar a um objeto.


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



 

 