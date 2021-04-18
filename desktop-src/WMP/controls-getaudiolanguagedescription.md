---
title: Método Controls. getAudioLanguageDescription
description: O método getAudioLanguageDescription recupera a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- método getAudioLanguageDescription Windows Media Player
- método getAudioLanguageDescription Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760271"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="75c8e-106">Método Controls. getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="75c8e-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="75c8e-107">O método **getAudioLanguageDescription** recupera a descrição para o idioma de áudio correspondente ao índice baseado em um especificado.</span><span class="sxs-lookup"><span data-stu-id="75c8e-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c8e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75c8e-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="75c8e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75c8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c8e-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="75c8e-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c8e-111">**Número** (**longo**) especificando o índice de idioma de áudio baseado em um.</span><span class="sxs-lookup"><span data-stu-id="75c8e-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c8e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75c8e-112">Return value</span></span>

<span data-ttu-id="75c8e-113">Esse método retorna um valor de **cadeia de caracteres** .</span><span class="sxs-lookup"><span data-stu-id="75c8e-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75c8e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="75c8e-114">Remarks</span></span>

<span data-ttu-id="75c8e-115">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.</span><span class="sxs-lookup"><span data-stu-id="75c8e-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="75c8e-116">Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte e, em seguida, acesse um idioma de áudio individualmente usando um índice com base em um.</span><span class="sxs-lookup"><span data-stu-id="75c8e-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="75c8e-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="75c8e-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c8e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c8e-118">Requirements</span></span>



| <span data-ttu-id="75c8e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c8e-119">Requirement</span></span> | <span data-ttu-id="75c8e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="75c8e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75c8e-121">Versão</span><span class="sxs-lookup"><span data-stu-id="75c8e-121">Version</span></span><br/> | <span data-ttu-id="75c8e-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="75c8e-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="75c8e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="75c8e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="75c8e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c8e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75c8e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="75c8e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75c8e-126">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="75c8e-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="75c8e-127">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="75c8e-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="75c8e-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="75c8e-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="75c8e-129">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="75c8e-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="75c8e-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="75c8e-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="75c8e-131">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="75c8e-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





