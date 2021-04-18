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
# <a name="the-get-method"></a><span data-ttu-id="69eb7-105">O método Get</span><span class="sxs-lookup"><span data-stu-id="69eb7-105">The Get Method</span></span>

<span data-ttu-id="69eb7-106">O método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) é usado para recuperar atributos nomeados individuais de um objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="69eb7-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="69eb7-107">O exemplo de código a seguir usa o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar um atributo nomeado de um objeto.</span><span class="sxs-lookup"><span data-stu-id="69eb7-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


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



<span data-ttu-id="69eb7-108">Em linguagens de automação, os atributos nomeados também podem ser acessados diretamente usando a notação de ponto.</span><span class="sxs-lookup"><span data-stu-id="69eb7-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="69eb7-109">Por exemplo, **objeto. Get ("distinguishedName")** é idêntico a **Object. DistinguishedName**.</span><span class="sxs-lookup"><span data-stu-id="69eb7-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="69eb7-110">O exemplo de código a seguir é idêntico ao exemplo anterior, exceto pelo fato de que o atributo **distinguishedName** é acessado usando a notação de ponto.</span><span class="sxs-lookup"><span data-stu-id="69eb7-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


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



<span data-ttu-id="69eb7-111">Se um valor não for definido no objeto, o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) retornará o erro "propriedade não encontrada no cache".</span><span class="sxs-lookup"><span data-stu-id="69eb7-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 




