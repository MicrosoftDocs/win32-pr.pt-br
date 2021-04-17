---
title: Propriedade de taxa de bits IWMPNetwork
description: A propriedade de taxa de bits Obtém a taxa de bit atual sendo recebida.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- Propriedade de taxa de bits Windows Media Player
- Propriedade de taxa de bits Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, propriedade de taxa de bits
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797574"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="31f69-106">Propriedade IWMPNetwork:: taxa de bits</span><span class="sxs-lookup"><span data-stu-id="31f69-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="31f69-107">A propriedade de **taxa** de bits Obtém a taxa de bit atual sendo recebida.</span><span class="sxs-lookup"><span data-stu-id="31f69-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f69-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="31f69-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="31f69-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="31f69-109">Property value</span></span>

<span data-ttu-id="31f69-110">Um **System. Int32** que é a taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="31f69-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="31f69-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="31f69-111">Remarks</span></span>

<span data-ttu-id="31f69-112">O valor dessa propriedade é uma combinação das taxas de bits de fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="31f69-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="31f69-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31f69-113">Examples</span></span>

<span data-ttu-id="31f69-114">O exemplo a seguir **usa taxa de bits para** exibir a taxa do bit de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="31f69-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="31f69-115">As informações são exibidas em um rótulo em resposta ao evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="31f69-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="31f69-116">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="31f69-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="31f69-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f69-117">Requirements</span></span>



| <span data-ttu-id="31f69-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f69-118">Requirement</span></span> | <span data-ttu-id="31f69-119">Valor</span><span class="sxs-lookup"><span data-stu-id="31f69-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f69-120">Versão</span><span class="sxs-lookup"><span data-stu-id="31f69-120">Version</span></span><br/>   | <span data-ttu-id="31f69-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="31f69-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="31f69-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="31f69-122">Namespace</span></span><br/> | <span data-ttu-id="31f69-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="31f69-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="31f69-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="31f69-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="31f69-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="31f69-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f69-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="31f69-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f69-127">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="31f69-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





