---
title: Evento LibraryDisconnect do objeto AxWindowsMediaPlayer
description: O evento LibraryDisconnect ocorre quando uma biblioteca não está mais disponível.
ms.assetid: 053d914a-dcd9-4fd6-a789-10c26147d08a
keywords:
- Evento LibraryDisconnect do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- LibraryDisconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058c75ed0d1173661b16baa6e4b4394ba4d0c38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794518"
---
# <a name="librarydisconnect-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="c3351-104">Evento LibraryDisconnect do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="c3351-104">LibraryDisconnect Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="c3351-105">O evento LibraryDisconnect ocorre quando uma biblioteca não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="c3351-105">The LibraryDisconnect event occurs when a library is no longer available.</span></span>

``` syntax
[C#]
private void player_LibraryDisconnect(
  object sender,
  _WMPOCXEvents_LibraryDisconnectEvent e
)

[Visual Basic]
Private Sub player_LibraryDisconnect(  
   sender As Object,  
   e As _WMPOCXEvents_LibraryDisconnectEvent
) Handles player.LibraryDisconnect
```

## <a name="event-data"></a><span data-ttu-id="c3351-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="c3351-106">Event Data</span></span>

<span data-ttu-id="c3351-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="c3351-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEventHandler**.</span></span> <span data-ttu-id="c3351-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryDisconnectEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="c3351-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_LibraryDisconnectEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="c3351-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c3351-109">Property</span></span> | <span data-ttu-id="c3351-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3351-110">Description</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3351-111">pLibrary</span><span class="sxs-lookup"><span data-stu-id="c3351-111">pLibrary</span></span> | <span data-ttu-id="c3351-112">**WMPLib. IWMPLibrary** A interface que representa a biblioteca desconectada.</span><span class="sxs-lookup"><span data-stu-id="c3351-112">**WMPLib.IWMPLibrary** The interface that represents the library that disconnected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3351-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3351-113">Remarks</span></span>

<span data-ttu-id="c3351-114">Esse evento não ocorre para a biblioteca local.</span><span class="sxs-lookup"><span data-stu-id="c3351-114">This event does not occur for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3351-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3351-115">Requirements</span></span>



| <span data-ttu-id="c3351-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3351-116">Requirement</span></span> | <span data-ttu-id="c3351-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c3351-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3351-118">Versão</span><span class="sxs-lookup"><span data-stu-id="c3351-118">Version</span></span><br/>   | <span data-ttu-id="c3351-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="c3351-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="c3351-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3351-120">Namespace</span></span><br/> | <span data-ttu-id="c3351-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3351-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c3351-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3351-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3351-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3351-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3351-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3351-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3351-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3351-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3351-126">**Interface IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c3351-126">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





