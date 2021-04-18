---
title: Método external. changeView
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método changeView altera a exibição no Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- método changeView Windows Media Player
- método changeView Windows Media Player, classe externa
- Classe externa Windows Media Player, método changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800133"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="af04a-108">Método external. changeView</span><span class="sxs-lookup"><span data-stu-id="af04a-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="af04a-109">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="af04a-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="af04a-110">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="af04a-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="af04a-111">O método **changeView** altera a exibição no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="af04a-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="af04a-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af04a-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="af04a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af04a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af04a-114">*LibraryLocationType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af04a-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af04a-115">Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo da nova exibição.</span><span class="sxs-lookup"><span data-stu-id="af04a-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="af04a-116">Por exemplo, a constante CPGenreID especifica que a nova exibição mostrará um gênero específico.</span><span class="sxs-lookup"><span data-stu-id="af04a-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="af04a-117">*LibraryLocationID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af04a-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af04a-118">**Cadeia de caracteres** que contém a ID do item específico a ser mostrado na nova exibição.</span><span class="sxs-lookup"><span data-stu-id="af04a-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="af04a-119">Por exemplo, se *LibraryLocationType* for CPGenreID, esse parâmetro especificará a ID do gênero a ser mostrado na nova exibição.</span><span class="sxs-lookup"><span data-stu-id="af04a-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="af04a-120">Esta cadeia de caracteres pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="af04a-120">This string can be empty.</span></span> <span data-ttu-id="af04a-121">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="af04a-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="af04a-122">*Filtrar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af04a-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af04a-123">**Cadeia de caracteres** que contém o filtro para a nova exibição.</span><span class="sxs-lookup"><span data-stu-id="af04a-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="af04a-124">O modo de exibição será filtrado como se o usuário tivesse inserido esse texto no controle de roda de palavras do jogador.</span><span class="sxs-lookup"><span data-stu-id="af04a-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="af04a-125">Esta cadeia de caracteres pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="af04a-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="af04a-126">*ViewParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af04a-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af04a-127">**Cadeia de caracteres** que contém parâmetros que o Windows Media Player disponibiliza para a nova página de descoberta exibida com a nova exibição.</span><span class="sxs-lookup"><span data-stu-id="af04a-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="af04a-128">Esses parâmetros não são interpretados pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="af04a-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="af04a-129">Eles são criados pela loja online e têm significado apenas para a loja online.</span><span class="sxs-lookup"><span data-stu-id="af04a-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af04a-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af04a-130">Return value</span></span>

<span data-ttu-id="af04a-131">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="af04a-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af04a-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="af04a-132">Remarks</span></span>

<span data-ttu-id="af04a-133">Em alguns casos, faz sentido definir o parâmetro *LibraryLocationID* para a cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="af04a-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="af04a-134">Por exemplo, se você definir o parâmetro *LibraryLocationType* como AllCPAlbumIDs, o novo modo de exibição representará todos os álbuns.</span><span class="sxs-lookup"><span data-stu-id="af04a-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="af04a-135">Nenhum álbum individual será o foco da nova exibição, portanto, não há necessidade de fornecer uma ID de álbum no parâmetro *LibraryLocationID* .</span><span class="sxs-lookup"><span data-stu-id="af04a-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="af04a-136">O parâmetro *ViewParams* fornece uma maneira para uma página de descoberta se comunicar com outra página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="af04a-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="af04a-137">Quando o script em uma página de descoberta chama **changeView**, o Windows Media Player ajusta sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="af04a-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="af04a-138">Esse ajuste faz com que o Player chame o método [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) do plug-in para obter a URL de uma nova página de descoberta.</span><span class="sxs-lookup"><span data-stu-id="af04a-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="af04a-139">A cadeia de caracteres que a página de descoberta original passa no parâmetro *ViewParams* não é passada para **GetTemplate**.</span><span class="sxs-lookup"><span data-stu-id="af04a-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="af04a-140">No entanto, a página nova descoberta pode recuperar a cadeia de caracteres *ViewParams* chamando [external. viewparameters](external-viewparameters.md).</span><span class="sxs-lookup"><span data-stu-id="af04a-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af04a-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af04a-141">Requirements</span></span>



| <span data-ttu-id="af04a-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="af04a-142">Requirement</span></span> | <span data-ttu-id="af04a-143">Valor</span><span class="sxs-lookup"><span data-stu-id="af04a-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af04a-144">Versão</span><span class="sxs-lookup"><span data-stu-id="af04a-144">Version</span></span><br/> | <span data-ttu-id="af04a-145">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="af04a-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="af04a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="af04a-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="af04a-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af04a-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af04a-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="af04a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af04a-149">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="af04a-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="af04a-150">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="af04a-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="af04a-151">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="af04a-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="af04a-152">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="af04a-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="af04a-153">**External. viewparameters**</span><span class="sxs-lookup"><span data-stu-id="af04a-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 





