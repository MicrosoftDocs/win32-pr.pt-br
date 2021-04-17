---
title: Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionAttributeStringRemoved ocorre quando um valor de atributo é removido da biblioteca. | Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784916"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="382c2-105">Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="382c2-105">MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="382c2-106">O evento MediaCollectionAttributeStringRemoved ocorre quando um valor de atributo é removido da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="382c2-106">The MediaCollectionAttributeStringRemoved event occurs when an attribute value is removed from the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a><span data-ttu-id="382c2-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="382c2-107">Event Data</span></span>

<span data-ttu-id="382c2-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="382c2-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEventHandler**.</span></span> <span data-ttu-id="382c2-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="382c2-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringRemovedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="382c2-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="382c2-110">Property</span></span>           | <span data-ttu-id="382c2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="382c2-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382c2-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="382c2-112">**bstrAttribName**</span></span> | <span data-ttu-id="382c2-113">System. StringSpecifies o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="382c2-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="382c2-114">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="382c2-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="382c2-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="382c2-115">bstrAttribVal</span></span>      | <span data-ttu-id="382c2-116">System. StringSpecifies o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="382c2-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="382c2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="382c2-117">Remarks</span></span>

<span data-ttu-id="382c2-118">Quando um item de mídia é removido da biblioteca, seus metadados são removidos do **mediacollection** e esse evento é acionado para cada atributo removido.</span><span class="sxs-lookup"><span data-stu-id="382c2-118">When a media item is removed from the library, its metadata is removed from the **MediaCollection** and this event is fired for each attribute removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="382c2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="382c2-119">Requirements</span></span>



| <span data-ttu-id="382c2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="382c2-120">Requirement</span></span> | <span data-ttu-id="382c2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="382c2-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382c2-122">Versão</span><span class="sxs-lookup"><span data-stu-id="382c2-122">Version</span></span><br/>   | <span data-ttu-id="382c2-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="382c2-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="382c2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="382c2-124">Namespace</span></span><br/> | <span data-ttu-id="382c2-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="382c2-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="382c2-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="382c2-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="382c2-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="382c2-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="382c2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="382c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382c2-129">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="382c2-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="382c2-130">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="382c2-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="382c2-131">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="382c2-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





