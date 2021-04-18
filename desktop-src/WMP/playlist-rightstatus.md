---
title: PLAYLIST. rightStatus
description: O atributo rightStatus especifica ou recupera o texto de status que é exibido no lado direito e no final do elemento PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST. rightStatus Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796240"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="b35bd-104">PLAYLIST. rightStatus</span><span class="sxs-lookup"><span data-stu-id="b35bd-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="b35bd-105">O atributo **rightStatus** especifica ou recupera o texto de status que é exibido no lado direito e no final do elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="b35bd-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="b35bd-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b35bd-106">Possible Values</span></span>

<span data-ttu-id="b35bd-107">Este atributo é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b35bd-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b35bd-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b35bd-108">Remarks</span></span>

<span data-ttu-id="b35bd-109">Esse atributo pode combinar qualquer texto com palavras-chave específicas que exibirão as informações desejadas, como a duração total da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="b35bd-110">As palavras-chave são circundadas por símbolos percentuais (%) para mantê-los distintos do texto comum.</span><span class="sxs-lookup"><span data-stu-id="b35bd-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="b35bd-111">As palavras-chave a seguir podem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="b35bd-111">The following keywords can be used.</span></span>



| <span data-ttu-id="b35bd-112">Palavra-chave</span><span class="sxs-lookup"><span data-stu-id="b35bd-112">Keyword</span></span>               | <span data-ttu-id="b35bd-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="b35bd-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35bd-114">count</span><span class="sxs-lookup"><span data-stu-id="b35bd-114">count</span></span>                 | <span data-ttu-id="b35bd-115">Número de itens na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="b35bd-116">tamanho</span><span class="sxs-lookup"><span data-stu-id="b35bd-116">size</span></span>                  | <span data-ttu-id="b35bd-117">Tamanho total da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="b35bd-118">duration</span><span class="sxs-lookup"><span data-stu-id="b35bd-118">duration</span></span>              | <span data-ttu-id="b35bd-119">Duração total da playlist.</span><span class="sxs-lookup"><span data-stu-id="b35bd-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="b35bd-120">*XXX*</span><span class="sxs-lookup"><span data-stu-id="b35bd-120">*XXX*</span></span>                 | <span data-ttu-id="b35bd-121">Faz um **getItemInfo** na playlist com *xxx* ser o item a receber.</span><span class="sxs-lookup"><span data-stu-id="b35bd-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="b35bd-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="b35bd-122">SelectedSize</span></span>          | <span data-ttu-id="b35bd-123">Tamanho total das entradas selecionadas na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="b35bd-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="b35bd-124">SelectedCount</span></span>         | <span data-ttu-id="b35bd-125">Número total de entradas selecionadas na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="b35bd-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="b35bd-126">SelectedDuration</span></span>      | <span data-ttu-id="b35bd-127">Duração total das entradas selecionadas na playlist.</span><span class="sxs-lookup"><span data-stu-id="b35bd-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="b35bd-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="b35bd-128">CheckedCount</span></span>          | <span data-ttu-id="b35bd-129">Número total de faixas verificadas na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="b35bd-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="b35bd-130">CheckedDuration</span></span>       | <span data-ttu-id="b35bd-131">Duração total das faixas verificadas na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="b35bd-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="b35bd-132">CheckedSize</span></span>           | <span data-ttu-id="b35bd-133">Tamanho total das faixas marcadas na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b35bd-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="b35bd-134">Duraçãostring</span><span class="sxs-lookup"><span data-stu-id="b35bd-134">DurationString</span></span>        | <span data-ttu-id="b35bd-135">Exibe o texto que descreve a duração como "tempo total" ou "tempo estimado", dependendo se os valores totais são conhecidos.</span><span class="sxs-lookup"><span data-stu-id="b35bd-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="b35bd-136">Este texto é seguido por "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="b35bd-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="b35bd-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="b35bd-137">CheckedDurationString</span></span> | <span data-ttu-id="b35bd-138">Exibe o texto que descreve a duração de todos os itens marcados na lista de reprodução como "tempo total" ou "tempo estimado", dependendo se os valores totais são conhecidos.</span><span class="sxs-lookup"><span data-stu-id="b35bd-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="b35bd-139">Este texto é seguido por "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="b35bd-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="b35bd-140">O valor "tempo total:% Duration%" para uma lista de reprodução que contém uma duração total de sete minutos exibirá "tempo total: 07:00".</span><span class="sxs-lookup"><span data-stu-id="b35bd-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="b35bd-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b35bd-141">Requirements</span></span>



| <span data-ttu-id="b35bd-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="b35bd-142">Requirement</span></span> | <span data-ttu-id="b35bd-143">Valor</span><span class="sxs-lookup"><span data-stu-id="b35bd-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b35bd-144">Versão</span><span class="sxs-lookup"><span data-stu-id="b35bd-144">Version</span></span><br/> | <span data-ttu-id="b35bd-145">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b35bd-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b35bd-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b35bd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35bd-147">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="b35bd-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





