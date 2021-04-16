---
title: A senha nunca expira (provedor WinNT)
description: 'Para habilitar essa opção usando o provedor ADSI do WinNT, defina o sinalizador da UF do ADS que não \_ \_ \_ expirar de \_ senha (0x10000) no atributo UserFlags. Observação: para o Windows 2000 e posterior, use o provedor ADSI LDAP para operações de gerenciamento de usuário, conforme mostrado.'
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- A senha nunca expira (provedor WinNT)
- A senha nunca expira em ADSI, provedor WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, senha nunca expira
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105754048"
---
# <a name="password-never-expires-winnt-provider"></a>A senha nunca expira (provedor WinNT)

Para habilitar essa opção usando o provedor ADSI do WinNT, defina o sinalizador da UF do ADS que não **\_ \_ \_ expirar de \_ senha** (0x10000) no atributo **UserFlags** .

> [!Note]  
> Para o Windows 2000 e posterior, use o provedor ADSI LDAP para operações de gerenciamento de usuário, conforme mostrado. Para obter mais informações, consulte a [senha nunca expira (provedor LDAP)](password-never-expires.md).

 

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como definir a opção a senha nunca expira usando Visual Basic com ADSI.


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

O exemplo de código a seguir mostra como definir a opção a senha nunca expira usando C++ com ADSI.


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



 

 




