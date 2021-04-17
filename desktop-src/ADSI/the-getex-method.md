---
title: O método GetEx
description: Alguns atributos podem armazenar um ou mais valores.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- GetEx ADSI, usando IADs GetEx
- ADSI ADSI, usando, usando o método IADs GetEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a909b33664ad805b0bf483ee9f0c2b40316ec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755232"
---
# <a name="the-getex-method"></a><span data-ttu-id="c2b07-105">O método GetEx</span><span class="sxs-lookup"><span data-stu-id="c2b07-105">The GetEx Method</span></span>

<span data-ttu-id="c2b07-106">Alguns atributos podem armazenar um ou mais valores.</span><span class="sxs-lookup"><span data-stu-id="c2b07-106">Some attributes can store one or more values.</span></span> <span data-ttu-id="c2b07-107">Por exemplo, o atributo **otherTelephone** de um objeto de usuário em Active Directory é uma propriedade que pode ter zero, um ou muitos valores.</span><span class="sxs-lookup"><span data-stu-id="c2b07-107">For example, the **otherTelephone** attribute of a user object in Active Directory is a property that can have zero, one, or many values.</span></span> <span data-ttu-id="c2b07-108">Os atributos que têm vários valores são conhecidos como "atributos com valores múltiplos".</span><span class="sxs-lookup"><span data-stu-id="c2b07-108">Attributes that have multiple values are known as "multi-valued attributes".</span></span> <span data-ttu-id="c2b07-109">Se o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) for usado para recuperar um atributo de valores múltiplos, os resultados deverão ser processados de forma diferente do que se o atributo tiver um único valor.</span><span class="sxs-lookup"><span data-stu-id="c2b07-109">If the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve a multi-valued attribute, the results must be processed differently than if the attribute has a single value.</span></span> <span data-ttu-id="c2b07-110">Os resultados fornecidos pelo método [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) , no entanto, são processados da mesma maneira, independentemente se o atributo tiver um único ou vários valores.</span><span class="sxs-lookup"><span data-stu-id="c2b07-110">The results provided by the [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method, however, are processed in the same manner, regardless if the attribute has a single or multiple values.</span></span> <span data-ttu-id="c2b07-111">Em ambos os casos, o método **IADs:: GetEx** retorna os valores em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="c2b07-111">In both cases, the **IADs::GetEx** method returns the values in an array.</span></span>

<span data-ttu-id="c2b07-112">O método [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) recupera propriedades do cache de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c2b07-112">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method retrieves properties from the property cache.</span></span> <span data-ttu-id="c2b07-113">Se a propriedade especificada não for encontrada no cache, **IADs:: GetEx** executará uma chamada [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) implícita.</span><span class="sxs-lookup"><span data-stu-id="c2b07-113">If the specified property is not found in the cache, **IADs::GetEx** performs an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span>

<span data-ttu-id="c2b07-114">O método [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retorna uma matriz variante de variantes, independentemente do número de valores retornados do servidor.</span><span class="sxs-lookup"><span data-stu-id="c2b07-114">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method returns a variant array of variants regardless of the number of values returned from the server.</span></span> <span data-ttu-id="c2b07-115">Isso é verdadeiro mesmo se o atributo contiver apenas um valor.</span><span class="sxs-lookup"><span data-stu-id="c2b07-115">This is true even if the attribute only contains one value.</span></span>


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



<span data-ttu-id="c2b07-116">O método [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) também pode ser usado para atributos de valor único.</span><span class="sxs-lookup"><span data-stu-id="c2b07-116">The [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method can also be used for single-valued attributes.</span></span> <span data-ttu-id="c2b07-117">Os resultados de um atributo de valor único são processados da mesma forma que os resultados para um atributo de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="c2b07-117">The results of a single-valued attribute are processed the same as the results for a multi-valued attribute.</span></span>


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



<span data-ttu-id="c2b07-118">Se nenhum valor for definido para o atributo, [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) retornará o erro "propriedade não encontrada no cache".</span><span class="sxs-lookup"><span data-stu-id="c2b07-118">If no value is set for the attribute, [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) returns the error "Property not found in cache".</span></span>

 

 




