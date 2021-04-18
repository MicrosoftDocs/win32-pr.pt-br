---
title: Método IWMPMediaCollection getByAttribute
description: O método getByAttribute retorna uma interface IWMPPlaylist que corresponde ao atributo especificado com o valor especificado.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- método getByAttribute Windows Media Player
- método getByAttribute Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758904"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="15ceb-106">Método IWMPMediaCollection:: getByAttribute</span><span class="sxs-lookup"><span data-stu-id="15ceb-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="15ceb-107">O método **getByAttribute** retorna uma interface **IWMPPlaylist** que corresponde ao atributo especificado com o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="15ceb-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ceb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15ceb-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="15ceb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15ceb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ceb-110">*bstrattribute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ceb-111">O **System. String** que é o atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="15ceb-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="15ceb-112">*bstrvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ceb-113">O **System. String** que é o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="15ceb-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ceb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15ceb-114">Return value</span></span>

<span data-ttu-id="15ceb-115">Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.</span><span class="sxs-lookup"><span data-stu-id="15ceb-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ceb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="15ceb-116">Remarks</span></span>

<span data-ttu-id="15ceb-117">Esse método pode ser usado para criar uma consulta genérica para itens de mídia que correspondem a um valor para um atributo na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="15ceb-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="15ceb-118">Isso é útil no caso de atributos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="15ceb-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="15ceb-119">Se o atributo não existir, será resultado um erro.</span><span class="sxs-lookup"><span data-stu-id="15ceb-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="15ceb-120">Você pode usar esse método para recuperar todos os itens de mídia de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="15ceb-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="15ceb-121">Use o nome de atributo **MediaType** e um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="15ceb-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="15ceb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="15ceb-122">Value</span></span>    | <span data-ttu-id="15ceb-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="15ceb-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="15ceb-124">áudio</span><span class="sxs-lookup"><span data-stu-id="15ceb-124">audio</span></span>    | <span data-ttu-id="15ceb-125">Música e outros itens somente de áudio</span><span class="sxs-lookup"><span data-stu-id="15ceb-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="15ceb-126">outros</span><span class="sxs-lookup"><span data-stu-id="15ceb-126">other</span></span>    | <span data-ttu-id="15ceb-127">Outros itens, como um arquivo. ASF ou a URL de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="15ceb-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="15ceb-128">foto</span><span class="sxs-lookup"><span data-stu-id="15ceb-128">photo</span></span>    | <span data-ttu-id="15ceb-129">Itens de foto.</span><span class="sxs-lookup"><span data-stu-id="15ceb-129">Photo items.</span></span> <span data-ttu-id="15ceb-130">Requer o Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="15ceb-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="15ceb-131">playlist</span><span class="sxs-lookup"><span data-stu-id="15ceb-131">playlist</span></span> | <span data-ttu-id="15ceb-132">Listas de reprodução representadas como itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="15ceb-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="15ceb-133">radio</span><span class="sxs-lookup"><span data-stu-id="15ceb-133">radio</span></span>    | <span data-ttu-id="15ceb-134">Itens da estação de rádio.</span><span class="sxs-lookup"><span data-stu-id="15ceb-134">Radio station items.</span></span> <span data-ttu-id="15ceb-135">Não usado pelo Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="15ceb-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="15ceb-136">video</span><span class="sxs-lookup"><span data-stu-id="15ceb-136">video</span></span>    | <span data-ttu-id="15ceb-137">Itens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="15ceb-137">Video items.</span></span>                                              |



 

<span data-ttu-id="15ceb-138">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="15ceb-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="15ceb-139">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="15ceb-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="15ceb-140">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="15ceb-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="15ceb-141">Há duas maneiras de recuperar uma interface **IWMPMediaCollection** , e o comportamento do método **getByAttribute** depende de quais dessas duas maneiras você usa.</span><span class="sxs-lookup"><span data-stu-id="15ceb-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="15ceb-142">Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método **getByAttribute** retornará todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="15ceb-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="15ceb-143">No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método **getByAttribute** retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.</span><span class="sxs-lookup"><span data-stu-id="15ceb-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="15ceb-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="15ceb-144">Examples</span></span>

<span data-ttu-id="15ceb-145">O exemplo de código a seguir usa **getByAttribute** para reproduzir todo o conteúdo da biblioteca pelo artista chamado Triode 48.</span><span class="sxs-lookup"><span data-stu-id="15ceb-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="15ceb-146">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="15ceb-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="15ceb-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ceb-147">Requirements</span></span>



| <span data-ttu-id="15ceb-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ceb-148">Requirement</span></span> | <span data-ttu-id="15ceb-149">Valor</span><span class="sxs-lookup"><span data-stu-id="15ceb-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ceb-150">Versão</span><span class="sxs-lookup"><span data-stu-id="15ceb-150">Version</span></span><br/>   | <span data-ttu-id="15ceb-151">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="15ceb-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="15ceb-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="15ceb-152">Namespace</span></span><br/> | <span data-ttu-id="15ceb-153">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="15ceb-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="15ceb-154">Assembly</span><span class="sxs-lookup"><span data-stu-id="15ceb-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="15ceb-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="15ceb-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ceb-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="15ceb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ceb-157">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="15ceb-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="15ceb-158">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="15ceb-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="15ceb-159">**IWMPPlaylistCollection. getAll (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="15ceb-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





