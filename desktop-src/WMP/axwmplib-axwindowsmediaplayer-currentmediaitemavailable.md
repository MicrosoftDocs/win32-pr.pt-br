---
title: Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer
description: O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráfico no item de mídia atual fica disponível. | Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759749"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="18adc-105">Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="18adc-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="18adc-106">O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráfico no item de mídia atual fica disponível.</span><span class="sxs-lookup"><span data-stu-id="18adc-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="18adc-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="18adc-107">Event Data</span></span>

<span data-ttu-id="18adc-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="18adc-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="18adc-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="18adc-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="18adc-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="18adc-110">Property</span></span>     | <span data-ttu-id="18adc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="18adc-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="18adc-112">bstrItemName</span><span class="sxs-lookup"><span data-stu-id="18adc-112">bstrItemName</span></span> | <span data-ttu-id="18adc-113">System. StringThe nome do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="18adc-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18adc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="18adc-114">Remarks</span></span>

<span data-ttu-id="18adc-115">Como a reprodução pode começar antes que um item de mídia seja totalmente baixado, todos os gráficos de metadados contidos no item de mídia (como arte de capa do álbum) podem não estar disponíveis quando começam a ser reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="18adc-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="18adc-116">Esse evento alerta quando um item gráfico de metadados termina o download.</span><span class="sxs-lookup"><span data-stu-id="18adc-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="18adc-117">Em seguida, você pode recuperar a interface **IWMPMedia** passando o valor de **BstrItemName** para o *IWMPMediaCollection*. método **getByName** , depois do qual você pode acessar o item gráfico de metadados usando *IWMPMedia3*. **getItemInfoByType** e especificando o **WM/Picture** para o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="18adc-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="18adc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18adc-118">Requirements</span></span>



| <span data-ttu-id="18adc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="18adc-119">Requirement</span></span> | <span data-ttu-id="18adc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="18adc-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18adc-121">Versão</span><span class="sxs-lookup"><span data-stu-id="18adc-121">Version</span></span><br/>   | <span data-ttu-id="18adc-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="18adc-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="18adc-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="18adc-123">Namespace</span></span><br/> | <span data-ttu-id="18adc-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="18adc-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="18adc-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="18adc-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18adc-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18adc-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18adc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="18adc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18adc-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18adc-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18adc-129">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18adc-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18adc-130">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18adc-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18adc-131">**IWMPMediaCollection. getByName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18adc-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





