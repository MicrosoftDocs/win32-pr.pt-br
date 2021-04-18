---
title: Método external. changeViewOnlineList
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. changeViewOnlineList
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- método changeViewOnlineList Windows Media Player
- método changeViewOnlineList Windows Media Player, classe externa
- Classe externa Windows Media Player, método changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810553"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="fe525-107">Método external. changeViewOnlineList</span><span class="sxs-lookup"><span data-stu-id="fe525-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="fe525-108">Este tópico descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="fe525-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fe525-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fe525-110">O método **changeViewOnlineList** altera a exibição no Windows Media Player para exibir uma lista gerada dinamicamente pela loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe525-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe525-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="fe525-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe525-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe525-113">*LibraryLocationType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe525-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe525-114">Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo da nova exibição.</span><span class="sxs-lookup"><span data-stu-id="fe525-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="fe525-115">Por exemplo, a constante CPGenreID especifica que a nova exibição mostrará um gênero específico.</span><span class="sxs-lookup"><span data-stu-id="fe525-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="fe525-116">*LibraryLocationID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe525-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe525-117">**Cadeia de caracteres** que contém a ID do item específico a ser mostrado na nova exibição.</span><span class="sxs-lookup"><span data-stu-id="fe525-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="fe525-118">Por exemplo, se *LibraryLocationType* for CPGenreID, esse parâmetro especificará a ID do gênero a ser mostrado na nova exibição.</span><span class="sxs-lookup"><span data-stu-id="fe525-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="fe525-119">Esta cadeia de caracteres pode estar vazia.</span><span class="sxs-lookup"><span data-stu-id="fe525-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="fe525-120">*Parâmetros* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe525-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe525-121">**Cadeia de caracteres** que contém parâmetros que o Windows Media Player passa para o plug-in do loja online chamando [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span><span class="sxs-lookup"><span data-stu-id="fe525-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="fe525-122">Esses parâmetros não são interpretados pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fe525-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="fe525-123">Eles são criados pela loja online e têm significado apenas para a loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="fe525-124">Esta cadeia de caracteres pode estar vazia</span><span class="sxs-lookup"><span data-stu-id="fe525-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="fe525-125">*FriendlyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe525-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe525-126">A **cadeia de caracteres** que contém um nome amigável, a ser exibida pelo Windows Media Player, para a lista dinâmica.</span><span class="sxs-lookup"><span data-stu-id="fe525-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="fe525-127">*ListType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe525-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe525-128">Uma constante de local de biblioteca que especifica o tipo dos itens na lista gerada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fe525-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="fe525-129">Por exemplo, se o valor desse parâmetro for CPTrackID, a lista dinâmica conterá faixas.</span><span class="sxs-lookup"><span data-stu-id="fe525-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="fe525-130">*Modo de exibição* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe525-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe525-131">**Cadeia de caracteres** que especifica o modo que o Windows Media Player usará para exibir a lista dinâmica.</span><span class="sxs-lookup"><span data-stu-id="fe525-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="fe525-132">O chamador deve definir esse parâmetro como um dos valores a seguir, que são definidos em contentpartner. h:</span><span class="sxs-lookup"><span data-stu-id="fe525-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="fe525-133">ViewModeReport</span><span class="sxs-lookup"><span data-stu-id="fe525-133">ViewModeReport</span></span>

<span data-ttu-id="fe525-134">ViewModeDetails</span><span class="sxs-lookup"><span data-stu-id="fe525-134">ViewModeDetails</span></span>

<span data-ttu-id="fe525-135">ViewModeIcon</span><span class="sxs-lookup"><span data-stu-id="fe525-135">ViewModeIcon</span></span>

<span data-ttu-id="fe525-136">ViewModeTile</span><span class="sxs-lookup"><span data-stu-id="fe525-136">ViewModeTile</span></span>

<span data-ttu-id="fe525-137">ViewModeOrderedList</span><span class="sxs-lookup"><span data-stu-id="fe525-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe525-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe525-138">Return value</span></span>

<span data-ttu-id="fe525-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fe525-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe525-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe525-140">Remarks</span></span>

<span data-ttu-id="fe525-141">Quando o script em uma página de descoberta chama **changeViewOnlineList**, o Windows Media Player passa alguns dos parâmetros para os métodos [IWMPContentPartner:: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) e [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , que são implementados pelo plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="fe525-142">A tabela a seguir mostra a correspondência entre os parâmetros dos três métodos.</span><span class="sxs-lookup"><span data-stu-id="fe525-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="fe525-143">parâmetro changeViewOnlineList</span><span class="sxs-lookup"><span data-stu-id="fe525-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="fe525-144">Parâmetro GetListContents</span><span class="sxs-lookup"><span data-stu-id="fe525-144">GetListContents parameter</span></span> | <span data-ttu-id="fe525-145">Parâmetro GetTemplate</span><span class="sxs-lookup"><span data-stu-id="fe525-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="fe525-146">*LocalType*</span><span class="sxs-lookup"><span data-stu-id="fe525-146">*LocationType*</span></span>                 | <span data-ttu-id="fe525-147">*local*</span><span class="sxs-lookup"><span data-stu-id="fe525-147">*location*</span></span>                | <span data-ttu-id="fe525-148">*local*</span><span class="sxs-lookup"><span data-stu-id="fe525-148">*location*</span></span>            |
| <span data-ttu-id="fe525-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="fe525-149">*LocationID*</span></span>                   | <span data-ttu-id="fe525-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fe525-150">*pContext*</span></span>                | <span data-ttu-id="fe525-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fe525-151">*pContext*</span></span>            |
| <span data-ttu-id="fe525-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="fe525-152">*Params*</span></span>                       | <span data-ttu-id="fe525-153">*bstrParams*</span><span class="sxs-lookup"><span data-stu-id="fe525-153">*bstrParams*</span></span>              | <span data-ttu-id="fe525-154">*bstrViewParams*</span><span class="sxs-lookup"><span data-stu-id="fe525-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="fe525-155">*ListType*</span><span class="sxs-lookup"><span data-stu-id="fe525-155">*ListType*</span></span>                     | <span data-ttu-id="fe525-156">*bstrListType*</span><span class="sxs-lookup"><span data-stu-id="fe525-156">*bstrListType*</span></span>            | <span data-ttu-id="fe525-157">não aplicável</span><span class="sxs-lookup"><span data-stu-id="fe525-157">not applicable</span></span>        |



 

<span data-ttu-id="fe525-158">Como todos os três métodos mostrados na tabela anterior são implementados pela loja online, você tem alguma flexibilidade em como usar os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe525-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="fe525-159">A ideia é que você forneça informações suficientes para **GetListContents** para determinar qual lista deve ser recuperada e para **GetTemplate** para determinar qual página de descoberta deve ser exibida em seguida.</span><span class="sxs-lookup"><span data-stu-id="fe525-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="fe525-160">Os exemplos a seguir ilustram duas possibilidades.</span><span class="sxs-lookup"><span data-stu-id="fe525-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="fe525-161">**Exemplo 1: uma lista dinâmica que está no catálogo da loja online**</span><span class="sxs-lookup"><span data-stu-id="fe525-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="fe525-162">Suponha que você queira que o plug-in obtenha o conteúdo da lista dinâmica que tem uma ID de 6 no catálogo da loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="fe525-163">Suponha que a lista 6 seja uma lista de faixas.</span><span class="sxs-lookup"><span data-stu-id="fe525-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="fe525-164">Você pode fornecer o plug-in com informações suficientes fazendo a seguinte chamada.</span><span class="sxs-lookup"><span data-stu-id="fe525-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="fe525-165">Observe que o parâmetro *params* está vazio; o plug-in tem informações suficientes nos outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe525-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="fe525-166">**Exemplo 2: uma lista dinâmica que não está no catálogo da loja online**</span><span class="sxs-lookup"><span data-stu-id="fe525-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="fe525-167">Suponha que você deseja que o plug-in obtenha o conteúdo de uma lista dinâmica que não esteja no catálogo da loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="fe525-168">Talvez você tenha decidido ter uma lista dinâmica que inclui as músicas escolhidas por um determinado artista.</span><span class="sxs-lookup"><span data-stu-id="fe525-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="fe525-169">Suponha que o artista tenha uma ID de 2 no catálogo da loja online.</span><span class="sxs-lookup"><span data-stu-id="fe525-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="fe525-170">Você pode fazer a chamada a seguir.</span><span class="sxs-lookup"><span data-stu-id="fe525-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="fe525-171">Observe que os parâmetros *LocationType* e *LocationID* não especificam a lista.</span><span class="sxs-lookup"><span data-stu-id="fe525-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="fe525-172">Em vez disso, o parâmetro *params* especifica a lista.</span><span class="sxs-lookup"><span data-stu-id="fe525-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="fe525-173">Os parâmetros *LocationType* e *LocationID* são passados para **IWMPContentPartner:: GetListContents**, mas, nesse caso, **GetListContents** podem ignorá-los.</span><span class="sxs-lookup"><span data-stu-id="fe525-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="fe525-174">Os parâmetros *LocationType* e *LocationID* também são passados para **IWMPContentPartner:: GetTemplate**, que podem usá-los para determinar qual página de descoberta deve ser exibida com a lista dinâmica.</span><span class="sxs-lookup"><span data-stu-id="fe525-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe525-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe525-175">Requirements</span></span>



| <span data-ttu-id="fe525-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe525-176">Requirement</span></span> | <span data-ttu-id="fe525-177">Valor</span><span class="sxs-lookup"><span data-stu-id="fe525-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe525-178">Versão</span><span class="sxs-lookup"><span data-stu-id="fe525-178">Version</span></span><br/> | <span data-ttu-id="fe525-179">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="fe525-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="fe525-180">DLL</span><span class="sxs-lookup"><span data-stu-id="fe525-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe525-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe525-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe525-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe525-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe525-183">**Objeto externo para repositórios online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="fe525-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fe525-184">**IWMPContentPartner::GetListContents**</span><span class="sxs-lookup"><span data-stu-id="fe525-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="fe525-185">**IWMPContentPartnerCallback::AddListContents**</span><span class="sxs-lookup"><span data-stu-id="fe525-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="fe525-186">**IWMPContentPartner:: GetTemplate**</span><span class="sxs-lookup"><span data-stu-id="fe525-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="fe525-187">**Local e item selecionado**</span><span class="sxs-lookup"><span data-stu-id="fe525-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





