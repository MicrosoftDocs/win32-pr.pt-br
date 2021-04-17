---
title: Expiração da conta (provedor de WinNT)
description: Ao usar o provedor WinNT, a data de expiração da conta pode ser definida usando a propriedade IADsUser. AccountExpirationDate.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- ADSI de expiração de conta, provedor de WinNT
- ADSI do provedor WinNT, exemplos de gerenciamento de usuário, expiração da conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105811230"
---
# <a name="account-expiration-winnt-provider"></a>Expiração da conta (provedor de WinNT)

Ao usar o provedor WinNT, a data de expiração da conta pode ser definida usando a propriedade [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) .

Para definir a data de expiração da conta, defina a propriedade [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) para o valor de data desejado. Para definir a data de expiração da conta para nunca expirar, defina essa propriedade como "1º de janeiro de 1970".

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir mostra como definir a data de expiração da conta usando Visual Basic com ADSI.


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

O exemplo de código a seguir mostra como definir a data de expiração da conta usando C++ com ADSI.


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



 

 




