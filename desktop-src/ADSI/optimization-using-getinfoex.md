---
title: Otimização usando GetInfoEx
description: Usado para carregar valores de atributo específicos no cache local do serviço de diretório subjacente.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Otimização usando o ADSI getInfoEx
- GetInfoEx ADSI , otimização usando IADs GetInfoEx
- ADSI ADSI , usando, otimização usando o método GetInfoEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4daf75fa3961a57996d6ae51d237d27835213a25a20c52452b5896c6224964a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838990"
---
# <a name="optimization-using-getinfoex"></a>Otimização usando GetInfoEx

O [**método IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) é usado para carregar valores de atributo específicos no cache local do serviço de diretório subjacente. Esse método carrega apenas os valores de atributo especificados no cache local. O [**método IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é usado para carregar todos os valores de atributo no cache local.

O [**método IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtém valores atuais específicos para as propriedades de um objeto do Active Directory do armazenamento de diretórios subjacente, atualize os valores armazenados em cache.

No entanto, se um valor já existir no cache de propriedades, chamar o método [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) sem chamar [**PRIMEIRO IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para esse atributo recuperará o valor armazenado em cache em vez do valor mais atual do diretório subjacente. Isso pode fazer com que os valores de atributo atualizados sejam substituídos se o cache local tiver sido modificado, mas os valores não foram confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) O método sugerido para evitar problemas de cache é sempre fazer commit de alterações de valor de atributo chamando **IADs.SetInfo** antes de chamar [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a>Recuperando atributos construídos do Active Directory

No Active Directory, a maioria dos atributos construídos é recuperada e armazenada em cache quando o método [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é chamado ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) executa uma chamada **IADs.GetInfo** implícita se o cache estiver vazio). Alguns atributos construídos, no entanto, não são recuperados e armazenados em cache automaticamente e, portanto, exigem que o método [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) seja chamado explicitamente para recuperá-los. Por exemplo, no Active Directory, o atributo [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) não é recuperado quando o método **IADs.GetInfo** é chamado e **IADs.Get** retornará **a PROPRIEDADE E ADS NÃO \_ \_ \_ \_ ENCONTRADA.** O **método IADs.GetInfoEx** deve ser chamado para recuperar o **atributo canonicalName.** Esses mesmos atributos construídos também não serão recuperados usando a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) para enumerar os atributos.

Para obter mais informações e um exemplo de código que mostra como recuperar todos os valores de atributo, consulte Código de [exemplo para ler um atributo construído.](example-code-for-reading-a-constructed-attribute.md)

 

 