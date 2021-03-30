---
title: O método GetInfo
description: O método IADs GetInfo carrega todos os valores de atributo para um objeto ADSI no cache local do serviço de diretório subjacente.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- ADSI GetInfo, usando IADs GetInfo
- ADSI da ADSI, usando, usando o método IADs GetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634859"
---
# <a name="the-getinfo-method"></a>O método GetInfo

O método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carrega todos os valores de atributo para um objeto ADSI no cache local do serviço de diretório subjacente. O método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) é usado para carregar valores de atributo específicos no cache local. Para obter mais informações sobre como usar o método **IADs:: GetInfoEx** , consulte [otimização usando GetInfoEx](optimization-using-getinfoex.md).

A ADSI fará uma chamada implícita [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) quando o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) for chamado para um atributo específico e nenhum valor for encontrado no cache local. Quando **IADs:: GetInfo** tiver sido chamado, uma chamada implícita não será repetida. No entanto, se um valor já existir no cache de propriedades, chamar o método **IADs:: Get** ou **IADs:: GetEx** sem primeiro chamar **IADs:: GetInfo** recuperará o valor em cache em vez do valor mais atual do diretório subjacente. Isso pode fazer com que os valores de atributo atualizados sejam substituídos se o cache local tiver sido modificado, mas os valores não tiverem sido confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Para evitar problemas de cache, confirme as alterações de valor de atributo chamando **IADs:: setinfo** antes de chamar **IADs:: GetInfo**.


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



Alguns serviços de diretório não retornam todos os valores de atributo de um objeto em resposta a uma chamada [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) . Nesses casos, use o método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para carregar esses valores no cache local.

 

 




