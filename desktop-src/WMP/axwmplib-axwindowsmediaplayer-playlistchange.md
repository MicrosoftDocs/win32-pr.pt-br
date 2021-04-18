---
title: Evento PlaylistChange do objeto AxWindowsMediaPlayer
description: O evento PlaylistChange ocorre quando uma lista de reprodução é alterada. | Evento PlaylistChange do objeto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781280"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="df164-105">Evento PlaylistChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="df164-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="df164-106">O evento PlaylistChange ocorre quando uma lista de reprodução é alterada.</span><span class="sxs-lookup"><span data-stu-id="df164-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="df164-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="df164-107">Event Data</span></span>

<span data-ttu-id="df164-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="df164-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="df164-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="df164-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="df164-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="df164-110">Property</span></span>     | <span data-ttu-id="df164-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="df164-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df164-112">**playlist**</span><span class="sxs-lookup"><span data-stu-id="df164-112">**playlist**</span></span> | <span data-ttu-id="df164-113">Objeto System. ObjectThe que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="df164-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="df164-114">Você pode convertê-lo em uma interface IWMPPlaylist para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="df164-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="df164-115">**change**</span><span class="sxs-lookup"><span data-stu-id="df164-115">**change**</span></span>   | <span data-ttu-id="df164-116">Valor de enumeração WMPLib. WMPPlaylistChangeEventTypeAn que indica o tipo de alteração ocorrida na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="df164-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df164-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df164-117">Requirements</span></span>



| <span data-ttu-id="df164-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df164-118">Requirement</span></span> | <span data-ttu-id="df164-119">Valor</span><span class="sxs-lookup"><span data-stu-id="df164-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df164-120">Versão</span><span class="sxs-lookup"><span data-stu-id="df164-120">Version</span></span><br/>   | <span data-ttu-id="df164-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="df164-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="df164-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="df164-122">Namespace</span></span><br/> | <span data-ttu-id="df164-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="df164-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="df164-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="df164-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="df164-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="df164-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df164-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="df164-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df164-127">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="df164-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="df164-128">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="df164-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





