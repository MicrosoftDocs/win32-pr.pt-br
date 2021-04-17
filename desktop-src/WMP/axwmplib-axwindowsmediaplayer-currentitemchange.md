---
title: Evento CurrentItemChange do objeto AxWindowsMediaPlayer
description: O evento CurrentItemChange ocorre quando o valor de IWMPControls. currentItem é alterado.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Evento CurrentItemChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763377"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f30ee-104">Evento CurrentItemChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f30ee-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f30ee-105">O evento CurrentItemChange ocorre quando o valor de IWMPControls. **currentItem** é alterado.</span><span class="sxs-lookup"><span data-stu-id="f30ee-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="f30ee-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="f30ee-106">Event Data</span></span>

<span data-ttu-id="f30ee-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="f30ee-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="f30ee-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="f30ee-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f30ee-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f30ee-109">Property</span></span>   | <span data-ttu-id="f30ee-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f30ee-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f30ee-111">pdispMedia</span><span class="sxs-lookup"><span data-stu-id="f30ee-111">pdispMedia</span></span> | <span data-ttu-id="f30ee-112">System. ObjectThe novo item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="f30ee-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="f30ee-113">Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="f30ee-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="f30ee-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f30ee-114">Examples</span></span>

<span data-ttu-id="f30ee-115">O exemplo a seguir demonstra um manipulador de eventos para o evento CurrentItemChange.</span><span class="sxs-lookup"><span data-stu-id="f30ee-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="f30ee-116">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="f30ee-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f30ee-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f30ee-117">Requirements</span></span>



| <span data-ttu-id="f30ee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f30ee-118">Requirement</span></span> | <span data-ttu-id="f30ee-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f30ee-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f30ee-120">Versão</span><span class="sxs-lookup"><span data-stu-id="f30ee-120">Version</span></span><br/>   | <span data-ttu-id="f30ee-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f30ee-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f30ee-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f30ee-122">Namespace</span></span><br/> | <span data-ttu-id="f30ee-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f30ee-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f30ee-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="f30ee-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f30ee-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f30ee-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f30ee-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f30ee-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f30ee-127">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f30ee-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f30ee-128">**IWMPControls. currentItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f30ee-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f30ee-129">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f30ee-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





