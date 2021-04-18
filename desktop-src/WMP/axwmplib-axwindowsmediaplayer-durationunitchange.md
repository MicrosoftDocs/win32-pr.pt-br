---
title: Evento DurationUnitChange do objeto AxWindowsMediaPlayer
description: O evento DurationUnitChange é reservado para uso futuro.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Evento DurationUnitChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813385"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f1b6f-104">Evento DurationUnitChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f1b6f-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f1b6f-105">O evento DurationUnitChange é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f1b6f-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="f1b6f-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="f1b6f-106">Event Data</span></span>

<span data-ttu-id="f1b6f-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="f1b6f-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="f1b6f-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="f1b6f-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f1b6f-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f1b6f-109">Property</span></span>        | <span data-ttu-id="f1b6f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1b6f-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="f1b6f-111">newDurationUnit</span><span class="sxs-lookup"><span data-stu-id="f1b6f-111">newDurationUnit</span></span> | <span data-ttu-id="f1b6f-112">**System. Int32** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="f1b6f-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1b6f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1b6f-113">Remarks</span></span>

<span data-ttu-id="f1b6f-114">Esse evento é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f1b6f-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b6f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b6f-115">Requirements</span></span>



| <span data-ttu-id="f1b6f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b6f-116">Requirement</span></span> | <span data-ttu-id="f1b6f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f1b6f-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b6f-118">Versão</span><span class="sxs-lookup"><span data-stu-id="f1b6f-118">Version</span></span><br/>   | <span data-ttu-id="f1b6f-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f1b6f-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f1b6f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1b6f-120">Namespace</span></span><br/> | <span data-ttu-id="f1b6f-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f1b6f-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f1b6f-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="f1b6f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f1b6f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f1b6f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b6f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1b6f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b6f-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f1b6f-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





