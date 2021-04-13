---
description: O método SelectParentalCountry define o país/região pai especificado para reprodução subsequente.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Método SelectParentalCountry
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500582"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="17d9b-103">Método SelectParentalCountry</span><span class="sxs-lookup"><span data-stu-id="17d9b-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="17d9b-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="17d9b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="17d9b-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="17d9b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="17d9b-106">O `SelectParentalCountry` método define o país/região pai especificado para reprodução subsequente.</span><span class="sxs-lookup"><span data-stu-id="17d9b-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="17d9b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17d9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d9b-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="17d9b-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="17d9b-109">Especifica o país/região como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="17d9b-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="17d9b-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="17d9b-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="17d9b-111">Especifica o usuário conectado no momento como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="17d9b-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="17d9b-112">(Ignorado no momento.)</span><span class="sxs-lookup"><span data-stu-id="17d9b-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="17d9b-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="17d9b-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="17d9b-114">Especifica a cadeia de caracteres de senha do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="17d9b-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d9b-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="17d9b-115">Return Value</span></span>

<span data-ttu-id="17d9b-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="17d9b-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d9b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="17d9b-117">Remarks</span></span>

<span data-ttu-id="17d9b-118">O país/região pai determina como os níveis de pais são interpretados.</span><span class="sxs-lookup"><span data-stu-id="17d9b-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="17d9b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="17d9b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d9b-120">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="17d9b-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="17d9b-121">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="17d9b-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="17d9b-122">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="17d9b-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="17d9b-123">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="17d9b-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="17d9b-124">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="17d9b-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="17d9b-125">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="17d9b-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



