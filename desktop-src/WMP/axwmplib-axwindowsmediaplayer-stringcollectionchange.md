---
title: Evento StringCollectionChange do objeto AxWindowsMediaPlayer
description: O evento StringCollectionChange ocorre quando uma coleção de cadeia de caracteres é alterada. | Evento StringCollectionChange do objeto AxWindowsMediaPlayer
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Evento StringCollectionChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813380"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="4fd14-105">Evento StringCollectionChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="4fd14-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="4fd14-106">O evento StringCollectionChange ocorre quando uma coleção de cadeia de caracteres é alterada.</span><span class="sxs-lookup"><span data-stu-id="4fd14-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="4fd14-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="4fd14-107">Event Data</span></span>

<span data-ttu-id="4fd14-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="4fd14-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="4fd14-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ StringCollectionChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="4fd14-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="4fd14-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4fd14-110">Property</span></span>              | <span data-ttu-id="4fd14-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fd14-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd14-112">pdispStringCollection</span><span class="sxs-lookup"><span data-stu-id="4fd14-112">pdispStringCollection</span></span> | <span data-ttu-id="4fd14-113">Item de coleção de cadeia de caracteres System. ObjectThe que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4fd14-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="4fd14-114">Você pode convertê-lo em uma interface IWMPStringCollection para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="4fd14-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="4fd14-115">lCollectionIndex</span><span class="sxs-lookup"><span data-stu-id="4fd14-115">lCollectionIndex</span></span>      | <span data-ttu-id="4fd14-116">O índice System. Int32The do item de coleção de cadeia de caracteres que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4fd14-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="4fd14-117">alterar</span><span class="sxs-lookup"><span data-stu-id="4fd14-117">change</span></span>                | <span data-ttu-id="4fd14-118">Valor de enumeração WMPLib. WMPStringCollectionChangeEventTypeAn que indica o tipo de alteração ocorrida.</span><span class="sxs-lookup"><span data-stu-id="4fd14-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="4fd14-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fd14-119">Requirements</span></span>



| <span data-ttu-id="4fd14-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fd14-120">Requirement</span></span> | <span data-ttu-id="4fd14-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4fd14-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd14-122">Versão</span><span class="sxs-lookup"><span data-stu-id="4fd14-122">Version</span></span><br/>   | <span data-ttu-id="4fd14-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="4fd14-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4fd14-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4fd14-124">Namespace</span></span><br/> | <span data-ttu-id="4fd14-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4fd14-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4fd14-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="4fd14-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4fd14-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4fd14-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fd14-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fd14-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd14-129">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4fd14-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4fd14-130">**Interface IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="4fd14-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4fd14-131">**WMPStringCollectionChangeEventType**</span><span class="sxs-lookup"><span data-stu-id="4fd14-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





