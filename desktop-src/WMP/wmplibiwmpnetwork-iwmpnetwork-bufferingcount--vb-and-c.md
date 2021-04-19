---
title: Propriedade IWMPNetwork bufferingCount
description: A propriedade bufferingCount Obtém o número de vezes que o buffer ocorreu durante a reprodução.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- Propriedade bufferingCount Windows Media Player
- Propriedade bufferingCount Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade bufferingCount
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770647"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="cafe8-106">Propriedade IWMPNetwork:: bufferingCount</span><span class="sxs-lookup"><span data-stu-id="cafe8-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="cafe8-107">A propriedade **bufferingCount** Obtém o número de vezes que o buffer ocorreu durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="cafe8-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafe8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cafe8-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="cafe8-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cafe8-109">Property value</span></span>

<span data-ttu-id="cafe8-110">Um **System. Int32** que é a contagem de buffers.</span><span class="sxs-lookup"><span data-stu-id="cafe8-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="cafe8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cafe8-111">Remarks</span></span>

<span data-ttu-id="cafe8-112">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é redefinida como zero.</span><span class="sxs-lookup"><span data-stu-id="cafe8-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="cafe8-113">Ele não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="cafe8-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="cafe8-114">O armazenamento em buffer se aplica somente ao conteúdo de streaming.</span><span class="sxs-lookup"><span data-stu-id="cafe8-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="cafe8-115">Essa propriedade obtém informações válidas somente durante o tempo de execução quando a URL para reprodução é definida usando a propriedade **AxWindowsMediaPlayer. URL** .</span><span class="sxs-lookup"><span data-stu-id="cafe8-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="cafe8-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cafe8-116">Examples</span></span>

<span data-ttu-id="cafe8-117">O exemplo a seguir usa *bufferingCount* para exibir o número de vezes que o buffer ocorre durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="cafe8-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="cafe8-118">As informações são exibidas em um rótulo em resposta ao evento de buffer.</span><span class="sxs-lookup"><span data-stu-id="cafe8-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="cafe8-119">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="cafe8-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="cafe8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cafe8-120">Requirements</span></span>



| <span data-ttu-id="cafe8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cafe8-121">Requirement</span></span> | <span data-ttu-id="cafe8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cafe8-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cafe8-123">Versão</span><span class="sxs-lookup"><span data-stu-id="cafe8-123">Version</span></span><br/>   | <span data-ttu-id="cafe8-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="cafe8-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cafe8-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="cafe8-125">Namespace</span></span><br/> | <span data-ttu-id="cafe8-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cafe8-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cafe8-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="cafe8-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cafe8-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cafe8-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cafe8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cafe8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafe8-130">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cafe8-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cafe8-131">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cafe8-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





