---
title: Propriedade Duration IWMPMedia
description: A Propriedade Duration Obtém a duração em segundos do item de mídia atual.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Propriedade Duration Windows Media Player
- Propriedade Duration Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, Propriedade Duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756666"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="810c0-106">IWMPMedia: Propriedade uração de:d</span><span class="sxs-lookup"><span data-stu-id="810c0-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="810c0-107">A propriedade **Duration** Obtém a duração em segundos do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="810c0-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="810c0-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="810c0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="810c0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="810c0-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="810c0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="810c0-110">Property value</span></span>

<span data-ttu-id="810c0-111">Um **sistema. Double** que é a duração em segundos.</span><span class="sxs-lookup"><span data-stu-id="810c0-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="810c0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="810c0-112">Remarks</span></span>

<span data-ttu-id="810c0-113">Se essa propriedade for usada com um item de mídia diferente daquele especificado em AxWindowsMediaPlayer. currentMedia, ele não poderá conter um valor válido.</span><span class="sxs-lookup"><span data-stu-id="810c0-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="810c0-114">Para recuperar a duração de arquivos que não estão na biblioteca do usuário, você deve aguardar que o Windows Media Player Abra o arquivo; ou seja, o **OpenState** atual deve ser igual a **MediaOpen**.</span><span class="sxs-lookup"><span data-stu-id="810c0-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="810c0-115">Você pode verificar isso tratando o **AxWindowsMediaPlayer. \_ Evento WMPOCXEvents \_ OpenStateChange** ou verificando periodicamente o valor de **AxWindowsMediaPlayer. OpenState**.</span><span class="sxs-lookup"><span data-stu-id="810c0-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="810c0-116">Para listas de reprodução, a duração de cada item de mídia pode ser recuperada quando o item de mídia individual é aberto, em vez de quando a playlist é aberta.</span><span class="sxs-lookup"><span data-stu-id="810c0-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="810c0-117">Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="810c0-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="810c0-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="810c0-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="810c0-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="810c0-119">Examples</span></span>

<span data-ttu-id="810c0-120">O exemplo a seguir usa **Duration** para exibir o tempo restante no item de mídia atual em um rótulo.</span><span class="sxs-lookup"><span data-stu-id="810c0-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="810c0-121">Um temporizador atualiza o texto no rótulo a cada segundo.</span><span class="sxs-lookup"><span data-stu-id="810c0-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="810c0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="810c0-122">Requirements</span></span>



| <span data-ttu-id="810c0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="810c0-123">Requirement</span></span> | <span data-ttu-id="810c0-124">Valor</span><span class="sxs-lookup"><span data-stu-id="810c0-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="810c0-125">Versão</span><span class="sxs-lookup"><span data-stu-id="810c0-125">Version</span></span><br/>   | <span data-ttu-id="810c0-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="810c0-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="810c0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="810c0-127">Namespace</span></span><br/> | <span data-ttu-id="810c0-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="810c0-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="810c0-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="810c0-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="810c0-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="810c0-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="810c0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="810c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="810c0-132">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="810c0-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="810c0-133">**AxWindowsMediaPlayer. OpenState (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="810c0-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="810c0-134">**Evento AxWindowsMediaPlayer. OpenStateChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="810c0-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="810c0-135">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="810c0-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="810c0-136">**IWMPMedia. durationstring (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="810c0-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





