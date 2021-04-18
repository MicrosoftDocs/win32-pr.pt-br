---
title: Evento CdromRipStateChange do objeto AxWindowsMediaPlayer
description: O evento CdromRipStateChange ocorre quando uma operação de cópia de CD muda de estado.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Evento CdromRipStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760471"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9130f-104">Evento CdromRipStateChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9130f-104">CdromRipStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9130f-105">O evento CdromRipStateChange ocorre quando uma operação de cópia de CD muda de estado.</span><span class="sxs-lookup"><span data-stu-id="9130f-105">The CdromRipStateChange event occurs when a CD ripping operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a><span data-ttu-id="9130f-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="9130f-106">Event Data</span></span>

<span data-ttu-id="9130f-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="9130f-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEventHandler**.</span></span> <span data-ttu-id="9130f-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="9130f-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromRipStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="9130f-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9130f-109">Property</span></span>  | <span data-ttu-id="9130f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9130f-110">Description</span></span>                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9130f-111">pCdromRip</span><span class="sxs-lookup"><span data-stu-id="9130f-111">pCdromRip</span></span> | <span data-ttu-id="9130f-112">A interface WMPLib. IWMPCdromRipThe que representa a operação de cópia de CDs que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="9130f-112">WMPLib.IWMPCdromRipThe interface that represents the ripping operation that raised the error.</span></span><br/> |
| <span data-ttu-id="9130f-113">wmprs</span><span class="sxs-lookup"><span data-stu-id="9130f-113">wmprs</span></span>     | <span data-ttu-id="9130f-114">Valor de enumeração WMPLib. WMPRipStateThe que indica o novo estado.</span><span class="sxs-lookup"><span data-stu-id="9130f-114">WMPLib.WMPRipStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="9130f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9130f-115">Requirements</span></span>



| <span data-ttu-id="9130f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9130f-116">Requirement</span></span> | <span data-ttu-id="9130f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9130f-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9130f-118">Versão</span><span class="sxs-lookup"><span data-stu-id="9130f-118">Version</span></span><br/>   | <span data-ttu-id="9130f-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="9130f-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="9130f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="9130f-120">Namespace</span></span><br/> | <span data-ttu-id="9130f-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9130f-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9130f-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="9130f-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9130f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9130f-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9130f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9130f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9130f-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9130f-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9130f-126">**Interface IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9130f-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9130f-127">**WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="9130f-127">**WMPRipState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





