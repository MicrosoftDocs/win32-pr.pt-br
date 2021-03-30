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
# <a name="the-getinfo-method"></a><span data-ttu-id="c6a34-105">O método GetInfo</span><span class="sxs-lookup"><span data-stu-id="c6a34-105">The GetInfo Method</span></span>

<span data-ttu-id="c6a34-106">O método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) carrega todos os valores de atributo para um objeto ADSI no cache local do serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="c6a34-106">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method loads all of the attribute values for an ADSI object into the local cache from the underlying directory service.</span></span> <span data-ttu-id="c6a34-107">O método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) é usado para carregar valores de atributo específicos no cache local.</span><span class="sxs-lookup"><span data-stu-id="c6a34-107">The [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache.</span></span> <span data-ttu-id="c6a34-108">Para obter mais informações sobre como usar o método **IADs:: GetInfoEx** , consulte [otimização usando GetInfoEx](optimization-using-getinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="c6a34-108">For more information about using the **IADs::GetInfoEx** method, see [Optimization Using GetInfoEx](optimization-using-getinfoex.md).</span></span>

<span data-ttu-id="c6a34-109">A ADSI fará uma chamada implícita [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) quando o método [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) ou [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) for chamado para um atributo específico e nenhum valor for encontrado no cache local.</span><span class="sxs-lookup"><span data-stu-id="c6a34-109">ADSI will make an implicit [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call when the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method is called for a specific attribute and no value is found in the local cache.</span></span> <span data-ttu-id="c6a34-110">Quando **IADs:: GetInfo** tiver sido chamado, uma chamada implícita não será repetida.</span><span class="sxs-lookup"><span data-stu-id="c6a34-110">When **IADs::GetInfo** has been called, an implicit call is not repeated.</span></span> <span data-ttu-id="c6a34-111">No entanto, se um valor já existir no cache de propriedades, chamar o método **IADs:: Get** ou **IADs:: GetEx** sem primeiro chamar **IADs:: GetInfo** recuperará o valor em cache em vez do valor mais atual do diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="c6a34-111">If a value already exists in the property cache, however, calling the **IADs::Get** or **IADs::GetEx** method without first calling **IADs::GetInfo** will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="c6a34-112">Isso pode fazer com que os valores de atributo atualizados sejam substituídos se o cache local tiver sido modificado, mas os valores não tiverem sido confirmados no serviço de diretório subjacente com uma chamada para o método [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c6a34-112">This can cause updated attribute values to be overwritten if the local cache has been modified but the values have not been committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="c6a34-113">Para evitar problemas de cache, confirme as alterações de valor de atributo chamando **IADs:: setinfo** antes de chamar **IADs:: GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="c6a34-113">To avoid caching problems, commit attribute value changes by calling **IADs::SetInfo** before calling **IADs::GetInfo**.</span></span>


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



<span data-ttu-id="c6a34-114">Alguns serviços de diretório não retornam todos os valores de atributo de um objeto em resposta a uma chamada [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="c6a34-114">Some directory services do not return all attribute values for an object in response to a [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) call.</span></span> <span data-ttu-id="c6a34-115">Nesses casos, use o método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para carregar esses valores no cache local.</span><span class="sxs-lookup"><span data-stu-id="c6a34-115">In these cases, use the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method to load these values into the local cache.</span></span>

 

 




