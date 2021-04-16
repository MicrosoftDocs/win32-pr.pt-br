---
title: Propriedade IWMPControls3 currentAudioLanguage
description: A propriedade currentAudioLanguage Obtém ou define o identificador de localidade (LCID) do idioma de áudio para reprodução.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- Propriedade currentAudioLanguage Windows Media Player
- Propriedade currentAudioLanguage Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765749"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="9a927-106">Propriedade IWMPControls3:: currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="9a927-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="9a927-107">A propriedade **currentAudioLanguage** Obtém ou define o identificador de localidade (LCID) do idioma de áudio para reprodução.</span><span class="sxs-lookup"><span data-stu-id="9a927-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a927-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a927-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9a927-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9a927-109">Property value</span></span>

<span data-ttu-id="9a927-110">Um **System. Int32** que é o LCID do idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="9a927-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a927-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a927-111">Remarks</span></span>

<span data-ttu-id="9a927-112">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="9a927-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="9a927-113">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.</span><span class="sxs-lookup"><span data-stu-id="9a927-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="9a927-114">Ao trabalhar com conteúdo de DVD, a especificação de um LCID fará com que a primeira faixa de áudio disponível com a ID de idioma especificada seja selecionada.</span><span class="sxs-lookup"><span data-stu-id="9a927-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a927-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a927-115">Requirements</span></span>



| <span data-ttu-id="9a927-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a927-116">Requirement</span></span> | <span data-ttu-id="9a927-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9a927-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a927-118">Versão</span><span class="sxs-lookup"><span data-stu-id="9a927-118">Version</span></span><br/>   | <span data-ttu-id="9a927-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="9a927-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9a927-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a927-120">Namespace</span></span><br/> | <span data-ttu-id="9a927-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9a927-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9a927-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="9a927-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9a927-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9a927-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a927-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a927-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a927-125">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a927-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a927-126">**IWMPControls3. audioLanguageCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a927-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a927-127">**IWMPControls3. currentAudioLanguageIndex (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a927-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a927-128">**IWMPControls3. getAudioLanguageDescription (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a927-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a927-129">**IWMPControls3. getAudioLanguageID (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a927-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9a927-130">**IWMPControls3. getLanguageName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="9a927-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





