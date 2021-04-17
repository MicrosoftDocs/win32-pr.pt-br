---
title: Evento CdromBurnError do objeto AxWindowsMediaPlayer
description: O evento CdromBurnError ocorre quando um erro genérico ocorre durante uma operação de gravação de CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Evento CdromBurnError do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c27969ea83089b225ba92eb93854fc1dcde9bde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813197"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="047e9-104">Evento CdromBurnError do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="047e9-104">CdromBurnError Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="047e9-105">O evento CdromBurnError ocorre quando um erro genérico ocorre durante uma operação de gravação de CD.</span><span class="sxs-lookup"><span data-stu-id="047e9-105">The CdromBurnError event occurs when a generic error happens during a CD burning operation.</span></span>

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a><span data-ttu-id="047e9-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="047e9-106">Event Data</span></span>

<span data-ttu-id="047e9-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="047e9-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEventHandler**.</span></span> <span data-ttu-id="047e9-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="047e9-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnErrorEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="047e9-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="047e9-109">Property</span></span>   | <span data-ttu-id="047e9-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="047e9-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047e9-111">hrError</span><span class="sxs-lookup"><span data-stu-id="047e9-111">hrError</span></span>    | <span data-ttu-id="047e9-112">**System. Int32** O erro que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="047e9-112">**System.Int32** The error that raised the event.</span></span><br/>                                               |
| <span data-ttu-id="047e9-113">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="047e9-113">pCdromBurn</span></span> | <span data-ttu-id="047e9-114">A interface WMPLib. IWMPCdromBurnThe que representa a operação de gravação que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="047e9-114">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="047e9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="047e9-115">Remarks</span></span>

<span data-ttu-id="047e9-116">Para capturar erros de mídia específicos, manipule o AxWMPLib. \_ \_Evento WMPOCXEvents CdromBurnMediaError.</span><span class="sxs-lookup"><span data-stu-id="047e9-116">To capture media specific errors, handle the AxWMPLib.\_WMPOCXEvents\_CdromBurnMediaError event.</span></span>

## <a name="requirements"></a><span data-ttu-id="047e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="047e9-117">Requirements</span></span>



| <span data-ttu-id="047e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="047e9-118">Requirement</span></span> | <span data-ttu-id="047e9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="047e9-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047e9-120">Versão</span><span class="sxs-lookup"><span data-stu-id="047e9-120">Version</span></span><br/>   | <span data-ttu-id="047e9-121">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="047e9-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="047e9-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="047e9-122">Namespace</span></span><br/> | <span data-ttu-id="047e9-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="047e9-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="047e9-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="047e9-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="047e9-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="047e9-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="047e9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="047e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047e9-127">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="047e9-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="047e9-128">**Evento AxWindowsMediaPlayer. CdromBurnMediaError (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="047e9-128">**AxWindowsMediaPlayer.CdromBurnMediaError Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[<span data-ttu-id="047e9-129">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="047e9-129">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





