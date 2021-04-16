---
title: Evento buffer do objeto AxWindowsMediaPlayer
description: O evento de buffer ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download. | Evento buffer do objeto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento buffer do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794525"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7b98a-105">Evento buffer do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7b98a-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7b98a-106">O evento de buffer ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download.</span><span class="sxs-lookup"><span data-stu-id="7b98a-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="7b98a-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="7b98a-107">Event Data</span></span>

<span data-ttu-id="7b98a-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7b98a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="7b98a-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="7b98a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7b98a-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7b98a-110">Property</span></span> | <span data-ttu-id="7b98a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b98a-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b98a-112">Iniciar</span><span class="sxs-lookup"><span data-stu-id="7b98a-112">Start</span></span>    | <span data-ttu-id="7b98a-113">System. BooleanSpecifies se o armazenamento em buffer foi iniciado ou encerrado.</span><span class="sxs-lookup"><span data-stu-id="7b98a-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="7b98a-114">Um valor true indica que ele foi iniciado; um valor false indica que ele terminou.</span><span class="sxs-lookup"><span data-stu-id="7b98a-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7b98a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b98a-115">Remarks</span></span>

<span data-ttu-id="7b98a-116">Use esse evento para determinar quando o buffer ou o download é iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="7b98a-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="7b98a-117">Você pode usar o mesmo bloco de eventos para ambos os casos e testar o *IWMPNetwork*. **bufferingProgress** e *IWMPNetwork*. **downloadProgress** para determinar se o Windows Media Player está atualmente armazenando em buffer ou baixando conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7b98a-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b98a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b98a-118">Requirements</span></span>



| <span data-ttu-id="7b98a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b98a-119">Requirement</span></span> | <span data-ttu-id="7b98a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b98a-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b98a-121">Versão</span><span class="sxs-lookup"><span data-stu-id="7b98a-121">Version</span></span><br/>   | <span data-ttu-id="7b98a-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7b98a-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7b98a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b98a-123">Namespace</span></span><br/> | <span data-ttu-id="7b98a-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7b98a-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7b98a-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="7b98a-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7b98a-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7b98a-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b98a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b98a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b98a-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7b98a-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b98a-129">**IWMPNetwork. bufferingProgress (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7b98a-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7b98a-130">**IWMPNetwork. downloadProgress (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7b98a-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





