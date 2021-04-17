---
title: Evento MediaCollectionAttributeStringAdded do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionAttributeStringAdded ocorre quando um valor de atributo é adicionado à biblioteca. | Evento MediaCollectionAttributeStringAdded do objeto AxWindowsMediaPlayer
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Evento MediaCollectionAttributeStringAdded do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811351"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="0f574-105">Evento MediaCollectionAttributeStringAdded do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="0f574-105">MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="0f574-106">O evento MediaCollectionAttributeStringAdded ocorre quando um valor de atributo é adicionado à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0f574-106">The MediaCollectionAttributeStringAdded event occurs when an attribute value is added to the library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a><span data-ttu-id="0f574-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="0f574-107">Event Data</span></span>

<span data-ttu-id="0f574-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="0f574-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEventHandler**.</span></span> <span data-ttu-id="0f574-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="0f574-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringAddedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="0f574-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0f574-110">Property</span></span>           | <span data-ttu-id="0f574-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f574-111">Description</span></span>                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f574-112">**bstrAttribName**</span><span class="sxs-lookup"><span data-stu-id="0f574-112">**bstrAttribName**</span></span> | <span data-ttu-id="0f574-113">System. StringSpecifies o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="0f574-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="0f574-114">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="0f574-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="0f574-115">bstrAttribVal</span><span class="sxs-lookup"><span data-stu-id="0f574-115">bstrAttribVal</span></span>      | <span data-ttu-id="0f574-116">System. StringSpecifies o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="0f574-116">System.StringSpecifies the value of the attribute.</span></span><br/>                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="0f574-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f574-117">Remarks</span></span>

<span data-ttu-id="0f574-118">Quando um item de mídia é adicionado à biblioteca, seus metadados são adicionados à coleção de mídia e esse evento é acionado para cada atributo adicionado.</span><span class="sxs-lookup"><span data-stu-id="0f574-118">When a media item is added to the library, its metadata is added to the media collection and this event is fired for each attribute added.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f574-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f574-119">Requirements</span></span>



| <span data-ttu-id="0f574-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f574-120">Requirement</span></span> | <span data-ttu-id="0f574-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0f574-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f574-122">Versão</span><span class="sxs-lookup"><span data-stu-id="0f574-122">Version</span></span><br/>   | <span data-ttu-id="0f574-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0f574-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="0f574-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f574-124">Namespace</span></span><br/> | <span data-ttu-id="0f574-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="0f574-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="0f574-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="0f574-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0f574-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0f574-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f574-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f574-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f574-129">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0f574-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0f574-130">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0f574-130">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0f574-131">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0f574-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





