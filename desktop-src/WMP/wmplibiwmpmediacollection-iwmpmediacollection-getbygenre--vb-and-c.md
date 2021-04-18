---
title: Método IWMPMediaCollection getByGenre
description: O método getByGenre retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia do gênero especificado.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- método getByGenre Windows Media Player
- método getByGenre Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByGenre
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778664"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a><span data-ttu-id="e4bf5-106">Método IWMPMediaCollection:: getByGenre</span><span class="sxs-lookup"><span data-stu-id="e4bf5-106">IWMPMediaCollection::getByGenre method</span></span>

<span data-ttu-id="e4bf5-107">O `getByGenre` método retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do gênero especificado.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-107">The `getByGenre` method returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bf5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4bf5-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a><span data-ttu-id="e4bf5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4bf5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4bf5-110">*bstrGenre* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4bf5-110">*bstrGenre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4bf5-111">O **System. String** que é o nome do gênero.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-111">The **System.String** that is the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4bf5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4bf5-112">Return value</span></span>

<span data-ttu-id="e4bf5-113">Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4bf5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4bf5-114">Remarks</span></span>

<span data-ttu-id="e4bf5-115">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e4bf5-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e4bf5-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e4bf5-117">Há duas maneiras de se recuperar uma interface **IWMPMediaCollection** , e o comportamento do `getByGenre` método depende de quais dessas duas maneiras você usa.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByGenre` method depends on which of those two ways you use.</span></span> <span data-ttu-id="e4bf5-118">Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o `getByGenre` método retornará todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByGenre` method returns all the media items in the library.</span></span> <span data-ttu-id="e4bf5-119">No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o `getByGenre` método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByGenre` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="e4bf5-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4bf5-120">Examples</span></span>

<span data-ttu-id="e4bf5-121">O exemplo a seguir usa `getByGenre` para recuperar uma lista de reprodução de itens de mídia quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-121">The following example uses `getByGenre` to retrieve a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="e4bf5-122">A lista de reprodução contém itens com o gênero especificado pelo usuário em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-122">The playlist contains items with the genre specified by the user in a text box.</span></span> <span data-ttu-id="e4bf5-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="e4bf5-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e4bf5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4bf5-124">Requirements</span></span>



| <span data-ttu-id="e4bf5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4bf5-125">Requirement</span></span> | <span data-ttu-id="e4bf5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e4bf5-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bf5-127">Versão</span><span class="sxs-lookup"><span data-stu-id="e4bf5-127">Version</span></span><br/>   | <span data-ttu-id="e4bf5-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e4bf5-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e4bf5-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4bf5-129">Namespace</span></span><br/> | <span data-ttu-id="e4bf5-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e4bf5-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e4bf5-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="e4bf5-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e4bf5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e4bf5-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4bf5-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4bf5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4bf5-134">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4bf5-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4bf5-135">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4bf5-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





