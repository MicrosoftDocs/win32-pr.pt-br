---
title: Evento MediaCollectionAttributeStringChanged do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionAttributeStringChanged ocorre quando um valor de atributo na biblioteca é alterado. | Evento MediaCollectionAttributeStringChanged do objeto AxWindowsMediaPlayer
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Evento MediaCollectionAttributeStringChanged do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761122"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7b50b-105">Evento MediaCollectionAttributeStringChanged do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7b50b-105">MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7b50b-106">O evento MediaCollectionAttributeStringChanged ocorre quando um valor de atributo na biblioteca é alterado.</span><span class="sxs-lookup"><span data-stu-id="7b50b-106">The MediaCollectionAttributeStringChanged event occurs when an attribute value in the library is changed.</span></span>

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a><span data-ttu-id="7b50b-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="7b50b-107">Event Data</span></span>

<span data-ttu-id="7b50b-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7b50b-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEventHandler**.</span></span> <span data-ttu-id="7b50b-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="7b50b-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionAttributeStringChangedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="7b50b-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7b50b-110">Property</span></span>         | <span data-ttu-id="7b50b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b50b-111">Description</span></span>                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b50b-112">bstrAttribName</span><span class="sxs-lookup"><span data-stu-id="7b50b-112">bstrAttribName</span></span>   | <span data-ttu-id="7b50b-113">System. StringSpecifies o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="7b50b-113">System.StringSpecifies the name of the attribute.</span></span> <span data-ttu-id="7b50b-114">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7b50b-114">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span><br/> |
| <span data-ttu-id="7b50b-115">bstrOldAttribVal</span><span class="sxs-lookup"><span data-stu-id="7b50b-115">bstrOldAttribVal</span></span> | <span data-ttu-id="7b50b-116">System. StringSpecifies o valor antigo do atributo.</span><span class="sxs-lookup"><span data-stu-id="7b50b-116">System.StringSpecifies the old value of the attribute.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="7b50b-117">bstrNewAttribVal</span><span class="sxs-lookup"><span data-stu-id="7b50b-117">bstrNewAttribVal</span></span> | <span data-ttu-id="7b50b-118">System. StringSpecifies o novo valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="7b50b-118">System.StringSpecifies the new value of the attribute.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="7b50b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b50b-119">Remarks</span></span>

<span data-ttu-id="7b50b-120">Quando um usuário modifica os metadados da biblioteca, a coleção de mídia é atualizada e esse evento é disparado para cada atributo alterado.</span><span class="sxs-lookup"><span data-stu-id="7b50b-120">When a user modifies library metadata, the media collection is updated and this event fires for each attribute changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b50b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b50b-121">Requirements</span></span>



| <span data-ttu-id="7b50b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b50b-122">Requirement</span></span> | <span data-ttu-id="7b50b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7b50b-123">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b50b-124">Versão</span><span class="sxs-lookup"><span data-stu-id="7b50b-124">Version</span></span><br/>   | <span data-ttu-id="7b50b-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7b50b-125">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7b50b-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b50b-126">Namespace</span></span><br/> | <span data-ttu-id="7b50b-127">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7b50b-127">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7b50b-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="7b50b-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7b50b-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7b50b-129"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b50b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b50b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b50b-131">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7b50b-131">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b50b-132">**AxWindowsMediaPlayer. mediacollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7b50b-132">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b50b-133">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7b50b-133">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





