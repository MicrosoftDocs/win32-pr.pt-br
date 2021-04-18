---
title: Tentativas de renderização
description: O consórcio de cor internacional (ICC) definiu quatro valores diferentes chamados de tentativas de renderização.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- WCS (sistema de cores do Windows), tentativas de renderização
- WCS (sistema de cores do Windows), tentativas de renderização
- gerenciamento de cores de imagem, tentativas de renderização
- gerenciamento de cores, tentativas de renderização
- cores, tentativas de renderização
- tentativas de renderização
- ICC (International Color Consortium)
- IIC (consórcio de cor internacional)
- Intenção de imagem
- Intenção gráfica
- Tentativa de prova
- Tentativa de correspondência
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105773943"
---
# <a name="rendering-intents"></a><span data-ttu-id="8b522-115">Tentativas de renderização</span><span class="sxs-lookup"><span data-stu-id="8b522-115">Rendering Intents</span></span>

<span data-ttu-id="8b522-116">O consórcio de cor internacional (ICC) definiu quatro valores diferentes chamados de *tentativas de renderização*.</span><span class="sxs-lookup"><span data-stu-id="8b522-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="8b522-117">Elas representam quatro abordagens diferentes para criar uma renderização de cor.</span><span class="sxs-lookup"><span data-stu-id="8b522-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="8b522-118">Essas quatro intenções, e as constantes usadas para fazer referência a elas no código são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="8b522-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="8b522-119">Intencional</span><span class="sxs-lookup"><span data-stu-id="8b522-119">Intent</span></span>                            | <span data-ttu-id="8b522-120">Nome ICC</span><span class="sxs-lookup"><span data-stu-id="8b522-120">ICC Name</span></span>              | <span data-ttu-id="8b522-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b522-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="8b522-122">Picture</span><span class="sxs-lookup"><span data-stu-id="8b522-122">Picture</span></span> | <span data-ttu-id="8b522-123">Perceptiva</span><span class="sxs-lookup"><span data-stu-id="8b522-123">Perceptual</span></span>            | <span data-ttu-id="8b522-124">\_PERCEPTIVA intenção</span><span class="sxs-lookup"><span data-stu-id="8b522-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="8b522-125">Graphic</span><span class="sxs-lookup"><span data-stu-id="8b522-125">Graphic</span></span> | <span data-ttu-id="8b522-126">Saturação</span><span class="sxs-lookup"><span data-stu-id="8b522-126">Saturation</span></span>            | <span data-ttu-id="8b522-127">saturação da intenção \_</span><span class="sxs-lookup"><span data-stu-id="8b522-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="8b522-128">Prova</span><span class="sxs-lookup"><span data-stu-id="8b522-128">Proof</span></span>     | <span data-ttu-id="8b522-129">Colorimétrico relativo</span><span class="sxs-lookup"><span data-stu-id="8b522-129">Relative Colorimetric</span></span> | <span data-ttu-id="8b522-130">\_colorimétrico relativo da intenção \_</span><span class="sxs-lookup"><span data-stu-id="8b522-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="8b522-131">Corresponder a</span><span class="sxs-lookup"><span data-stu-id="8b522-131">Match</span></span>     | <span data-ttu-id="8b522-132">Colorimétrico absoluto</span><span class="sxs-lookup"><span data-stu-id="8b522-132">Absolute Colorimetric</span></span> | <span data-ttu-id="8b522-133">\_colorimétrico absoluto da intenção \_</span><span class="sxs-lookup"><span data-stu-id="8b522-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="8b522-134">A especificação de formato de perfil ICC versão 3,4, que descreve essas intenções, pode ser baixada em color.org.</span><span class="sxs-lookup"><span data-stu-id="8b522-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="8b522-135">Intenção de imagem</span><span class="sxs-lookup"><span data-stu-id="8b522-135">Picture Intent</span></span>

<span data-ttu-id="8b522-136">Chamado perceptiva intenção na cláusula de especificação ICC 4,9, uma intenção de imagem faz com que a [gama](./g.md) completa da imagem seja compactada ou expandida para preencher a gama do dispositivo de destino, de modo que o saldo em cinza seja preservado, mas a precisão colorimétrico pode não ser preservada.</span><span class="sxs-lookup"><span data-stu-id="8b522-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="8b522-137">Em outras palavras, se determinadas cores em uma imagem ficarem fora do intervalo de cores que o dispositivo de saída puder renderizar, a intenção de imagem fará com que todas as cores da imagem sejam ajustadas para que cada cor da imagem esteja dentro do intervalo que pode ser renderizado e que a relação entre as cores seja preservada o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="8b522-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="8b522-138">Essa intenção é mais adequada para a exibição de fotografias e imagens, e geralmente é a intenção padrão.</span><span class="sxs-lookup"><span data-stu-id="8b522-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="8b522-139">Intenção gráfica</span><span class="sxs-lookup"><span data-stu-id="8b522-139">Graphic Intent</span></span>

