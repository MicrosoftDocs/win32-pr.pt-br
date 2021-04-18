---
title: Propriedade de largura de banda IWMPNetwork
description: A propriedade bandWidth Obtém a largura de banda atual do item de mídia.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- Propriedade de largura de banda Windows Media Player
- Propriedade de largura de banda Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade bandWidth
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790523"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="6e543-106">Propriedade IWMPNetwork:: bandWidth</span><span class="sxs-lookup"><span data-stu-id="6e543-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="6e543-107">A propriedade **Bandwidth** Obtém a largura de banda atual do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="6e543-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e543-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e543-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6e543-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e543-109">Property value</span></span>

<span data-ttu-id="6e543-110">Um **System. Int32** que é a largura de banda.</span><span class="sxs-lookup"><span data-stu-id="6e543-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e543-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e543-111">Remarks</span></span>

<span data-ttu-id="6e543-112">O valor recuperado por meio de **AxWindowsMediaPlayer. URL** será zero se a URL não estiver definida.</span><span class="sxs-lookup"><span data-stu-id="6e543-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="6e543-113">Esta propriedade é válida somente para mídia de streaming.</span><span class="sxs-lookup"><span data-stu-id="6e543-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="6e543-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e543-114">Examples</span></span>

<span data-ttu-id="6e543-115">O exemplo a seguir usa a **largura de banda** para exibir a largura de banda de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="6e543-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="6e543-116">As informações são exibidas em um rótulo em resposta ao evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="6e543-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="6e543-117">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="6e543-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6e543-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e543-118">Requirements</span></span>



| <span data-ttu-id="6e543-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e543-119">Requirement</span></span> | <span data-ttu-id="6e543-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e543-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e543-121">Versão</span><span class="sxs-lookup"><span data-stu-id="6e543-121">Version</span></span><br/>   | <span data-ttu-id="6e543-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="6e543-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6e543-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e543-123">Namespace</span></span><br/> | <span data-ttu-id="6e543-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6e543-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6e543-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="6e543-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6e543-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6e543-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e543-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e543-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e543-128">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6e543-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6e543-129">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6e543-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





