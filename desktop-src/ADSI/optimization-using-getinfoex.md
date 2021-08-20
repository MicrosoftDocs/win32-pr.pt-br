---
title: Otimização usando GetInfoEx
description: Usado para carregar valores de atributo específicos no cache local do serviço de diretório subjacente.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Otimização usando a ADSI GetInfoEx
- GetInfoEx ADSI, otimização usando IADs GetInfoEx
- ADSI ADSI, usando, otimização usando o método IADs GetInfoEx
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

O método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) é usado para carregar valores de atributo específicos no cache local do serviço de diretório subjacente. Esse método carrega apenas os valores de atributo especificados no cache local. O método [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é usado para carregar todos os valores de atributo no cache local.

O método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtém valores atuais específicos para as propriedades de um objeto Active Directory do repositório de diretórios subjacente, atualizando os valores armazenados em cache.

No entanto, se um valor já existir no cache de propriedades, chamar o método [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) sem primeiro chamar [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para esse atributo recuperará o valor em cache em vez do valor mais atual do diretório subjacente. Isso pode fazer com que os valores de atributo atualizados sejam substituídos se o cache local tiver sido modificado, mas os valores não tiverem sido confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . O método sugerido para evitar problemas de cache é sempre confirmar alterações de valor de atributo chamando **IADs. setinfo** antes de chamar [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).


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



## <a name="retrieving-active-directory-constructed-attributes"></a>Recuperando Active Directory atributos construídos

Em Active Directory, a maioria dos atributos construídos é recuperada e armazenada em cache quando o método [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) é chamado ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) executa uma chamada de **IADs. GetInfo** implícita se o cache estiver vazio). Alguns atributos construídos, no entanto, não são automaticamente recuperados e armazenados em cache e, portanto, exigem que o método [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) seja chamado explicitamente para recuperá-los. Por exemplo, em Active Directory, o atributo [**canôniconame**](/windows/desktop/ADSchema/a-canonicalname) não é recuperado quando o método **IADs. GetInfo** é chamado e **IADs. Get** retornará a **\_ propriedade e ADS \_ \_ não \_ encontrada**. O método **IADs. GetInfoEx** deve ser chamado para recuperar o atributo **canôniconame** . Esses mesmos atributos construídos também não serão recuperados usando a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) para enumerar os atributos.

Para obter mais informações e um exemplo de código que mostra como recuperar todos os valores de atributo, consulte [exemplo de código para ler um atributo construído](example-code-for-reading-a-constructed-attribute.md).

 

 