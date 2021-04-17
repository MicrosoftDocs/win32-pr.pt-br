---
title: Controls. currentAudioLanguageIndex
description: A propriedade currentAudioLanguageIndex especifica ou recupera o índice com base em um que corresponde ao idioma de áudio para reprodução.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Controls. currentAudioLanguageIndex Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789570"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="66b79-104">Controls. currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="66b79-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="66b79-105">A propriedade **currentAudioLanguageIndex** especifica ou recupera o índice com base em um que corresponde ao idioma de áudio para reprodução.</span><span class="sxs-lookup"><span data-stu-id="66b79-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="66b79-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="66b79-106">Possible Values</span></span>

<span data-ttu-id="66b79-107">Essa propriedade é um **número** de leitura/gravação (**longo**).</span><span class="sxs-lookup"><span data-stu-id="66b79-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="66b79-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="66b79-108">Remarks</span></span>

<span data-ttu-id="66b79-109">Para conteúdo baseado no Windows Media, as propriedades e os métodos relacionados à seleção de idioma dão suporte apenas a uma única saída.</span><span class="sxs-lookup"><span data-stu-id="66b79-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="66b79-110">Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte.</span><span class="sxs-lookup"><span data-stu-id="66b79-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="66b79-111">**Windows Media Player 10 Mobile:** Essa propriedade só aceita ou retorna 0.</span><span class="sxs-lookup"><span data-stu-id="66b79-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b79-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66b79-112">Requirements</span></span>



| <span data-ttu-id="66b79-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="66b79-113">Requirement</span></span> | <span data-ttu-id="66b79-114">Valor</span><span class="sxs-lookup"><span data-stu-id="66b79-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66b79-115">Versão</span><span class="sxs-lookup"><span data-stu-id="66b79-115">Version</span></span><br/> | <span data-ttu-id="66b79-116">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="66b79-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="66b79-117">DLL</span><span class="sxs-lookup"><span data-stu-id="66b79-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="66b79-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66b79-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b79-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="66b79-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b79-120">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="66b79-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="66b79-121">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="66b79-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="66b79-122">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="66b79-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="66b79-123">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="66b79-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="66b79-124">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="66b79-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="66b79-125">**Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="66b79-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





