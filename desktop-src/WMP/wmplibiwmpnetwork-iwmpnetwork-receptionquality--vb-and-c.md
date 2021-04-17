---
title: Propriedade IWMPNetwork receptionQuality
description: A propriedade receptionQuality Obtém a porcentagem de pacotes que não são perdidos nos últimos 30 segundos.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- Propriedade receptionQuality Windows Media Player
- Propriedade receptionQuality Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade receptionQuality
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764092"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="dc707-106">Propriedade IWMPNetwork:: receptionQuality</span><span class="sxs-lookup"><span data-stu-id="dc707-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="dc707-107">A propriedade **receptionQuality** Obtém a porcentagem de pacotes que não são perdidos nos últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="dc707-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc707-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc707-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="dc707-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dc707-109">Property value</span></span>

<span data-ttu-id="dc707-110">Um **System. Int32** que é a qualidade da recepção.</span><span class="sxs-lookup"><span data-stu-id="dc707-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc707-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc707-111">Remarks</span></span>

<span data-ttu-id="dc707-112">O número de pacotes recebidos, perdidos e recuperados durante o streaming é monitorado uma vez a cada segundo.</span><span class="sxs-lookup"><span data-stu-id="dc707-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="dc707-113">A propriedade **receptionQuality** Obtém a porcentagem de pacotes que não foram perdidos durante os últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="dc707-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="dc707-114">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero.</span><span class="sxs-lookup"><span data-stu-id="dc707-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="dc707-115">O valor não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="dc707-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="dc707-116">Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="dc707-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="dc707-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc707-117">Examples</span></span>

<span data-ttu-id="dc707-118">O exemplo a seguir usa **receptionQuality** para exibir a porcentagem de pacotes recebidos em um rótulo, em resposta ao evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dc707-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="dc707-119">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="dc707-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="dc707-120">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="dc707-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="dc707-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc707-121">Requirements</span></span>



| <span data-ttu-id="dc707-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc707-122">Requirement</span></span> | <span data-ttu-id="dc707-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dc707-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc707-124">Versão</span><span class="sxs-lookup"><span data-stu-id="dc707-124">Version</span></span><br/>   | <span data-ttu-id="dc707-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="dc707-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dc707-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc707-126">Namespace</span></span><br/> | <span data-ttu-id="dc707-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dc707-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dc707-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="dc707-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dc707-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dc707-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc707-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc707-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc707-131">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc707-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc707-132">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc707-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





