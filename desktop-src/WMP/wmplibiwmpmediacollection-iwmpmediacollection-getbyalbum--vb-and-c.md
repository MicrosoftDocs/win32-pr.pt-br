---
title: Método IWMPMediaCollection getByAlbum
description: O método getByAlbum retorna uma interface IWMPPlaylist que fornece acesso a itens de mídia do álbum especificado.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- método getByAlbum Windows Media Player
- método getByAlbum Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758264"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="6fef7-106">Método IWMPMediaCollection:: getByAlbum</span><span class="sxs-lookup"><span data-stu-id="6fef7-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="6fef7-107">O método **getByAlbum** retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="6fef7-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fef7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fef7-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="6fef7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fef7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fef7-110">*bstrAlbum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fef7-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fef7-111">O **System. String** que é o título do álbum.</span><span class="sxs-lookup"><span data-stu-id="6fef7-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fef7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fef7-112">Return value</span></span>

<span data-ttu-id="6fef7-113">Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.</span><span class="sxs-lookup"><span data-stu-id="6fef7-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fef7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fef7-114">Remarks</span></span>

<span data-ttu-id="6fef7-115">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6fef7-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="6fef7-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6fef7-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6fef7-117">Há duas maneiras de recuperar uma interface **IWMPMediaCollection** , e o comportamento do método **getByAlbum** depende de quais dessas duas maneiras você usa.</span><span class="sxs-lookup"><span data-stu-id="6fef7-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="6fef7-118">Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o método **getByAlbum** retornará todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6fef7-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="6fef7-119">No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o método **getByAlbum** retornará apenas os itens de áudio na biblioteca que pertencem ao álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="6fef7-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="6fef7-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6fef7-120">Examples</span></span>

<span data-ttu-id="6fef7-121">O exemplo a seguir usa **getByAlbum** para criar uma lista de reprodução de itens de mídia quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="6fef7-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="6fef7-122">A lista de reprodução contém itens com o álbum especificado pelo usuário em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="6fef7-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="6fef7-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="6fef7-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6fef7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fef7-124">Requirements</span></span>



| <span data-ttu-id="6fef7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fef7-125">Requirement</span></span> | <span data-ttu-id="6fef7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6fef7-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fef7-127">Versão</span><span class="sxs-lookup"><span data-stu-id="6fef7-127">Version</span></span><br/>   | <span data-ttu-id="6fef7-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="6fef7-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6fef7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fef7-129">Namespace</span></span><br/> | <span data-ttu-id="6fef7-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6fef7-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6fef7-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="6fef7-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6fef7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6fef7-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fef7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fef7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fef7-134">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6fef7-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6fef7-135">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6fef7-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





