---
title: Método IWMPMediaCollection getByAuthor
description: O método getByAuthor retorna uma interface IWMPPlaylist que fornece acesso aos itens de mídia pelo autor especificado.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- método getByAuthor Windows Media Player
- método getByAuthor Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getByAuthor
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787443"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="853df-106">Método IWMPMediaCollection:: getByAuthor</span><span class="sxs-lookup"><span data-stu-id="853df-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="853df-107">O `getByAuthor` método retorna uma interface **IWMPPlaylist** que fornece acesso aos itens de mídia pelo autor especificado.</span><span class="sxs-lookup"><span data-stu-id="853df-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="853df-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="853df-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="853df-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="853df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="853df-110">*bstrAuthor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="853df-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="853df-111">O **System. String** que é o nome do autor.</span><span class="sxs-lookup"><span data-stu-id="853df-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="853df-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="853df-112">Return value</span></span>

<span data-ttu-id="853df-113">Uma interface **WMPLib. IWMPPlaylist** para os itens de mídia recuperados.</span><span class="sxs-lookup"><span data-stu-id="853df-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="853df-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="853df-114">Remarks</span></span>

<span data-ttu-id="853df-115">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="853df-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="853df-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="853df-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="853df-117">Há duas maneiras de se recuperar uma interface **IWMPMediaCollection** , e o comportamento do `getByAuthor` método depende de quais dessas duas maneiras você usa.</span><span class="sxs-lookup"><span data-stu-id="853df-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="853df-118">Se você recuperar a interface chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), o `getByAuthor` método retornará todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="853df-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="853df-119">No entanto, se você recuperar a interface chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o `getByAuthor` método retornará apenas os itens de áudio na biblioteca que têm o atributo e o valor especificados.</span><span class="sxs-lookup"><span data-stu-id="853df-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="853df-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="853df-120">Examples</span></span>

<span data-ttu-id="853df-121">O exemplo a seguir usa `getByAuthor` para criar uma lista de reprodução de itens de mídia quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="853df-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="853df-122">A lista de reprodução contém itens que correspondem ao nome do autor especificado pelo usuário em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="853df-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="853df-123">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="853df-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="853df-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="853df-124">Requirements</span></span>



| <span data-ttu-id="853df-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="853df-125">Requirement</span></span> | <span data-ttu-id="853df-126">Valor</span><span class="sxs-lookup"><span data-stu-id="853df-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="853df-127">Versão</span><span class="sxs-lookup"><span data-stu-id="853df-127">Version</span></span><br/>   | <span data-ttu-id="853df-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="853df-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="853df-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="853df-129">Namespace</span></span><br/> | <span data-ttu-id="853df-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="853df-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="853df-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="853df-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="853df-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="853df-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="853df-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="853df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="853df-134">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="853df-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="853df-135">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="853df-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





