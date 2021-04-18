---
title: Evento OpenPlaylistSwitch do objeto AxWindowsMediaPlayer
description: O evento OpenPlaylistSwitch ocorre quando um título em um DVD começa a ser reproduzido. | Evento OpenPlaylistSwitch do objeto AxWindowsMediaPlayer
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Evento OpenPlaylistSwitch do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759743"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="a8876-105">Evento OpenPlaylistSwitch do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="a8876-105">OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="a8876-106">O evento OpenPlaylistSwitch ocorre quando um título em um DVD começa a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="a8876-106">The OpenPlaylistSwitch event occurs when a title on a DVD begins playing.</span></span>

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a><span data-ttu-id="a8876-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="a8876-107">Event Data</span></span>

<span data-ttu-id="a8876-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="a8876-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEventHandler**.</span></span> <span data-ttu-id="a8876-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="a8876-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_OpenPlaylistSwitchEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="a8876-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8876-110">Property</span></span>  | <span data-ttu-id="a8876-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8876-111">Description</span></span>                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8876-112">**pItem**</span><span class="sxs-lookup"><span data-stu-id="a8876-112">**pItem**</span></span> | <span data-ttu-id="a8876-113">System. Objectobject que representa o título.</span><span class="sxs-lookup"><span data-stu-id="a8876-113">System.ObjectObject representing the title.</span></span> <span data-ttu-id="a8876-114">Você pode convertê-lo em uma interface IWMPPlaylist para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="a8876-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8876-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8876-115">Requirements</span></span>



| <span data-ttu-id="a8876-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8876-116">Requirement</span></span> | <span data-ttu-id="a8876-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a8876-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8876-118">Versão</span><span class="sxs-lookup"><span data-stu-id="a8876-118">Version</span></span><br/>   | <span data-ttu-id="a8876-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a8876-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a8876-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8876-120">Namespace</span></span><br/> | <span data-ttu-id="a8876-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a8876-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a8876-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="a8876-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8876-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a8876-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8876-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8876-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8876-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a8876-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8876-126">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a8876-126">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





