---
title: Propriedade IWMPControls currentPositionString
description: A propriedade currentPositionString Obtém a posição atual no item de mídia como uma cadeia de caracteres formatada como HH MM SS (horas, minutos e segundos).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- Propriedade currentPositionString Windows Media Player
- Propriedade currentPositionString Windows Media Player, interface IWMPControls
- Interface IWMPControls Windows Media Player, Propriedade currentPositionString
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767716"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="ccfd9-106">Propriedade IWMPControls:: currentPositionString</span><span class="sxs-lookup"><span data-stu-id="ccfd9-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="ccfd9-107">A propriedade **currentPositionString** Obtém a posição atual no item de mídia como uma cadeia de caracteres formatada como hh: mm: SS (horas, minutos e segundos).</span><span class="sxs-lookup"><span data-stu-id="ccfd9-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="ccfd9-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ccfd9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfd9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccfd9-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="ccfd9-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ccfd9-110">Property value</span></span>

<span data-ttu-id="ccfd9-111">Um **System. String** formatado que é a posição atual.</span><span class="sxs-lookup"><span data-stu-id="ccfd9-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccfd9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccfd9-112">Remarks</span></span>

<span data-ttu-id="ccfd9-113">Se o item de mídia tiver menos de uma hora, a posição atual será formatada como MM: SS (minutos e segundos).</span><span class="sxs-lookup"><span data-stu-id="ccfd9-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="ccfd9-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccfd9-114">Examples</span></span>

<span data-ttu-id="ccfd9-115">O exemplo a seguir inicia um temporizador que dispara um evento em intervalos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="ccfd9-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="ccfd9-116">No manipulador de eventos do temporizador, um rótulo é atualizado com o **currentPositionString**.</span><span class="sxs-lookup"><span data-stu-id="ccfd9-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="ccfd9-117">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="ccfd9-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ccfd9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccfd9-118">Requirements</span></span>



| <span data-ttu-id="ccfd9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccfd9-119">Requirement</span></span> | <span data-ttu-id="ccfd9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ccfd9-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccfd9-121">Versão</span><span class="sxs-lookup"><span data-stu-id="ccfd9-121">Version</span></span><br/>   | <span data-ttu-id="ccfd9-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ccfd9-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ccfd9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ccfd9-123">Namespace</span></span><br/> | <span data-ttu-id="ccfd9-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ccfd9-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ccfd9-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="ccfd9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ccfd9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ccfd9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccfd9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccfd9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccfd9-128">**Interface IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ccfd9-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ccfd9-129">**IWMPControls. currentPosition (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ccfd9-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





