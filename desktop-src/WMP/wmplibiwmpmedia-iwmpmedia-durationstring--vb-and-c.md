---
title: Propriedade durationstring de IWMPMedia
description: A propriedade durationstring Obtém uma cadeia de caracteres que indica a duração do item de mídia atual no formato HH MM SS.
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- Propriedade durationstring Windows Media Player
- Propriedade durationstring Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade durationstring
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753386"
---
# <a name="iwmpmediadurationstring-property"></a><span data-ttu-id="6a68d-106">IWMPMedia: Propriedade urationString de:d</span><span class="sxs-lookup"><span data-stu-id="6a68d-106">IWMPMedia::durationString property</span></span>

<span data-ttu-id="6a68d-107">A propriedade **durationstring** Obtém uma cadeia de caracteres que indica a duração do item de mídia atual no formato hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="6a68d-107">The **durationString** property gets a string indicating the duration of the current media item in HH:MM:SS format.</span></span>

<span data-ttu-id="6a68d-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6a68d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a68d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a68d-109">Syntax</span></span>


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a><span data-ttu-id="6a68d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6a68d-110">Property value</span></span>

<span data-ttu-id="6a68d-111">Um **System. String** que é a duração.</span><span class="sxs-lookup"><span data-stu-id="6a68d-111">A **System.String** that is the duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a68d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a68d-112">Remarks</span></span>

<span data-ttu-id="6a68d-113">Se essa propriedade for usada com um item de mídia diferente daquele especificado em AxWindowsMediaPlayer. currentMedia, ele não poderá conter um valor válido.</span><span class="sxs-lookup"><span data-stu-id="6a68d-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span> <span data-ttu-id="6a68d-114">Se o item de mídia tiver menos de uma hora, a parte de horas do valor de retorno será omitida.</span><span class="sxs-lookup"><span data-stu-id="6a68d-114">If the media item is less than an hour long, the hours portion of the return value is omitted.</span></span>

<span data-ttu-id="6a68d-115">Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6a68d-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="6a68d-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6a68d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6a68d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a68d-117">Examples</span></span>

<span data-ttu-id="6a68d-118">O exemplo a seguir usa **durationstring** para exibir a duração do item de mídia atual como texto formatado em um rótulo.</span><span class="sxs-lookup"><span data-stu-id="6a68d-118">The following example uses **durationString** to display the duration of the current media item as formatted text in a label.</span></span> <span data-ttu-id="6a68d-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="6a68d-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6a68d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a68d-120">Requirements</span></span>



| <span data-ttu-id="6a68d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a68d-121">Requirement</span></span> | <span data-ttu-id="6a68d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6a68d-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a68d-123">Versão</span><span class="sxs-lookup"><span data-stu-id="6a68d-123">Version</span></span><br/>   | <span data-ttu-id="6a68d-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="6a68d-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6a68d-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a68d-125">Namespace</span></span><br/> | <span data-ttu-id="6a68d-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6a68d-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6a68d-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="6a68d-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6a68d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6a68d-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a68d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a68d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a68d-130">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6a68d-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a68d-131">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6a68d-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6a68d-132">**IWMPMedia. Duration (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6a68d-132">**IWMPMedia.duration (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





