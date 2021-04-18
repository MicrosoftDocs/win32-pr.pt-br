---
title: Evento CdromBurnMediaError do objeto AxWindowsMediaPlayer
description: O evento CdromBurnMediaError ocorre quando um erro ocorre durante a gravação de um item de mídia individual em um CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromBurnMediaError do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d9fac8902fe8700171d2c909e8140c74c8cc3c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789584"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="affe7-104">Evento CdromBurnMediaError do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="affe7-104">CdromBurnMediaError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="affe7-105">O evento CdromBurnMediaError ocorre quando um erro ocorre durante a gravação de um item de mídia individual em um CD.</span><span class="sxs-lookup"><span data-stu-id="affe7-105">The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.</span></span>

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a><span data-ttu-id="affe7-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="affe7-106">Event Data</span></span>

<span data-ttu-id="affe7-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="affe7-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEventHandler**.</span></span> <span data-ttu-id="affe7-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnMediaErrorEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="affe7-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="affe7-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="affe7-109">Property</span></span>   | <span data-ttu-id="affe7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="affe7-110">Description</span></span>                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="affe7-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="affe7-111">pCdromBurn</span></span> | <span data-ttu-id="affe7-112">A interface WMPLib. IWMPCdromBurnThe que representa a operação de gravação que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="affe7-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/>               |
| <span data-ttu-id="affe7-113">pMedia</span><span class="sxs-lookup"><span data-stu-id="affe7-113">pMedia</span></span>     | <span data-ttu-id="affe7-114">O item de mídia System. ObjectThe que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="affe7-114">System.ObjectThe media item that raised the error.</span></span> <span data-ttu-id="affe7-115">Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.</span><span class="sxs-lookup"><span data-stu-id="affe7-115">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="affe7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="affe7-116">Remarks</span></span>

<span data-ttu-id="affe7-117">Para capturar erros genéricos, manipule o AxWMPLib. \_ \_Evento WMPOCXEvents CdromBurnError.</span><span class="sxs-lookup"><span data-stu-id="affe7-117">To capture generic errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="affe7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="affe7-118">Requirements</span></span>



| <span data-ttu-id="affe7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="affe7-119">Requirement</span></span> | <span data-ttu-id="affe7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="affe7-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="affe7-121">Versão</span><span class="sxs-lookup"><span data-stu-id="affe7-121">Version</span></span><br/>   | <span data-ttu-id="affe7-122">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="affe7-122">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="affe7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="affe7-123">Namespace</span></span><br/> | <span data-ttu-id="affe7-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="affe7-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="affe7-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="affe7-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="affe7-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="affe7-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="affe7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="affe7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="affe7-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="affe7-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="affe7-129">**Evento AxWindowsMediaPlayer. CdromBurnError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="affe7-129">**AxWindowsMediaPlayer.CdromBurnError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[<span data-ttu-id="affe7-130">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="affe7-130">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="affe7-131">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="affe7-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





