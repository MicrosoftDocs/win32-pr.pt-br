---
description: O método SelectParentalLevel define o nível de pai especificado para reprodução subsequente.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Método SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500355"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="92df3-103">Método SelectParentalLevel</span><span class="sxs-lookup"><span data-stu-id="92df3-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="92df3-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="92df3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="92df3-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="92df3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="92df3-106">O `SelectParentalLevel` método define o nível de pai especificado para reprodução subsequente.</span><span class="sxs-lookup"><span data-stu-id="92df3-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="92df3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92df3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92df3-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="92df3-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="92df3-109">Especifica o nível de gerenciamento do pai como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="92df3-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="92df3-110">Para habilitar o gerenciamento de pais, o parâmetro *iLevel* deve variar de 1 a 8.</span><span class="sxs-lookup"><span data-stu-id="92df3-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="92df3-111">Para desabilitar o gerenciamento de pais, defina *iLevel* como-1.</span><span class="sxs-lookup"><span data-stu-id="92df3-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="92df3-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="92df3-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="92df3-113">Especifica o usuário atual como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92df3-113">Specifies the current user as a String.</span></span> <span data-ttu-id="92df3-114">(Ignorado no momento.)</span><span class="sxs-lookup"><span data-stu-id="92df3-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="92df3-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="92df3-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="92df3-116">Especifica a senha atualmente armazenada no registro como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="92df3-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92df3-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="92df3-117">Return Value</span></span>

<span data-ttu-id="92df3-118">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="92df3-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92df3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="92df3-119">Remarks</span></span>

<span data-ttu-id="92df3-120">Esse método define o nível de acesso no objeto MSWebDVD, que determina qual conteúdo o usuário pode reproduzir.</span><span class="sxs-lookup"><span data-stu-id="92df3-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="92df3-121">Níveis mais altos podem reproduzir conteúdo de nível inferior, mas níveis inferiores não podem reproduzir conteúdo de nível superior.</span><span class="sxs-lookup"><span data-stu-id="92df3-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="92df3-122">O significado exato dos oito níveis de gerenciamento de pais de DVD varia dependendo do país/região.</span><span class="sxs-lookup"><span data-stu-id="92df3-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="92df3-123">No Estados Unidos e no Canadá, os níveis são mapeados para as categorias de classificação da MPAA (Associação de imagem de movimento da América).</span><span class="sxs-lookup"><span data-stu-id="92df3-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="92df3-124">O gerenciamento de pais no navegador de DVD está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="92df3-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="92df3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="92df3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92df3-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="92df3-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="92df3-127">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="92df3-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="92df3-128">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="92df3-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="92df3-129">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="92df3-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="92df3-130">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="92df3-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="92df3-131">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="92df3-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



