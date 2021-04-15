---
title: Elemento ASX
description: O elemento ASX define um arquivo como um metarquivo.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Elemento ASX Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760898"
---
# <a name="asx-element"></a><span data-ttu-id="4cb24-104">Elemento ASX</span><span class="sxs-lookup"><span data-stu-id="4cb24-104">ASX Element</span></span>

<span data-ttu-id="4cb24-105">O elemento **ASX** define um arquivo como um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="4cb24-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="4cb24-106">Attributes</span></span>

<span data-ttu-id="4cb24-107">`VERSION` (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="4cb24-107">`VERSION` (required)</span></span>

<span data-ttu-id="4cb24-108">Número decimal que representa o número de versão da sintaxe para o metarquivo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="4cb24-109">Defina como 3 ou 3,0.</span><span class="sxs-lookup"><span data-stu-id="4cb24-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="4cb24-110">**Modo de exibição de visualização** (opcional)</span><span class="sxs-lookup"><span data-stu-id="4cb24-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="4cb24-111">Valor que indica se o Windows Media Player entra no modo de visualização antes de reproduzir o primeiro clipe.</span><span class="sxs-lookup"><span data-stu-id="4cb24-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="4cb24-112">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cb24-112">Must be one of the following values.</span></span>



| <span data-ttu-id="4cb24-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4cb24-113">Value</span></span> | <span data-ttu-id="4cb24-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cb24-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb24-115">YES</span><span class="sxs-lookup"><span data-stu-id="4cb24-115">YES</span></span>   | <span data-ttu-id="4cb24-116">O Windows Media Player entra no modo de visualização antes de executar o primeiro clipe.</span><span class="sxs-lookup"><span data-stu-id="4cb24-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="4cb24-117">Não</span><span class="sxs-lookup"><span data-stu-id="4cb24-117">NO</span></span>    | <span data-ttu-id="4cb24-118">O valor padrão.</span><span class="sxs-lookup"><span data-stu-id="4cb24-118">The default value.</span></span> <span data-ttu-id="4cb24-119">O Windows Media Player não entra no modo de visualização antes de executar o primeiro clipe.</span><span class="sxs-lookup"><span data-stu-id="4cb24-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="4cb24-120">**BANNERBAR** (opcional)</span><span class="sxs-lookup"><span data-stu-id="4cb24-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="4cb24-121">Valor que indica se o Windows Media Player reserva espaço para um gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="4cb24-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="4cb24-122">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4cb24-122">Must be one of the following values.</span></span>



| <span data-ttu-id="4cb24-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4cb24-123">Value</span></span> | <span data-ttu-id="4cb24-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cb24-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb24-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="4cb24-125">AUTO</span></span>  | <span data-ttu-id="4cb24-126">O valor padrão.</span><span class="sxs-lookup"><span data-stu-id="4cb24-126">The default value.</span></span> <span data-ttu-id="4cb24-127">O Windows Media Player reserva espaço para a barra de faixa somente quando uma parte do conteúdo inclui uma.</span><span class="sxs-lookup"><span data-stu-id="4cb24-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="4cb24-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="4cb24-128">FIXED</span></span> | <span data-ttu-id="4cb24-129">O Windows Media Player reserva um espaço fixo para um gráfico de banner para cada parte do conteúdo tocado, independentemente de haver uma faixa associada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="4cb24-130">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="4cb24-130">Parent/Child Elements</span></span>



| <span data-ttu-id="4cb24-131">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="4cb24-131">Hierarchy</span></span>       | <span data-ttu-id="4cb24-132">Elementos</span><span class="sxs-lookup"><span data-stu-id="4cb24-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb24-133">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4cb24-133">Parent elements</span></span> | <span data-ttu-id="4cb24-134">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4cb24-134">None.</span></span> <span data-ttu-id="4cb24-135">O elemento **ASX** deve ser o primeiro elemento em todos os metarquivos.</span><span class="sxs-lookup"><span data-stu-id="4cb24-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="4cb24-136">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4cb24-136">Child elements</span></span>  | <span data-ttu-id="4cb24-137">**abstrato**, **autor**, **faixa**, **base**, **direitos autorais**, **entrada**, **ENTRYREF**, **evento**, **moreinfo**, **PREVIEWDURATION**, **param**, **repetir**, **título**</span><span class="sxs-lookup"><span data-stu-id="4cb24-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4cb24-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cb24-138">Remarks</span></span>

<span data-ttu-id="4cb24-139">Os primeiros quatro caracteres de uma lista de reprodução de metarquivo devem ser "<ASX".</span><span class="sxs-lookup"><span data-stu-id="4cb24-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="4cb24-140">Outros elementos definidos no escopo do elemento **ASX** , como **título** e **autor**, são associados à exibição de informações exibidas pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4cb24-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="4cb24-141">Para o Windows Media Player, o número de versão da sintaxe é 3,0.</span><span class="sxs-lookup"><span data-stu-id="4cb24-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="4cb24-142">O Windows Media Player dá suporte a todas as versões anteriores da sintaxe de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="4cb24-143">Os valores aceitáveis para o atributo **version** incluem 3,0 e 3 (sem ponto decimal).</span><span class="sxs-lookup"><span data-stu-id="4cb24-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="4cb24-144">Se o valor do atributo **PREviewmode** for sim, o Windows Media Player entrará imediatamente no modo de visualização antes de reproduzir o primeiro clipe.</span><span class="sxs-lookup"><span data-stu-id="4cb24-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="4cb24-145">Quando o Windows Media Player entra no modo de visualização, ele visualiza cada clipe referenciado no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="4cb24-146">O elemento **PREVIEWDURATION** determina a duração de cada visualização.</span><span class="sxs-lookup"><span data-stu-id="4cb24-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="4cb24-147">O atributo **BANNERBAR** define se o player de mídia do Windows reserva espaço para um gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="4cb24-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="4cb24-148">Uma faixa é um gráfico que é exibido na área de exibição do vídeo enquanto o conteúdo da mídia está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="4cb24-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="4cb24-149">(Use o elemento **banner** para adicionar uma faixa ao conteúdo.) Se o valor de **BANNERBAR** for corrigido, o Windows Media Player reserva espaço em faixa para cada parte do conteúdo de mídia, independentemente de o conteúdo de mídia ter uma faixa.</span><span class="sxs-lookup"><span data-stu-id="4cb24-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="4cb24-150">Se uma parte do conteúdo de mídia não tiver uma faixa associada a ela, o espaço reservado para um será preto.</span><span class="sxs-lookup"><span data-stu-id="4cb24-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="4cb24-151">Se o valor do atributo **BANNERBAR** for auto, o Windows Media Player reserva espaço para a faixa somente quando o conteúdo da mídia inclui um.</span><span class="sxs-lookup"><span data-stu-id="4cb24-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="4cb24-152">Se você criar um metarquivo com vários clipes (elementos de **entrada** ou **ENTRYREF** ) e definir o valor do atributo **BANNERBAR** como auto, o Windows Media Player poderá ser redimensionado para permitir espaço para um gráfico de faixa para um clipe e redimensioná-lo novamente se o próximo clipe não contiver um gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="4cb24-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="4cb24-153">Se você quiser que o tamanho da janela permaneça o mesmo (exceto quando o tamanho do vídeo for alterado), use o valor fixo para o atributo **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="4cb24-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="4cb24-154">O espaço reservado para um gráfico de banner é de 32 pixels de altura por 194 pixels de largura.</span><span class="sxs-lookup"><span data-stu-id="4cb24-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="4cb24-155">O espaço reservado é exibido abaixo de qualquer conteúdo de vídeo renderizado e 6 pixels acima da borda inferior da área de vídeo, permitindo o espaço para a borda da área de vídeo de 6 pixels.</span><span class="sxs-lookup"><span data-stu-id="4cb24-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="4cb24-156">O espaço reservado da faixa é centralizado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="4cb24-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="4cb24-157">O Windows Media Player renderiza o gráfico a partir do pixel da extrema esquerda do espaço do banner.</span><span class="sxs-lookup"><span data-stu-id="4cb24-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="4cb24-158">Se o gráfico ocupar todo o espaço, ele aparecerá centralizado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="4cb24-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="4cb24-159">Caso contrário, haverá espaço à direita.</span><span class="sxs-lookup"><span data-stu-id="4cb24-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="4cb24-160">Observe que a largura mínima do Windows Media Player é sempre maior do que o tamanho do clipe de vídeo, independentemente do valor do atributo **BANNERBAR** .</span><span class="sxs-lookup"><span data-stu-id="4cb24-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="4cb24-161">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4cb24-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="4cb24-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cb24-162">Requirements</span></span>



| <span data-ttu-id="4cb24-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb24-163">Requirement</span></span> | <span data-ttu-id="4cb24-164">Valor</span><span class="sxs-lookup"><span data-stu-id="4cb24-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="4cb24-165">Versão</span><span class="sxs-lookup"><span data-stu-id="4cb24-165">Version</span></span><br/> | <span data-ttu-id="4cb24-166">Windows Media Player versão 70 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4cb24-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cb24-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cb24-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb24-168">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4cb24-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4cb24-169">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4cb24-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





