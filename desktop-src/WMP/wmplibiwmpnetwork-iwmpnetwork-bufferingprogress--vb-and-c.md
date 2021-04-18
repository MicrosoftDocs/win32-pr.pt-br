---
title: Propriedade IWMPNetwork bufferingProgress
description: A propriedade bufferingProgress Obtém a porcentagem de buffer concluído.
ms.assetid: 8dc9f31e-7c34-4714-a633-d92c3da3052b
keywords:
- Propriedade bufferingProgress Windows Media Player
- Propriedade bufferingProgress Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade bufferingProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da8a27ba41e5c4e201a5bdf0197992c30bce80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810732"
---
# <a name="iwmpnetworkbufferingprogress-property"></a><span data-ttu-id="dbe7d-106">Propriedade IWMPNetwork:: bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="dbe7d-106">IWMPNetwork::bufferingProgress property</span></span>

<span data-ttu-id="dbe7d-107">A propriedade **bufferingProgress** Obtém a porcentagem de buffer concluído.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-107">The **bufferingProgress** property gets the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe7d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbe7d-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingProgress {get; set;}
```


```VB

Public ReadOnly Property bufferingProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="dbe7d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dbe7d-109">Property value</span></span>

<span data-ttu-id="dbe7d-110">Um **System. Int32** que é o progresso do buffer expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-110">A **System.Int32** that is the buffering progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe7d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbe7d-111">Remarks</span></span>

<span data-ttu-id="dbe7d-112">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="dbe7d-113">Ele não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="dbe7d-114">O armazenamento em buffer se aplica somente ao conteúdo de streaming.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="dbe7d-115">Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="dbe7d-115">This property gets valid information only during run time when the URL for playback is set using the **AxWindowsMediaPlayer.URL** property.</span></span>

<span data-ttu-id="dbe7d-116">Use o **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar quando o buffer é iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-116">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="dbe7d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dbe7d-117">Examples</span></span>

<span data-ttu-id="dbe7d-118">O exemplo a seguir usa **bufferingProgress** para exibir a porcentagem de buffer concluído em um rótulo, em resposta ao evento de buffer.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-118">The following example uses **bufferingProgress** to display the percentage of buffering completed in a label, in response to the Buffering Event.</span></span> <span data-ttu-id="dbe7d-119">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="dbe7d-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="dbe7d-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the buffering progress in a timer event handler.
private void UpdateBufferingProgress(object sender, EventArgs e)
{
    bufferingProgressLabel.Text = ("Buffering progress: " + player.network.bufferingProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the buffering progress in a timer event handler.
Public Sub UpdateBufferingProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    bufferingProgressLabel.Text = (&quot;Buffering progress: &quot; + player.network.bufferingProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="dbe7d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbe7d-121">Requirements</span></span>



| <span data-ttu-id="dbe7d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbe7d-122">Requirement</span></span> | <span data-ttu-id="dbe7d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dbe7d-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe7d-124">Versão</span><span class="sxs-lookup"><span data-stu-id="dbe7d-124">Version</span></span><br/>   | <span data-ttu-id="dbe7d-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="dbe7d-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dbe7d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbe7d-126">Namespace</span></span><br/> | <span data-ttu-id="dbe7d-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dbe7d-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="dbe7d-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dbe7d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dbe7d-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe7d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbe7d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe7d-131">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbe7d-132">**Evento AxWindowsMediaPlayer. buffering (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-132">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="dbe7d-133">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dbe7d-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





