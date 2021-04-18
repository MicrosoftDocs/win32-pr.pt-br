---
title: Evento KeyPress do objeto AxWindowsMediaPlayer
description: O evento KeyPress ocorre quando uma tecla é pressionada e liberada. | Evento KeyPress do objeto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800165"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="db8bb-105">Evento KeyPress do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="db8bb-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="db8bb-106">O evento KeyPress ocorre quando uma tecla é pressionada e liberada.</span><span class="sxs-lookup"><span data-stu-id="db8bb-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="db8bb-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="db8bb-107">Event Data</span></span>

<span data-ttu-id="db8bb-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="db8bb-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="db8bb-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="db8bb-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="db8bb-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="db8bb-110">Property</span></span>      | <span data-ttu-id="db8bb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="db8bb-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db8bb-112">**nKeyAscii**</span><span class="sxs-lookup"><span data-stu-id="db8bb-112">**nKeyAscii**</span></span> | <span data-ttu-id="db8bb-113">System. Int16Specifies o código ANSI numérico padrão para o caractere.</span><span class="sxs-lookup"><span data-stu-id="db8bb-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db8bb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="db8bb-114">Remarks</span></span>

<span data-ttu-id="db8bb-115">Esse evento ocorre quando o pressionamento de tecla resulta em qualquer caractere de teclado imprimível, a tecla CTRL combinada com um caractere do alfabeto padrão ou um de alguns caracteres especiais e a tecla ENTER ou Backspace.</span><span class="sxs-lookup"><span data-stu-id="db8bb-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="db8bb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db8bb-116">Requirements</span></span>



| <span data-ttu-id="db8bb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db8bb-117">Requirement</span></span> | <span data-ttu-id="db8bb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db8bb-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db8bb-119">Versão</span><span class="sxs-lookup"><span data-stu-id="db8bb-119">Version</span></span><br/>   | <span data-ttu-id="db8bb-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="db8bb-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="db8bb-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="db8bb-121">Namespace</span></span><br/> | <span data-ttu-id="db8bb-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="db8bb-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="db8bb-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="db8bb-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="db8bb-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="db8bb-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8bb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="db8bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8bb-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="db8bb-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





