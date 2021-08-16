---
title: O método Get
description: O método IADs Get é usado para recuperar atributos nomeados individuais de um objeto de diretório.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Obter a ADSI, usando IADs Get
- ADSI ADSI, usando, usando o método IADs Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386c3fe6e50a9f7357ec161b1e6bd8731cf8d0a74eed4b4a765adc3315c1045d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838626"
---
# <a name="the-get-method"></a>O método Get

O método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) é usado para recuperar atributos nomeados individuais de um objeto de diretório.

O exemplo de código a seguir usa o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar um atributo nomeado de um objeto.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Em linguagens de automação, os atributos nomeados também podem ser acessados diretamente usando a notação de ponto. Por exemplo, **objeto. Get ("distinguishedName")** é idêntico a **Object. DistinguishedName**.

O exemplo de código a seguir é idêntico ao exemplo anterior, exceto pelo fato de que o atributo **distinguishedName** é acessado usando a notação de ponto.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Se um valor não for definido no objeto, o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) retornará o erro "propriedade não encontrada no cache".

 

 




