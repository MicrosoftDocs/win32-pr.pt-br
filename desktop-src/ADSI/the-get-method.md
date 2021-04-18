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
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771760"
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

 

 




