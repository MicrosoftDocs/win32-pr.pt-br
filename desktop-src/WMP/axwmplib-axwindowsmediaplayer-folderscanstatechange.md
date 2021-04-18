---
title: Evento FolderScanStateChange do objeto AxWindowsMediaPlayer
description: O evento FolderScanStateChange ocorre quando uma operação de monitoramento de pasta altera o estado.
ms.assetid: f68829a3-00df-417a-ae78-49dff1e6f09b
keywords:
- Evento FolderScanStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- FolderScanStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3672f16bee5251aa46e6a64a0da983e0f34ec54a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760468"
---
# <a name="folderscanstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="020eb-104">Evento FolderScanStateChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="020eb-104">FolderScanStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="020eb-105">O evento FolderScanStateChange ocorre quando uma operação de monitoramento de pasta altera o estado.</span><span class="sxs-lookup"><span data-stu-id="020eb-105">The FolderScanStateChange event occurs when a folder monitoring operation changes state.</span></span>

``` syntax
[C#]
private void player_FolderScanStateChange(
  object sender,
  _WMPOCXEvents_FolderScanStateChangeEvent e
)

[Visual Basic]
Private Sub player_FolderScanStateChange( 
  sender As Object,  
  e As _WMPOCXEvents_FolderScanStateChangeEvent
) Handles player.FolderScanStateChange
```

## <a name="event-data"></a><span data-ttu-id="020eb-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="020eb-106">Event Data</span></span>

<span data-ttu-id="020eb-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="020eb-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEventHandler**.</span></span> <span data-ttu-id="020eb-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ FolderScanStateChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="020eb-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_FolderScanStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="020eb-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="020eb-109">Property</span></span> | <span data-ttu-id="020eb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="020eb-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="020eb-111">wmpfss</span><span class="sxs-lookup"><span data-stu-id="020eb-111">wmpfss</span></span>   | <span data-ttu-id="020eb-112">Valor de enumeração WMPLib. WMPFolderScanStateThe que indica o novo estado.</span><span class="sxs-lookup"><span data-stu-id="020eb-112">WMPLib.WMPFolderScanStateThe enumeration value that indicates the new state.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="020eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="020eb-113">Requirements</span></span>



| <span data-ttu-id="020eb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="020eb-114">Requirement</span></span> | <span data-ttu-id="020eb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="020eb-115">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020eb-116">Versão</span><span class="sxs-lookup"><span data-stu-id="020eb-116">Version</span></span><br/>   | <span data-ttu-id="020eb-117">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="020eb-117">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="020eb-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="020eb-118">Namespace</span></span><br/> | <span data-ttu-id="020eb-119">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="020eb-119">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="020eb-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="020eb-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="020eb-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="020eb-121"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="020eb-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="020eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="020eb-123">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="020eb-123">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="020eb-124">**WMPFolderScanState**</span><span class="sxs-lookup"><span data-stu-id="020eb-124">**WMPFolderScanState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpfolderscanstate)
</dt> </dl>

 

 





