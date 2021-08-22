---
title: O método PutEx
description: O método PutEx de IADs usa o nome de uma propriedade para salvar uma propriedade com valores individuais ou múltiplos no cache de propriedades.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- PUTEx ADSI, sobre
- ADSI ADSI, exemplo de código Visual Basic , usando o método PutEx
- propriedades ADSI , salvando uma propriedade única ou com vários valores no cache de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c07fad5d22110d345b71a763add5483d7f0be5f6ae2c36557eb7f1563561c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023164"
---
# <a name="the-putex-method"></a>O método PutEx

O [**método IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa o nome de uma propriedade para salvar uma propriedade com valores individuais ou múltiplos no cache de propriedades. Isso substitui qualquer valor atualmente no cache de propriedade. Os valores no cache não são gravados no serviço de diretório subjacente até que ocorra um [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) O primeiro argumento de **PutEx** indica se você deseja substituir ou adicionar a quaisquer valores existentes para a propriedade . No exemplo a seguir, todos os valores existentes do atributo **de** descrição são apagados no cache quando **PutEx** é chamado e apagados no servidor quando **SetInfo** é chamado.


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



 

 




