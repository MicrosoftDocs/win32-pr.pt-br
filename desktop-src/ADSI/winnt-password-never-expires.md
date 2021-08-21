---
title: A senha nunca expira (provedor WinNT)
description: Para habilitar essa opção usando o provedor ADSI do WinNT, defina o sinalizador ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD (0x10000) no atributo UserFlags. Observação Para Windows 2000 e posteriores, use o provedor ADSI LDAP para operações de gerenciamento de usuário, conforme mostrado.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- A senha nunca expira (provedor WinNT)
- A senha nunca expira ADSI, provedor WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, Senha Nunca Expira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b47cdd7dc181c2875e8de06b66233d727c5b132963921b163b02fc09cbdc051d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082160"
---
# <a name="password-never-expires-winnt-provider"></a>A senha nunca expira (provedor WinNT)

Para habilitar essa opção usando o provedor ADSI do WinNT, defina o sinalizador **ADS \_ UF \_ DONT EXPIRE \_ \_ PASSWD** (0x10000) no atributo **UserFlags.**

> [!Note]  
> Por Windows 2000 e posteriores, use o provedor ADSI LDAP para operações de gerenciamento de usuário, conforme mostrado. Para obter mais informações, consulte [Password Never Expires (Provedor LDAP).](password-never-expires.md)

 

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como definir a opção de senha nunca expira usando Visual Basic ADSI.


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir mostra como definir a opção de senha nunca expira usando C++ com ADSI.


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




