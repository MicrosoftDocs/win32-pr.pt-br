---
description: O GetPlayerParentalLevel recupera o conjunto de nível de gerenciamento de pais no objeto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Método GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087265"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="2186c-103">Método GetPlayerParentalLevel</span><span class="sxs-lookup"><span data-stu-id="2186c-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="2186c-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2186c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2186c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2186c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2186c-106">O `GetPlayerParentalLevel` recupera o nível de gerenciamento do pai definido no objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="2186c-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="2186c-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2186c-107">Return Value</span></span>

<span data-ttu-id="2186c-108">Retorna um valor inteiro especificando o nível pai atual no navegador de DVD ou-1 se o gerenciamento de pais está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2186c-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="2186c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2186c-109">Remarks</span></span>

<span data-ttu-id="2186c-110">Um aplicativo de Player é responsável por impor controles dos pais.</span><span class="sxs-lookup"><span data-stu-id="2186c-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="2186c-111">O nível do pai do Player é um valor definido por um aplicativo do que pode ser usado para indicar o nível mais alto de pais que o usuário atual pode exibir.</span><span class="sxs-lookup"><span data-stu-id="2186c-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="2186c-112">Quando o navegador de DVD encontra um novo nível de pai, use esse método para determinar se o novo nível é maior do que o nível definido pelo aplicativo por meio de [**SelectParentalLevel**](selectparentallevel-method.md).</span><span class="sxs-lookup"><span data-stu-id="2186c-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2186c-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="2186c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2186c-114">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="2186c-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="2186c-115">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="2186c-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="2186c-116">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="2186c-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="2186c-117">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="2186c-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



