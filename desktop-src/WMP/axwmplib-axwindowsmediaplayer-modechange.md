---
title: Evento ModeChange do objeto AxWindowsMediaPlayer
description: O evento ModeChange ocorre quando um modo do Windows Media Player é alterado. | Evento ModeChange do objeto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813381"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="174d9-105">Evento ModeChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="174d9-105">ModeChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="174d9-106">O evento ModeChange ocorre quando um modo do Windows Media Player é alterado.</span><span class="sxs-lookup"><span data-stu-id="174d9-106">The ModeChange event occurs when a mode of Windows Media Player is changed.</span></span>

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a><span data-ttu-id="174d9-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="174d9-107">Event Data</span></span>

<span data-ttu-id="174d9-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="174d9-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEventHandler**.</span></span> <span data-ttu-id="174d9-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="174d9-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ModeChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="174d9-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="174d9-110">Property</span></span> | <span data-ttu-id="174d9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="174d9-111">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="174d9-112">modeName</span><span class="sxs-lookup"><span data-stu-id="174d9-112">modeName</span></span> | <span data-ttu-id="174d9-113">System. StringIndicates o modo que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="174d9-113">System.StringIndicates the mode that was changed.</span></span> <span data-ttu-id="174d9-114">Para obter os valores possíveis, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="174d9-114">For possible values, see Remarks.</span></span><br/> |
| <span data-ttu-id="174d9-115">newValue</span><span class="sxs-lookup"><span data-stu-id="174d9-115">newValue</span></span> | <span data-ttu-id="174d9-116">System. BooleanIndicates o novo estado do modo especificado.</span><span class="sxs-lookup"><span data-stu-id="174d9-116">System.BooleanIndicates the new state of the specified mode.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="174d9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="174d9-117">Remarks</span></span>

<span data-ttu-id="174d9-118">A tabela a seguir mostra os valores possíveis para a propriedade modeName.</span><span class="sxs-lookup"><span data-stu-id="174d9-118">The following table shows the possible values for the modeName property.</span></span>



| <span data-ttu-id="174d9-119">String</span><span class="sxs-lookup"><span data-stu-id="174d9-119">String</span></span>  | <span data-ttu-id="174d9-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="174d9-120">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="174d9-121">ordem aleatória</span><span class="sxs-lookup"><span data-stu-id="174d9-121">shuffle</span></span> | <span data-ttu-id="174d9-122">As faixas são reproduzidas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="174d9-122">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="174d9-123">loop</span><span class="sxs-lookup"><span data-stu-id="174d9-123">loop</span></span>    | <span data-ttu-id="174d9-124">A sequência inteira de faixas é reproduzida repetidamente.</span><span class="sxs-lookup"><span data-stu-id="174d9-124">The entire sequence of tracks is played repeatedly.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="174d9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="174d9-125">Requirements</span></span>



| <span data-ttu-id="174d9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="174d9-126">Requirement</span></span> | <span data-ttu-id="174d9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="174d9-127">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="174d9-128">Versão</span><span class="sxs-lookup"><span data-stu-id="174d9-128">Version</span></span><br/>   | <span data-ttu-id="174d9-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="174d9-129">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="174d9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="174d9-130">Namespace</span></span><br/> | <span data-ttu-id="174d9-131">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="174d9-131">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="174d9-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="174d9-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="174d9-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="174d9-133"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="174d9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="174d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="174d9-135">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="174d9-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="174d9-136">**IWMPSettings. GetMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="174d9-136">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="174d9-137">**IWMPSettings. setMode (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="174d9-137">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