<span data-ttu-id="8b522-140">A cláusula de especificação ICC 4,12 chama a intenção gráfica uma intenção de [saturação](s.md) .</span><span class="sxs-lookup"><span data-stu-id="8b522-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="8b522-141">Ele preserva o croma de cores na imagem em uma possível despesa de [matiz](h.md) e [claridade](l.md).</span><span class="sxs-lookup"><span data-stu-id="8b522-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="8b522-142">A implementação dessa tentativa permanece um tanto problema, e o ICC ainda está trabalhando em métodos para atingir os efeitos desejados.</span><span class="sxs-lookup"><span data-stu-id="8b522-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="8b522-143">Essa intenção é mais adequada para gráficos de negócios, como gráficos, em que é mais importante que as cores sejam vivas e contrastem bem entre si, em vez de uma cor específica.</span><span class="sxs-lookup"><span data-stu-id="8b522-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="8b522-144">Tentativa de prova</span><span class="sxs-lookup"><span data-stu-id="8b522-144">Proof Intent</span></span>

<span data-ttu-id="8b522-145">A intenção de prova, chamada de intenção de colorimétrico na especificação ICC, é definida de modo que qualquer cor que esteja fora do intervalo que o dispositivo de saída pode processar seja ajustada para a mais próxima que possa ser renderizada, enquanto todas as outras cores permanecem inalteradas.</span><span class="sxs-lookup"><span data-stu-id="8b522-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="8b522-146">A tentativa de prova não preserva o [ponto branco](w.md).</span><span class="sxs-lookup"><span data-stu-id="8b522-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="8b522-147">Por exemplo, o branco mais branco de um papel é mais amarelo do que o branco mais branco de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="8b522-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="8b522-148">Uma imagem convertida na gama da impressora usando a intenção colorimétrico relativa resultaria em todas as cores se tornando mais amarelas.</span><span class="sxs-lookup"><span data-stu-id="8b522-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="8b522-149">O ponto branco da imagem é movido para corresponder ao ponto branco da impressora.</span><span class="sxs-lookup"><span data-stu-id="8b522-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="8b522-150">Todas as outras cores na imagem mantêm sua posição em relação ao ponto branco.</span><span class="sxs-lookup"><span data-stu-id="8b522-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="8b522-151">Isso produz uma imagem que reflete com mais precisão qual será a aparência da imagem impressa.</span><span class="sxs-lookup"><span data-stu-id="8b522-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="8b522-152">No entanto, o usuário pode encontrá-lo visualmente desconcerto.</span><span class="sxs-lookup"><span data-stu-id="8b522-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="8b522-153">Tentativa de correspondência</span><span class="sxs-lookup"><span data-stu-id="8b522-153">Match Intent</span></span>

<span data-ttu-id="8b522-154">Em uma tentativa de correspondência, todas as cores que estão fora do intervalo que o dispositivo de saída pode processar são ajustadas para a cor mais próxima que pode ser renderizada, enquanto todas as outras cores permanecem inalteradas.</span><span class="sxs-lookup"><span data-stu-id="8b522-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="8b522-155">A especificação ICC chama a intenção colorimétrico absoluta de tentativa de correspondência.</span><span class="sxs-lookup"><span data-stu-id="8b522-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="8b522-156">A tentativa de correspondência preserva o ponto branco.</span><span class="sxs-lookup"><span data-stu-id="8b522-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="8b522-157">Por exemplo, o branco mais branco de um papel é mais amarelo do que o branco mais branco de um monitor de computador.</span><span class="sxs-lookup"><span data-stu-id="8b522-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="8b522-158">Uma imagem convertida na [gama](./g.md) da impressora usando a tentativa de correspondência resultaria em todas as cores sendo convertidas e correspondidas na gama da impressora.</span><span class="sxs-lookup"><span data-stu-id="8b522-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="8b522-159">O ponto branco da imagem não é movido para corresponder ao ponto branco da impressora.</span><span class="sxs-lookup"><span data-stu-id="8b522-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="8b522-160">Portanto, a distância das cores para o ponto branco pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="8b522-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="8b522-161">Isso produz uma imagem que é menos visualmente desconcerta ao usuário, mas também é uma representação menos precisa da saída da impressora.</span><span class="sxs-lookup"><span data-stu-id="8b522-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 