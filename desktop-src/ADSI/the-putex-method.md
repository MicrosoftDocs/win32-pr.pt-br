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
# <a name="the-putex-method"></a><span data-ttu-id="f1f33-106">O método PutEx</span><span class="sxs-lookup"><span data-stu-id="f1f33-106">The PutEx Method</span></span>

<span data-ttu-id="f1f33-107">O método [**IADs::P utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa o nome de uma propriedade para salvar uma propriedade com um ou vários valores no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1f33-107">The [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the name of a property to save a property with single or multiple values into the property cache.</span></span> <span data-ttu-id="f1f33-108">Isso substitui qualquer valor atualmente no cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1f33-108">This overwrites any value currently in the property cache.</span></span> <span data-ttu-id="f1f33-109">Os valores no cache não são gravados no serviço de diretório subjacente até que ocorra um [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="f1f33-109">The values in the cache are not written to the underlying directory service until an [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) occurs.</span></span> <span data-ttu-id="f1f33-110">O primeiro argumento de **PutEx** indica se você deseja substituir ou adicionar a quaisquer valores existentes para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="f1f33-110">The first argument of **PutEx** indicates whether you want to replace or add to any existing values for the property.</span></span> <span data-ttu-id="f1f33-111">No exemplo a seguir, todos os valores existentes do atributo **Description** são apagados no cache quando **PutEx** é chamado e apagados no servidor quando **setinfo** é chamado.</span><span class="sxs-lookup"><span data-stu-id="f1f33-111">In the following example, any existing values of the **description** attribute are erased in the cache when **PutEx** is called, and erased on the server when **SetInfo** is called.</span></span>


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



 

 




