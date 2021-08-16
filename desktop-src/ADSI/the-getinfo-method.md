---
title: O método GetInfo
description: O método GetInfo de IADs carrega todos os valores de atributo de um objeto ADSI no cache local do serviço de diretório subjacente.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- GetInfo ADSI , usando GETInfo de IADs
- ADSI ADSI usando o método GetInfo de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534de8bd667ed33d562ac55b6a70452b6496d0a3d708c55a2cb0fee1a86a8a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838450"
---
# <a name="the-getinfo-method"></a>O método GetInfo

O [**método IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carrega todos os valores de atributo de um objeto ADSI no cache local do serviço de diretório subjacente. O [**método IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) é usado para carregar valores de atributo específicos no cache local. Para obter mais informações sobre como usar o **método IADs::GetInfoEx,** consulte [Otimização usando GetInfoEx](optimization-using-getinfoex.md).

A ADSI fará uma chamada [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implícita quando o método [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) for chamado para um atributo específico e nenhum valor for encontrado no cache local. Quando **IADs::GetInfo** é chamado, uma chamada implícita não é repetida. No entanto, se um valor já existir no cache de propriedades, chamar o método **IADs::Get** ou **IADs::GetEx** sem chamar **PRIMEIRO IADs::GetInfo** recuperará o valor armazenado em cache em vez do valor mais atual do diretório subjacente. Isso pode fazer com que os valores de atributo atualizados sejam substituídos se o cache local tiver sido modificado, mas os valores não foram confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Para evitar problemas de cache, commit de alterações de valor de atributo chamando **IADs::SetInfo** antes de chamar **IADs::GetInfo**.


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



Alguns serviços de diretório não retornam todos os valores de atributo para um objeto em resposta a uma [**chamada IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) Nesses casos, use o [**método IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para carregar esses valores no cache local.

 

 




