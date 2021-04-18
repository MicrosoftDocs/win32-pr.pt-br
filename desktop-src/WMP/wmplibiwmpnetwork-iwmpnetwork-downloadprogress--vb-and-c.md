---
title: Propriedade IWMPNetwork downloadProgress
description: A propriedade downloadProgress Obtém a porcentagem de download concluído.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Propriedade downloadProgress Windows Media Player
- Propriedade downloadProgress Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade downloadProgress
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781407"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="5d398-106">IWMPNetwork: Propriedade ownloadProgress de:d</span><span class="sxs-lookup"><span data-stu-id="5d398-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="5d398-107">A propriedade **downloadProgress** Obtém a porcentagem de download concluído.</span><span class="sxs-lookup"><span data-stu-id="5d398-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d398-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d398-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5d398-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5d398-109">Property value</span></span>

<span data-ttu-id="5d398-110">Um **System. Int32** que é o progresso do download expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="5d398-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d398-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d398-111">Remarks</span></span>

<span data-ttu-id="5d398-112">Quando o controle do Windows Media Player está conectado a um arquivo de mídia digital que pode ser reproduzido e baixado ao mesmo tempo, a propriedade **downloadProgress** Obtém a porcentagem do arquivo total que foi baixado.</span><span class="sxs-lookup"><span data-stu-id="5d398-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="5d398-113">Atualmente, esse recurso tem suporte apenas para arquivos de mídia digital baixados de servidores Web.</span><span class="sxs-lookup"><span data-stu-id="5d398-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="5d398-114">Um arquivo de qualquer um dos seguintes formatos pode ser baixado e reproduzido simultaneamente:</span><span class="sxs-lookup"><span data-stu-id="5d398-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="5d398-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="5d398-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="5d398-116">Áudio do Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="5d398-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="5d398-117">Vídeo do Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="5d398-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="5d398-118">MP3</span><span class="sxs-lookup"><span data-stu-id="5d398-118">MP3</span></span>
-   <span data-ttu-id="5d398-119">FUNCIONALIDADES</span><span class="sxs-lookup"><span data-stu-id="5d398-119">MPEG</span></span>
-   <span data-ttu-id="5d398-120">WAV</span><span class="sxs-lookup"><span data-stu-id="5d398-120">WAV</span></span>

<span data-ttu-id="5d398-121">Além disso, alguns arquivos AVI podem ser baixados e reproduzidos simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="5d398-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="5d398-122">Use o **AxWindowsMediaPlayer. \_ WMPOCXEvents \_ BufferingEvent** para determinar quando o buffer é iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="5d398-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="5d398-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d398-123">Examples</span></span>

<span data-ttu-id="5d398-124">O exemplo de código a seguir usa **downloadProgress** para exibir a porcentagem de download concluído.</span><span class="sxs-lookup"><span data-stu-id="5d398-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="5d398-125">As informações são exibidas em um rótulo, em resposta ao evento de **buffer** .</span><span class="sxs-lookup"><span data-stu-id="5d398-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="5d398-126">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="5d398-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="5d398-127">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="5d398-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
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

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="5d398-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d398-128">Requirements</span></span>



| <span data-ttu-id="5d398-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d398-129">Requirement</span></span> | <span data-ttu-id="5d398-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5d398-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d398-131">Versão</span><span class="sxs-lookup"><span data-stu-id="5d398-131">Version</span></span><br/>   | <span data-ttu-id="5d398-132">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5d398-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5d398-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d398-133">Namespace</span></span><br/> | <span data-ttu-id="5d398-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5d398-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5d398-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="5d398-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5d398-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5d398-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d398-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d398-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d398-138">**Evento AxWindowsMediaPlayer. buffering (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5d398-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="5d398-139">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5d398-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





