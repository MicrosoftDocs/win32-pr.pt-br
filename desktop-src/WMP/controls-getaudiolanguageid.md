---
title: Método Controls. getAudioLanguageID
description: O método getAudioLanguageID recupera o LCID (identificador de localidade) para um índice de idioma de áudio especificado.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- método getAudioLanguageID Windows Media Player
- método getAudioLanguageID Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780019"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="e71c2-106">Método Controls. getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="e71c2-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="e71c2-107">O método **getAudioLanguageID** recupera o LCID (identificador de localidade) para um índice de idioma de áudio especificado.</span><span class="sxs-lookup"><span data-stu-id="e71c2-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e71c2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e71c2-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="e71c2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e71c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71c2-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e71c2-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71c2-111">**Número** (**longo**) que especifica o índice de idioma de áudio.</span><span class="sxs-lookup"><span data-stu-id="e71c2-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71c2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e71c2-112">Return value</span></span>

<span data-ttu-id="e71c2-113">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="e71c2-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e71c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e71c2-114">Remarks</span></span>

<span data-ttu-id="e71c2-115">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="e71c2-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="e71c2-116">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.</span><span class="sxs-lookup"><span data-stu-id="e71c2-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="e71c2-117">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna o LCID com neutralidade de idioma (0).</span><span class="sxs-lookup"><span data-stu-id="e71c2-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="e71c2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e71c2-118">Requirements</span></span>



| <span data-ttu-id="e71c2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e71c2-119">Requirement</span></span> | <span data-ttu-id="e71c2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e71c2-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e71c2-121">Versão</span><span class="sxs-lookup"><span data-stu-id="e71c2-121">Version</span></span><br/> | <span data-ttu-id="e71c2-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e71c2-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e71c2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e71c2-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e71c2-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e71c2-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e71c2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e71c2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71c2-126">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="e71c2-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e71c2-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="e71c2-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="e71c2-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="e71c2-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="e71c2-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="e71c2-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="e71c2-130">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="e71c2-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="e71c2-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="e71c2-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





