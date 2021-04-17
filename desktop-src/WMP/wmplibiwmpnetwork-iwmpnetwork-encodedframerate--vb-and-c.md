---
title: Propriedade IWMPNetwork encodedFrameRate
description: A propriedade encodedFrameRate Obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- Propriedade encodedFrameRate Windows Media Player
- Propriedade encodedFrameRate Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade encodedFrameRate
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754920"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="2bf10-106">Propriedade IWMPNetwork:: encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="2bf10-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="2bf10-107">A propriedade **encodedFrameRate** Obtém a taxa de quadros de vídeo especificada pelo autor do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2bf10-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf10-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bf10-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2bf10-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2bf10-109">Property value</span></span>

<span data-ttu-id="2bf10-110">Um **System. Int32** que é a taxa de quadros codificada em quadros por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="2bf10-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="2bf10-111">Embora a propriedade **encodedFrameRate** meça a taxa de quadros codificados em quadros por segundo, a propriedade de **taxa** de quadros mede a taxa de quadro atual em quadros por centenas de segundos.</span><span class="sxs-lookup"><span data-stu-id="2bf10-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2bf10-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2bf10-112">Examples</span></span>

<span data-ttu-id="2bf10-113">O exemplo de código a seguir usa **encodedFrameRate** para exibir a taxa de quadros especificada quando o arquivo foi codificado.</span><span class="sxs-lookup"><span data-stu-id="2bf10-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="2bf10-114">As informações são exibidas em um rótulo, em resposta ao evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="2bf10-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="2bf10-115">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="2bf10-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
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

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2bf10-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf10-116">Requirements</span></span>



| <span data-ttu-id="2bf10-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bf10-117">Requirement</span></span> | <span data-ttu-id="2bf10-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2bf10-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf10-119">Versão</span><span class="sxs-lookup"><span data-stu-id="2bf10-119">Version</span></span><br/>   | <span data-ttu-id="2bf10-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="2bf10-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2bf10-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bf10-121">Namespace</span></span><br/> | <span data-ttu-id="2bf10-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2bf10-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2bf10-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="2bf10-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2bf10-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf10-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf10-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bf10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf10-126">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2bf10-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2bf10-127">**IWMPNetwork. taxa de quadros (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2bf10-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





