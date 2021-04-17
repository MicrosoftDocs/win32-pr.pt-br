---
title: Evento de aviso do objeto AxWindowsMediaPlayer
description: O evento de aviso é reservado para uso futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento de aviso do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761120"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="deb58-104">Evento de aviso do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="deb58-104">Warning Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="deb58-105">O evento de aviso é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="deb58-105">The Warning event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a><span data-ttu-id="deb58-106">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="deb58-106">Event Data</span></span>

<span data-ttu-id="deb58-107">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="deb58-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_WarningEventHandler**.</span></span> <span data-ttu-id="deb58-108">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="deb58-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_WarningEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="deb58-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="deb58-109">Property</span></span>    | <span data-ttu-id="deb58-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="deb58-110">Description</span></span>                                |
|-------------|--------------------------------------------|
| <span data-ttu-id="deb58-111">aviso de</span><span class="sxs-lookup"><span data-stu-id="deb58-111">warningType</span></span> | <span data-ttu-id="deb58-112">**System. Int32** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="deb58-112">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="deb58-113">param</span><span class="sxs-lookup"><span data-stu-id="deb58-113">param</span></span>       | <span data-ttu-id="deb58-114">**System. Int32** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="deb58-114">**System.Int32** Not supported.</span></span><br/>  |
| <span data-ttu-id="deb58-115">descrição</span><span class="sxs-lookup"><span data-stu-id="deb58-115">description</span></span> | <span data-ttu-id="deb58-116">**System. String** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="deb58-116">**System.String** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="deb58-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="deb58-117">Remarks</span></span>

<span data-ttu-id="deb58-118">Esse evento é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="deb58-118">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb58-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deb58-119">Requirements</span></span>



| <span data-ttu-id="deb58-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb58-120">Requirement</span></span> | <span data-ttu-id="deb58-121">Valor</span><span class="sxs-lookup"><span data-stu-id="deb58-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb58-122">Versão</span><span class="sxs-lookup"><span data-stu-id="deb58-122">Version</span></span><br/>   | <span data-ttu-id="deb58-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="deb58-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="deb58-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="deb58-124">Namespace</span></span><br/> | <span data-ttu-id="deb58-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="deb58-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="deb58-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="deb58-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="deb58-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="deb58-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deb58-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="deb58-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb58-129">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="deb58-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





