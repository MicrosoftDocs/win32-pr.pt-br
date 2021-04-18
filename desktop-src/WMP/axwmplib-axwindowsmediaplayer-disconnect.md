---
title: Evento Disconnect do objeto AxWindowsMediaPlayer
description: O evento de desconexão é reservado para uso futuro.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Evento Disconnect do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763376"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c239a-104">Evento Disconnect do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c239a-104">Disconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c239a-105">O evento de desconexão é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c239a-105">The Disconnect event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a><span data-ttu-id="c239a-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="c239a-106">Event Data</span></span>

<span data-ttu-id="c239a-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="c239a-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEventHandler**.</span></span> <span data-ttu-id="c239a-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DisconnectEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="c239a-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c239a-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c239a-109">Property</span></span> | <span data-ttu-id="c239a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c239a-110">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="c239a-111">result</span><span class="sxs-lookup"><span data-stu-id="c239a-111">result</span></span>   | <span data-ttu-id="c239a-112">**System. Int32** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="c239a-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c239a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c239a-113">Remarks</span></span>

<span data-ttu-id="c239a-114">Esse evento é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c239a-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="c239a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c239a-115">Requirements</span></span>



| <span data-ttu-id="c239a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c239a-116">Requirement</span></span> | <span data-ttu-id="c239a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c239a-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c239a-118">Versão</span><span class="sxs-lookup"><span data-stu-id="c239a-118">Version</span></span><br/>   | <span data-ttu-id="c239a-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c239a-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c239a-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c239a-120">Namespace</span></span><br/> | <span data-ttu-id="c239a-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c239a-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c239a-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c239a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c239a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c239a-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c239a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c239a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c239a-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c239a-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





