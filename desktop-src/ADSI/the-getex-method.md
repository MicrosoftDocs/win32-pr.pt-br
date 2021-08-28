---
title: O método GetEx
description: Alguns atributos podem armazenar um ou mais valores.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI , usando IADs GetEx
- ADSI ADSI , usando, usando o método GetEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e656bd6a48830feb725e927f08be1d573e7b0232cf02c16ee87bd7d6a5b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690145"
---
# <a name="the-getex-method"></a>O método GetEx

Alguns atributos podem armazenar um ou mais valores. Por exemplo, o **outro atributoTelephone** de um objeto de usuário no Active Directory é uma propriedade que pode ter zero, um ou muitos valores. Atributos que têm vários valores são conhecidos como "atributos com vários valores". Se o [**método IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) for usado para recuperar um atributo com vários valores, os resultados deverão ser processados de maneira diferente de se o atributo tiver um único valor. No entanto, os resultados fornecidos pelo método [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) são processados da mesma maneira, independentemente de o atributo ter um ou vários valores. Em ambos os casos, o **método IADs::GetEx** retorna os valores em uma matriz.

O [**método IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera propriedades do cache de propriedades. Se a propriedade especificada não for encontrada no cache, **IADs::GetEx** executará uma chamada [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implícita.

O [**método IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retorna uma matriz variante de variantes, independentemente do número de valores retornados do servidor. Isso é verdadeiro mesmo que o atributo contenha apenas um valor.


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



O [**método IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) também pode ser usado para atributos de valor único. Os resultados de um atributo de valor único são processados da mesma forma que os resultados de um atributo com vários valores.


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Se nenhum valor for definido para o atributo, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retornará o erro "Propriedade não encontrada no cache".

 

 




