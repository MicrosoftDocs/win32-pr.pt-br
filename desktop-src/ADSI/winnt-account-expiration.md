---
title: Expiração da conta (Provedor WinNT)
description: Ao usar o provedor WinNT, a data de validade da conta pode ser definida usando a propriedade IADsUser.AccountExpirationDate.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- ADSI de expiração da conta, provedor WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuários, Expiração da Conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd23973a4de31fed629428be9f4df1b6cade34e77f78680a5f87c9d55c42234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838406"
---
# <a name="account-expiration-winnt-provider"></a>Expiração da conta (Provedor WinNT)

Ao usar o provedor WinNT, a data de validade da conta pode ser definida usando a [**propriedade IADsUser.AccountExpirationDate.**](iadsuser-property-methods.md)

Para definir a data de expiração da conta, de definido a [**propriedade IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) como o valor de data desejado. Para definir a data de expiração da conta para nunca expirar, de definir essa propriedade como "1º de janeiro de 1970".

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como definir a data de validade da conta usando Visual Basic adsi.


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir mostra como definir a data de validade da conta usando C++ com ADSI.


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




