---
title: Evento LibraryConnect do objeto AxWindowsMediaPlayer
description: O evento LibraryConnect ocorre quando uma biblioteca fica disponível.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Evento LibraryConnect do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794519"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="dcaa3-104">Evento LibraryConnect do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="dcaa3-104">LibraryConnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="dcaa3-105">O evento LibraryConnect ocorre quando uma biblioteca fica disponível.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-105">The LibraryConnect event occurs when a library becomes available.</span></span>

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a><span data-ttu-id="dcaa3-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="dcaa3-106">Event Data</span></span>

<span data-ttu-id="dcaa3-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEventHandler**.</span></span> <span data-ttu-id="dcaa3-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryConnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="dcaa3-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dcaa3-109">Property</span></span> | <span data-ttu-id="dcaa3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dcaa3-110">Description</span></span>                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcaa3-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="dcaa3-111">pLibrary</span></span> | <span data-ttu-id="dcaa3-112">**WMPLib. IWMPLibrary** A interface que representa a biblioteca conectada.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-112">**WMPLib.IWMPLibrary** The interface that represents the library that connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcaa3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dcaa3-113">Remarks</span></span>

<span data-ttu-id="dcaa3-114">Esse evento não ocorre para a biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="dcaa3-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcaa3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcaa3-115">Requirements</span></span>



| <span data-ttu-id="dcaa3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcaa3-116">Requirement</span></span> | <span data-ttu-id="dcaa3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dcaa3-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcaa3-118">Versão</span><span class="sxs-lookup"><span data-stu-id="dcaa3-118">Version</span></span><br/>   | <span data-ttu-id="dcaa3-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="dcaa3-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="dcaa3-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="dcaa3-120">Namespace</span></span><br/> | <span data-ttu-id="dcaa3-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="dcaa3-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="dcaa3-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dcaa3-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dcaa3-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcaa3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dcaa3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcaa3-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dcaa3-126">**Interface IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dcaa3-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





