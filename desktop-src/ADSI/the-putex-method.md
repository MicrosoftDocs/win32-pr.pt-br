---
title: O método PutEx
description: O método IADs PutEx usa o nome de uma propriedade para salvar uma propriedade com um ou vários valores no cache de propriedades.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PutEx ADSI, sobre
- ADSI ADSI, código de exemplo Visual Basic, usando o método PutEx
- Propriedades ADSI, salvando uma propriedade única ou com vários valores no cache de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822180"
---
# <a name="the-putex-method"></a>O método PutEx

O método [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa o nome de uma propriedade para salvar uma propriedade com um ou vários valores no cache de propriedades. Isso substitui qualquer valor atualmente no cache de propriedades. Os valores no cache não são gravados no serviço de diretório subjacente até que ocorra um [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . O primeiro argumento de **PutEx** indica se você deseja substituir ou adicionar a quaisquer valores existentes para a propriedade. No exemplo a seguir, todos os valores existentes do atributo **Description** são apagados no cache quando **PutEx** é chamado e apagados no servidor quando **setinfo** é chamado.


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




