---
title: Evento CdromMediaChange do objeto AxWindowsMediaPlayer
description: O evento CdromMediaChange ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD. | Evento CdromMediaChange do objeto AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Evento CdromMediaChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788191"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7f192-105">Evento CdromMediaChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7f192-105">CdromMediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7f192-106">O evento **CdromMediaChange** ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="7f192-106">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a><span data-ttu-id="7f192-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="7f192-107">Event Data</span></span>

<span data-ttu-id="7f192-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7f192-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEventHandler**.</span></span> <span data-ttu-id="7f192-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="7f192-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CdromMediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7f192-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7f192-110">Property</span></span> | <span data-ttu-id="7f192-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f192-111">Description</span></span>                                                        |
|----------|--------------------------------------------------------------------|
| <span data-ttu-id="7f192-112">CdromNum</span><span class="sxs-lookup"><span data-stu-id="7f192-112">CdromNum</span></span> | <span data-ttu-id="7f192-113">System. Int32Specifies o índice da unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="7f192-113">System.Int32Specifies the index of the CD or DVD drive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f192-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f192-114">Remarks</span></span>

<span data-ttu-id="7f192-115">O índice da unidade de CD corresponde ao índice de uma interface IWMPCdrom acessível por meio da interface IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="7f192-115">The index of the CD drive corresponds to the index of an IWMPCdrom interface accessible through the IWMPCdromCollection interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f192-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f192-116">Requirements</span></span>



| <span data-ttu-id="7f192-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f192-117">Requirement</span></span> | <span data-ttu-id="7f192-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7f192-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f192-119">Versão</span><span class="sxs-lookup"><span data-stu-id="7f192-119">Version</span></span><br/>   | <span data-ttu-id="7f192-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7f192-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7f192-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f192-121">Namespace</span></span><br/> | <span data-ttu-id="7f192-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7f192-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7f192-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="7f192-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7f192-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7f192-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f192-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f192-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f192-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7f192-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7f192-127">**Interface IWMPCdrom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7f192-127">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7f192-128">**Interface IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7f192-128">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





