---
title: Controls. currentAudioLanguage
description: A propriedade currentAudioLanguage especifica ou recupera o identificador de localidade (LCID) do idioma de áudio para reprodução.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls. currentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758234"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="347dd-104">Controls. currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="347dd-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="347dd-105">A propriedade **currentAudioLanguage** especifica ou recupera o identificador de localidade (LCID) do idioma de áudio para reprodução.</span><span class="sxs-lookup"><span data-stu-id="347dd-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="347dd-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="347dd-106">Possible Values</span></span>

<span data-ttu-id="347dd-107">Essa propriedade é um **número** de leitura/gravação (**longo**).</span><span class="sxs-lookup"><span data-stu-id="347dd-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="347dd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="347dd-108">Remarks</span></span>

<span data-ttu-id="347dd-109">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="347dd-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="347dd-110">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.</span><span class="sxs-lookup"><span data-stu-id="347dd-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="347dd-111">Ao trabalhar com conteúdo de DVD, a especificação de um LCID fará com que a primeira faixa de áudio disponível com a ID de idioma especificada seja selecionada.</span><span class="sxs-lookup"><span data-stu-id="347dd-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="347dd-112">**Windows Media Player 10 Mobile:** Essa propriedade só aceita ou retorna o LCID com neutralidade de idioma (0).</span><span class="sxs-lookup"><span data-stu-id="347dd-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="347dd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="347dd-113">Requirements</span></span>



| <span data-ttu-id="347dd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="347dd-114">Requirement</span></span> | <span data-ttu-id="347dd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="347dd-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="347dd-116">Versão</span><span class="sxs-lookup"><span data-stu-id="347dd-116">Version</span></span><br/> | <span data-ttu-id="347dd-117">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="347dd-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="347dd-118">DLL</span><span class="sxs-lookup"><span data-stu-id="347dd-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="347dd-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="347dd-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="347dd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="347dd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347dd-121">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="347dd-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="347dd-122">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="347dd-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="347dd-123">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="347dd-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="347dd-124">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="347dd-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="347dd-125">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="347dd-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="347dd-126">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="347dd-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





