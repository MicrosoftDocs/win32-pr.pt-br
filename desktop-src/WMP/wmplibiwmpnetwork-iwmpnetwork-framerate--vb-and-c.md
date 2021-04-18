---
title: Propriedade de taxa de quadros IWMPNetwork
description: A propriedade de taxa de quadros Obtém a taxa de quadros de vídeo atual.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Propriedade de taxa de quadros Windows Media Player
- Propriedade de taxa de quadros Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, propriedade de taxa de quadros
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756528"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="a8c72-106">Propriedade IWMPNetwork:: taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="a8c72-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="a8c72-107">A propriedade de **taxa** de quadros Obtém a taxa de quadros de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="a8c72-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8c72-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8c72-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a8c72-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a8c72-109">Property value</span></span>

<span data-ttu-id="a8c72-110">Um **System. Int32** que é a taxa de quadros atual em quadros por centenas de segundos.</span><span class="sxs-lookup"><span data-stu-id="a8c72-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="a8c72-111">Embora a propriedade **encodedFrameRate** meça a taxa de quadros codificados em quadros por segundo, a propriedade de **taxa** de quadros mede a taxa de quadro atual em quadros por centenas de segundos.</span><span class="sxs-lookup"><span data-stu-id="a8c72-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="a8c72-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="a8c72-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="a8c72-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8c72-113">Remarks</span></span>

<span data-ttu-id="a8c72-114">O valor da taxa de quadros atual é retornado em quadros por centenas de segundos.</span><span class="sxs-lookup"><span data-stu-id="a8c72-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="a8c72-115">Por exemplo, um valor de 2998 indica 29,98 quadros por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="a8c72-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="a8c72-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8c72-116">Examples</span></span>

<span data-ttu-id="a8c72-117">O exemplo de código a seguir usa taxa de **quadros** para exibir a taxa de quadros especificada quando o arquivo foi codificado.</span><span class="sxs-lookup"><span data-stu-id="a8c72-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="a8c72-118">As informações são exibidas em um rótulo em resposta ao evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="a8c72-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="a8c72-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="a8c72-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a8c72-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8c72-120">Requirements</span></span>



| <span data-ttu-id="a8c72-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8c72-121">Requirement</span></span> | <span data-ttu-id="a8c72-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a8c72-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c72-123">Versão</span><span class="sxs-lookup"><span data-stu-id="a8c72-123">Version</span></span><br/>   | <span data-ttu-id="a8c72-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a8c72-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a8c72-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8c72-125">Namespace</span></span><br/> | <span data-ttu-id="a8c72-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a8c72-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a8c72-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a8c72-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8c72-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a8c72-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8c72-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8c72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c72-130">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a8c72-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8c72-131">**IWMPNetwork. encodedFrameRate (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a8c72-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





