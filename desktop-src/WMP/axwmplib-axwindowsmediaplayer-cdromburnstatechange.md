---
title: Evento CdromBurnStateChange do objeto AxWindowsMediaPlayer
description: O evento CdromBurnStateChange ocorre quando uma operação de gravação de CD muda de estado.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromBurnStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811355"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8ba4d-104">Evento CdromBurnStateChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="8ba4d-104">CdromBurnStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8ba4d-105">O evento CdromBurnStateChange ocorre quando uma operação de gravação de CD muda de estado.</span><span class="sxs-lookup"><span data-stu-id="8ba4d-105">The CdromBurnStateChange event occurs when a CD burning operation changes state.</span></span>

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a><span data-ttu-id="8ba4d-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="8ba4d-106">Event Data</span></span>

<span data-ttu-id="8ba4d-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="8ba4d-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEventHandler**.</span></span> <span data-ttu-id="8ba4d-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="8ba4d-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromBurnStateChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="8ba4d-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8ba4d-109">Property</span></span>   | <span data-ttu-id="8ba4d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ba4d-110">Description</span></span>                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba4d-111">pCdromBurn</span><span class="sxs-lookup"><span data-stu-id="8ba4d-111">pCdromBurn</span></span> | <span data-ttu-id="8ba4d-112">A interface WMPLib. IWMPCdromBurnThe que representa a operação de gravação que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="8ba4d-112">WMPLib.IWMPCdromBurnThe interface that represents the burning operation that raised the error.</span></span><br/> |
| <span data-ttu-id="8ba4d-113">wmpbs</span><span class="sxs-lookup"><span data-stu-id="8ba4d-113">wmpbs</span></span>      | <span data-ttu-id="8ba4d-114">Valor de enumeração WMPLib. WMPBurnStateThe que indica o novo estado.</span><span class="sxs-lookup"><span data-stu-id="8ba4d-114">WMPLib.WMPBurnStateThe enumeration value that indicates the new state.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="8ba4d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba4d-115">Requirements</span></span>



| <span data-ttu-id="8ba4d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba4d-116">Requirement</span></span> | <span data-ttu-id="8ba4d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8ba4d-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba4d-118">Versão</span><span class="sxs-lookup"><span data-stu-id="8ba4d-118">Version</span></span><br/>   | <span data-ttu-id="8ba4d-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="8ba4d-119">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="8ba4d-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ba4d-120">Namespace</span></span><br/> | <span data-ttu-id="8ba4d-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8ba4d-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8ba4d-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="8ba4d-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8ba4d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8ba4d-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba4d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ba4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba4d-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8ba4d-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ba4d-126">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8ba4d-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8ba4d-127">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="8ba4d-127">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





