---
title: Evento AudioLanguageChange do objeto AxWindowsMediaPlayer
description: O evento AudioLanguageChange ocorre quando o idioma de áudio atual é alterado. | Evento AudioLanguageChange do objeto AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Evento AudioLanguageChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784920"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7d9b9-105">Evento AudioLanguageChange do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="7d9b9-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7d9b9-106">O evento AudioLanguageChange ocorre quando o idioma de áudio atual é alterado.</span><span class="sxs-lookup"><span data-stu-id="7d9b9-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="7d9b9-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="7d9b9-107">Event Data</span></span>

<span data-ttu-id="7d9b9-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="7d9b9-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="7d9b9-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, que contém a seguinte propriedade relacionada a este evento.</span><span class="sxs-lookup"><span data-stu-id="7d9b9-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7d9b9-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7d9b9-110">Property</span></span>   | <span data-ttu-id="7d9b9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d9b9-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9b9-112">**langID**</span><span class="sxs-lookup"><span data-stu-id="7d9b9-112">**langID**</span></span> | <span data-ttu-id="7d9b9-113">**System. Int32** Identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="7d9b9-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d9b9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d9b9-114">Remarks</span></span>

<span data-ttu-id="7d9b9-115">Um LCID (identificador de localidade) identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="7d9b9-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d9b9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d9b9-116">Requirements</span></span>



| <span data-ttu-id="7d9b9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d9b9-117">Requirement</span></span> | <span data-ttu-id="7d9b9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7d9b9-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9b9-119">Versão</span><span class="sxs-lookup"><span data-stu-id="7d9b9-119">Version</span></span><br/>   | <span data-ttu-id="7d9b9-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7d9b9-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7d9b9-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d9b9-121">Namespace</span></span><br/> | <span data-ttu-id="7d9b9-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7d9b9-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7d9b9-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="7d9b9-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7d9b9-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7d9b9-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d9b9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d9b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9b9-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7d9b9-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7d9b9-127">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7d9b9-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





