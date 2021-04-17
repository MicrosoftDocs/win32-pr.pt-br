---
title: Mapas de sombra em cascata
description: Os mapas de sombra em cascata (CSMs) são a melhor maneira de combater um dos erros mais predominantes com a aplicação de alias de perspectiva de sombreamento.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70433f97f33c3cc28af8e282b14ea1f513cf4d
ms.sourcegitcommit: 54db9e6a00a5c8f68e7c1a16b8c6d4943374498c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/01/2021
ms.locfileid: "106165529"
---
# <a name="cascaded-shadow-maps"></a><span data-ttu-id="e333d-103">Mapas de sombra em cascata</span><span class="sxs-lookup"><span data-stu-id="e333d-103">Cascaded Shadow Maps</span></span>

<span data-ttu-id="e333d-104">Os mapas de sombra em cascata (CSMs) são a melhor maneira de combater um dos erros mais predominantes com sombreamento: alias de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="e333d-104">Cascaded shadow maps (CSMs) are the best way to combat one of the most prevalent errors with shadowing: perspective aliasing.</span></span> <span data-ttu-id="e333d-105">Este artigo técnico, que pressupõe que o leitor está familiarizado com o mapeamento de sombra, resolve o tópico de CSMs.</span><span class="sxs-lookup"><span data-stu-id="e333d-105">This technical article, which assumes the reader is familiar with shadow mapping, tackles the topic of CSMs.</span></span> <span data-ttu-id="e333d-106">Especificamente, ele:</span><span class="sxs-lookup"><span data-stu-id="e333d-106">Specifically, it:</span></span>

-   <span data-ttu-id="e333d-107">explica a complexidade do CSMs;</span><span class="sxs-lookup"><span data-stu-id="e333d-107">explains the complexity of CSMs;</span></span>
-   <span data-ttu-id="e333d-108">fornece detalhes sobre as possíveis variações dos algoritmos CSM;</span><span class="sxs-lookup"><span data-stu-id="e333d-108">gives details on the possible variations of the CSM algorithms;</span></span>
-   <span data-ttu-id="e333d-109">Descreve as duas técnicas de filtragem mais comuns: PCF (filtragem mais próxima de percentual) e filtragem com mapas de sombra de variação (VSMs);</span><span class="sxs-lookup"><span data-stu-id="e333d-109">describes the two most common filtering techniques—percentage closer filtering (PCF) and filtering with variance shadow maps (VSMs);</span></span>
-   <span data-ttu-id="e333d-110">Identifica e aborda algumas das armadilhas comuns associadas à adição de filtragem ao CSMs; e</span><span class="sxs-lookup"><span data-stu-id="e333d-110">identifies and addresses some of the common pitfalls associated with adding filtering to CSMs; and</span></span>
-   <span data-ttu-id="e333d-111">mostra como mapear CSMs para Direct3D 10 por meio de hardware do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e333d-111">shows how to map CSMs to Direct3D 10 through Direct3D 11 hardware.</span></span>

<span data-ttu-id="e333d-112">O código usado neste artigo pode ser encontrado no SDK (Software Development Kit) do DirectX nos exemplos CascadedShadowMaps11 e VarianceShadows11.</span><span class="sxs-lookup"><span data-stu-id="e333d-112">The code used in this article can be found in the DirectX Software Development Kit (SDK) in the CascadedShadowMaps11 and VarianceShadows11 samples.</span></span> <span data-ttu-id="e333d-113">Este artigo se mostrará mais útil depois de implementar as técnicas abordadas no artigo técnico, [técnicas comuns para melhorar os mapas de profundidade de sombra](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), são implementadas.</span><span class="sxs-lookup"><span data-stu-id="e333d-113">This article will prove most useful after implementing the techniques covered in the technical article, [Common Techniques to Improve Shadow Depth Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps), are implemented.</span></span>

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a><span data-ttu-id="e333d-114">Mapas de sombra em cascata e alias de perspectiva</span><span class="sxs-lookup"><span data-stu-id="e333d-114">Cascaded Shadow Maps and Perspective Aliasing</span></span>

<span data-ttu-id="e333d-115">O alias de perspectiva em um mapa de sombra é um dos problemas mais difíceis de superar.</span><span class="sxs-lookup"><span data-stu-id="e333d-115">Perspective aliasing in a shadow map is one of the most difficult problems to overcome.</span></span> <span data-ttu-id="e333d-116">No artigo técnico, técnicas comuns para melhorar os mapas de profundidade de sombra, o alias de perspectiva é descrito e algumas abordagens para mitigar o problema são identificadas.</span><span class="sxs-lookup"><span data-stu-id="e333d-116">In the technical article, Common Techniques to Improve Shadow Depth Maps, perspective aliasing is described and some approaches to mitigate the problem are identified.</span></span> <span data-ttu-id="e333d-117">Na prática, o CSMs tende a ser a melhor solução e é normalmente empregado em jogos modernos.</span><span class="sxs-lookup"><span data-stu-id="e333d-117">In practice, CSMs tend to be the best solution, and are commonly employed in modern games.</span></span>

<span data-ttu-id="e333d-118">O conceito básico de CSMs é fácil de entender.</span><span class="sxs-lookup"><span data-stu-id="e333d-118">The basic concept of CSMs is easy to understand.</span></span> <span data-ttu-id="e333d-119">Áreas diferentes da câmera frustum exigem mapas de sombra com resoluções diferentes.</span><span class="sxs-lookup"><span data-stu-id="e333d-119">Different areas of the camera frustum require shadow maps with different resolutions.</span></span> <span data-ttu-id="e333d-120">Os objetos mais próximos do olho exigem uma resolução maior do que fazer com mais objetos distantes.</span><span class="sxs-lookup"><span data-stu-id="e333d-120">Objects nearest the eye require a higher resolution than do more distant objects.</span></span> <span data-ttu-id="e333d-121">Na verdade, quando o olho se move muito próximo da geometria, os pixels mais próximos do olho podem exigir muita resolução que até mesmo um mapa de sombra de 4096 × 4096 é insuficiente.</span><span class="sxs-lookup"><span data-stu-id="e333d-121">In fact, when the eye moves very close to the geometry, the pixels nearest the eye can require so much resolution that even a 4096 × 4096 shadow map is insufficient.</span></span>

<span data-ttu-id="e333d-122">A ideia básica do CSMs é particionar o frustum em vários Frusta.</span><span class="sxs-lookup"><span data-stu-id="e333d-122">The basic idea of CSMs is to partition the frustum into multiple frusta.</span></span> <span data-ttu-id="e333d-123">Um mapa de sombra é renderizado para cada subfrustum; em seguida, o sombreador de pixel faz amostras do mapa que mais se aproximará da resolução necessária (Figura 2).</span><span class="sxs-lookup"><span data-stu-id="e333d-123">A shadow map is rendered for each subfrustum; the pixel shader then samples from the map that most closely matches the required resolution (Figure 2).</span></span>

<span data-ttu-id="e333d-124">**Figura 1. Cobertura do mapa de sombra**</span><span class="sxs-lookup"><span data-stu-id="e333d-124">**Figure 1. Shadow map coverage**</span></span>

![cobertura do mapa de sombra](images/shadow-map-coverage.png)

<span data-ttu-id="e333d-126">Na Figura 1, a qualidade é mostrada (da esquerda para a direita) da mais alta para a mais baixa.</span><span class="sxs-lookup"><span data-stu-id="e333d-126">In Figure 1, quality is shown (left to right) from highest to lowest.</span></span> <span data-ttu-id="e333d-127">A série de grades que representa mapas de sombra com uma exibição frustum (cone invertido em vermelho) mostra como a cobertura de pixel é afetada com mapas de sombra de resolução diferentes.</span><span class="sxs-lookup"><span data-stu-id="e333d-127">The series of grids representing shadow maps with a view frustum (inverted cone in red) shows how pixel coverage is affected with different resolution shadow maps.</span></span> <span data-ttu-id="e333d-128">As sombras são da qualidade mais alta (pixels brancos) quando há um mapeamento de proporção de 1:1 pixels em espaço leve para texels no mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-128">Shadows are of the highest quality (white pixels) when there is a 1:1 ratio mapping pixels in light space to texels in the shadow map.</span></span> <span data-ttu-id="e333d-129">O alias de perspectiva ocorre na forma de mapas de textura grandes e bloqueados (imagem esquerda) quando muitos pixels são mapeados para o mesmo Texel de sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-129">Perspective aliasing occurs in the form of large, blocky texture maps (left image) when too many pixels map to the same shadow texel.</span></span> <span data-ttu-id="e333d-130">Quando o mapa de sombra é muito grande, ele está em amostra.</span><span class="sxs-lookup"><span data-stu-id="e333d-130">When the shadow map is too large, it is under sampled.</span></span> <span data-ttu-id="e333d-131">Nesse caso, os texels são ignorados, os artefatos do shimmering são introduzidos e o desempenho é afetado.</span><span class="sxs-lookup"><span data-stu-id="e333d-131">In this case, texels are skipped, shimmering artifacts are introduced, and performance is affected.</span></span>

<span data-ttu-id="e333d-132">**Figura 2. Qualidade de sombra CSM**</span><span class="sxs-lookup"><span data-stu-id="e333d-132">**Figure 2. CSM shadow quality**</span></span>

![qualidade de sombra CSM](images/csm-shadow-quality.png)

<span data-ttu-id="e333d-134">A Figura 2 mostra recortes da seção de qualidade mais alta em cada mapa de sombra na Figura 1.</span><span class="sxs-lookup"><span data-stu-id="e333d-134">Figure 2 shows cutouts from the highest quality section in each shadow map in Figure 1.</span></span> <span data-ttu-id="e333d-135">O mapa de sombra com os pixels mais bem colocados (no Apex) é mais próximo do olho.</span><span class="sxs-lookup"><span data-stu-id="e333d-135">The shadow map with the most closely placed pixels (at the apex) is nearest the eye.</span></span> <span data-ttu-id="e333d-136">Tecnicamente, esses são mapas do mesmo tamanho, com branco e cinza usados para exemplificar o sucesso do mapa de sombra em cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-136">Technically, these are maps of the same size, with white and grey used to exemplify the success of the cascaded shadow map.</span></span> <span data-ttu-id="e333d-137">O branco é ideal porque mostra uma boa cobertura – uma proporção de 1:1 para pixels de espaço de olho e texels de mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-137">White is ideal because it shows good coverage—a 1:1 ratio for eye-space pixels and shadow-map texels.</span></span>

<span data-ttu-id="e333d-138">CSMs exigem as etapas a seguir por quadro.</span><span class="sxs-lookup"><span data-stu-id="e333d-138">CSMs require the following steps per frame.</span></span>

1.  <span data-ttu-id="e333d-139">Particione o frustum em subfrusta.</span><span class="sxs-lookup"><span data-stu-id="e333d-139">Partition the frustum into subfrusta.</span></span>
2.  <span data-ttu-id="e333d-140">Compute uma projeção ortográfica para cada subfrustum.</span><span class="sxs-lookup"><span data-stu-id="e333d-140">Compute an orthographic projection for each subfrustum.</span></span>
3.  <span data-ttu-id="e333d-141">Renderizar um mapa de sombra para cada subfrustum.</span><span class="sxs-lookup"><span data-stu-id="e333d-141">Render a shadow map for each subfrustum.</span></span>
4.  <span data-ttu-id="e333d-142">Renderizar a cena.</span><span class="sxs-lookup"><span data-stu-id="e333d-142">Render the scene.</span></span>

    1.  <span data-ttu-id="e333d-143">Associar os mapas de sombra e renderizar.</span><span class="sxs-lookup"><span data-stu-id="e333d-143">Bind the shadow maps and render.</span></span>
    2.  <span data-ttu-id="e333d-144">O sombreador de vértice faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e333d-144">The vertex shader does the following:</span></span>

        -   <span data-ttu-id="e333d-145">Computa coordenadas de textura para cada subfrustum leve (a menos que a coordenada de textura necessária seja calculada no sombreador de pixels).</span><span class="sxs-lookup"><span data-stu-id="e333d-145">Computes texture coordinates for each light subfrustum (unless the needed texture coordinate is calculated in the pixel shader).</span></span>
        -   <span data-ttu-id="e333d-146">Transforma e ilumina o vértice e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e333d-146">Transforms and lights the vertex, and so on.</span></span>

    3.  <span data-ttu-id="e333d-147">O sombreador de pixel faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e333d-147">The pixel shader does the following:</span></span>

        -   <span data-ttu-id="e333d-148">Determina o mapa de sombra adequado.</span><span class="sxs-lookup"><span data-stu-id="e333d-148">Determines the proper shadow map.</span></span>
        -   <span data-ttu-id="e333d-149">Transforma as coordenadas de textura, se necessário.</span><span class="sxs-lookup"><span data-stu-id="e333d-149">Transforms the texture coordinates if necessary.</span></span>
        -   <span data-ttu-id="e333d-150">A amostra da cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-150">Samples the cascade.</span></span>
        -   <span data-ttu-id="e333d-151">Acende o pixel.</span><span class="sxs-lookup"><span data-stu-id="e333d-151">Lights the pixel.</span></span>

## <a name="partitioning-the-frustum"></a><span data-ttu-id="e333d-152">Particionando o frustum</span><span class="sxs-lookup"><span data-stu-id="e333d-152">Partitioning the Frustum</span></span>

<span data-ttu-id="e333d-153">O particionamento do frustum é o ato de criar subfrusta.</span><span class="sxs-lookup"><span data-stu-id="e333d-153">Partitioning the frustum is the act of creating subfrusta.</span></span> <span data-ttu-id="e333d-154">Uma técnica para dividir o frustum é calcular intervalos de zero% a 100% na direção Z.</span><span class="sxs-lookup"><span data-stu-id="e333d-154">One technique for splitting the frustum is to calculate intervals from zero percent to one hundred percent in the Z-direction.</span></span> <span data-ttu-id="e333d-155">Cada intervalo representa um plano próximo e um plano distante como uma porcentagem do eixo Z.</span><span class="sxs-lookup"><span data-stu-id="e333d-155">Each interval then represents a near plane and a far plane as a percentage of the Z-axis.</span></span>

<span data-ttu-id="e333d-156">**Figura 3. Exibir frustums particionados arbitrariamente**</span><span class="sxs-lookup"><span data-stu-id="e333d-156">**Figure 3. View frustums partitioned arbitrarily**</span></span>

![Exibir frustums particionados arbitrariamente](images/view-frustums-partitioned-arbitrarily.png)

<span data-ttu-id="e333d-158">Na prática, recalcular as divisões de frustum por quadro causa bordas de sombra para shimmer.</span><span class="sxs-lookup"><span data-stu-id="e333d-158">In practice, recalculating the frustum splits per frame causes shadow edges to shimmer.</span></span> <span data-ttu-id="e333d-159">A prática geralmente aceita é usar um conjunto estático de intervalos em cascata por cenário.</span><span class="sxs-lookup"><span data-stu-id="e333d-159">The generally accepted practice is to use a static set of cascade intervals per scenario.</span></span> <span data-ttu-id="e333d-160">Nesse cenário, o intervalo ao longo do eixo Z é usado para descrever um subfrustum que ocorre ao particionar o frustum.</span><span class="sxs-lookup"><span data-stu-id="e333d-160">In this scenario, the interval along the Z-axis is used to describe a subfrustum that occurs when partitioning the frustum.</span></span> <span data-ttu-id="e333d-161">Determinar os intervalos de tamanho corretos para uma determinada cena depende de vários fatores.</span><span class="sxs-lookup"><span data-stu-id="e333d-161">Determining the correct size intervals for a given scene depends upon several factors.</span></span>

### <a name="orientation-of-the-scene-geometry"></a><span data-ttu-id="e333d-162">Orientação da geometria da cena</span><span class="sxs-lookup"><span data-stu-id="e333d-162">Orientation of the Scene Geometry</span></span>

<span data-ttu-id="e333d-163">Em relação à geometria da cena, a orientação da câmera afeta a seleção de intervalo em cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-163">With respect to scene geometry, camera orientation affects cascade interval selection.</span></span> <span data-ttu-id="e333d-164">Por exemplo, uma câmera muito perto do solo, como uma câmera de aterramento em um jogo de futebol, tem um conjunto estático diferente de intervalos em cascata do que uma câmera no céu.</span><span class="sxs-lookup"><span data-stu-id="e333d-164">For example, a camera very near the ground, such as a ground camera in a football game, has a different static set of cascade intervals than a camera in the sky.</span></span>

<span data-ttu-id="e333d-165">A Figura 4 mostra algumas câmeras diferentes e suas respectivas partições.</span><span class="sxs-lookup"><span data-stu-id="e333d-165">Figure 4 shows some different cameras and their respective partitions.</span></span> <span data-ttu-id="e333d-166">Quando o intervalo Z da cena é muito grande, mais planos de divisão são necessários.</span><span class="sxs-lookup"><span data-stu-id="e333d-166">When the scene's Z-range is very large, more split planes are required.</span></span> <span data-ttu-id="e333d-167">Por exemplo, quando o olho é muito próximo do plano de chão, mas objetos distantes ainda são visíveis, várias cascatas podem ser necessárias.</span><span class="sxs-lookup"><span data-stu-id="e333d-167">For example, when the eye is very near the ground plane, but distant objects are still visible, multiple cascades can be necessary.</span></span> <span data-ttu-id="e333d-168">Dividindo o frustum de forma que mais divisões estejam perto do olho (em que o alias da perspectiva está mudando o mais rápido) também é valioso.</span><span class="sxs-lookup"><span data-stu-id="e333d-168">Dividing the frustum so that more splits are near the eye (where perspective aliasing is changing the fastest) is also valuable.</span></span> <span data-ttu-id="e333d-169">Quando a maior parte da geometria é concentrados em uma pequena seção (como uma exibição de sobrecarga ou um simulador de voo) da exibição frustum, são necessárias menos cascatas.</span><span class="sxs-lookup"><span data-stu-id="e333d-169">When most of the geometry is clumped into a small section (such as an overhead view or a flight simulator) of the view frustum, fewer cascades are necessary.</span></span>

<span data-ttu-id="e333d-170">**Figura 4. Configurações diferentes exigem divisões de frustum diferentes**</span><span class="sxs-lookup"><span data-stu-id="e333d-170">**Figure 4. Different configurations require different frustum splits**</span></span>

![configurações diferentes exigem divisões de frustum diferentes](images/different-configurations-require-different-frustum-splits.png)

<span data-ttu-id="e333d-172">Mantida Quando Geometry tem um intervalo dinâmico alto em Z, muitas cascatas são necessárias.</span><span class="sxs-lookup"><span data-stu-id="e333d-172">(Left) When geometry has a high dynamic range in Z, lots of cascades are required.</span></span> <span data-ttu-id="e333d-173">Centraliza Quando a geometria tem um intervalo dinâmico baixo em Z, não há muito benefício de vários frustums.</span><span class="sxs-lookup"><span data-stu-id="e333d-173">(Center) When the geometry has low dynamic range in Z, there is little benefit from multiple frustums.</span></span> <span data-ttu-id="e333d-174">Adequada Somente três partições são necessárias quando o intervalo dinâmico é médio.</span><span class="sxs-lookup"><span data-stu-id="e333d-174">(Right) Only three partitions are needed when the dynamic range is medium.</span></span>

### <a name="orientation-of-the-light-and-the-camera"></a><span data-ttu-id="e333d-175">Orientação da luz e da câmera</span><span class="sxs-lookup"><span data-stu-id="e333d-175">Orientation of the Light and the Camera</span></span>

<span data-ttu-id="e333d-176">A matriz de projeção de cada cascata é ajustada rigidamente ao seu subfrustum correspondente.</span><span class="sxs-lookup"><span data-stu-id="e333d-176">Each cascade's projection matrix is fit tightly around its corresponding subfrustum.</span></span> <span data-ttu-id="e333d-177">Em configurações nas quais a câmera de exibição e as direções claras são ortogonal, as cascatas podem se ajustar com pouca sobreposição.</span><span class="sxs-lookup"><span data-stu-id="e333d-177">In configurations where the view camera and the light directions are orthogonal, the cascades can be fit tightly with little overlap.</span></span> <span data-ttu-id="e333d-178">A sobreposição se torna maior à medida que a luz e a câmera de exibição se movem para o alinhamento paralelo (Figura 5).</span><span class="sxs-lookup"><span data-stu-id="e333d-178">The overlap becomes larger as the light and the view camera move into parallel alignment (Figure 5).</span></span> <span data-ttu-id="e333d-179">Quando a luz e a câmera de exibição são quase paralelas, ela é chamada de "Dueling Frusta" e é um cenário muito difícil para a maioria dos algoritmos de sombreamento.</span><span class="sxs-lookup"><span data-stu-id="e333d-179">When the light and the view camera are nearly parallel, it is called a "dueling frusta," and is a very hard scenario for most shadowing algorithms.</span></span> <span data-ttu-id="e333d-180">Não é incomum restringir a luz e a câmera para que esse cenário não ocorra.</span><span class="sxs-lookup"><span data-stu-id="e333d-180">It is not uncommon to constrain the light and camera so that this scenario does not occur.</span></span> <span data-ttu-id="e333d-181">O CSMs, no entanto, executa muito melhor do que muitos outros algoritmos nesse cenário.</span><span class="sxs-lookup"><span data-stu-id="e333d-181">CSMs, however, perform much better than many other algorithms in this scenario.</span></span>

<span data-ttu-id="e333d-182">**Figura 5. Sobreposição em cascata aumenta conforme a direção da luz se torna paralela com a direção da câmera**</span><span class="sxs-lookup"><span data-stu-id="e333d-182">**Figure 5. Cascade overlap increases as light direction becomes parallel with camera direction**</span></span>

![sobreposição em cascata aumenta conforme a direção da luz se torna paralela com a direção da câmera](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

<span data-ttu-id="e333d-184">Muitas implementações de CSM usam Frusta de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="e333d-184">Many CSM implementations use fixed-size frusta.</span></span> <span data-ttu-id="e333d-185">O sombreador de pixel pode usar a profundidade Z para indexar na matriz de cascata quando o frustum é dividido em intervalos de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="e333d-185">The pixel shader can use the Z-depth to index into the array of cascades when the frustum is split in fixed-size intervals.</span></span>

## <a name="calculating-a-view-frustum-bound"></a><span data-ttu-id="e333d-186">Calculando um View-Frustum associado</span><span class="sxs-lookup"><span data-stu-id="e333d-186">Calculating a View-Frustum Bound</span></span>

<span data-ttu-id="e333d-187">Depois que os intervalos de frustum são selecionados, os subfrusta são criados usando um dos dois: ajustar à cena e ajustar à cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-187">Once the frustum intervals are selected, the subfrusta are created using one of two: fit to scene and fit to cascade.</span></span>

### <a name="fit-to-scene"></a><span data-ttu-id="e333d-188">Ajustar à cena</span><span class="sxs-lookup"><span data-stu-id="e333d-188">Fit to Scene</span></span>

<span data-ttu-id="e333d-189">Todos os Frusta podem ser criados com o mesmo plano próximo.</span><span class="sxs-lookup"><span data-stu-id="e333d-189">All of the frusta can be created with the same near plane.</span></span> <span data-ttu-id="e333d-190">Isso força a sobreposição das cascatas.</span><span class="sxs-lookup"><span data-stu-id="e333d-190">This forces the cascades to overlap.</span></span> <span data-ttu-id="e333d-191">O exemplo CascadedShadowMaps11 chama essa técnica ajustada à cena.</span><span class="sxs-lookup"><span data-stu-id="e333d-191">The CascadedShadowMaps11 sample calls this technique fit to scene.</span></span>

### <a name="fit-to-cascade"></a><span data-ttu-id="e333d-192">Ajustar à cascata</span><span class="sxs-lookup"><span data-stu-id="e333d-192">Fit to Cascade</span></span>

<span data-ttu-id="e333d-193">Como alternativa, Frusta pode ser criado com o intervalo de partição real que está sendo usado como planos próximos e distantes.</span><span class="sxs-lookup"><span data-stu-id="e333d-193">Alternatively, frusta can be created with the actual partition interval being used as near and far planes.</span></span> <span data-ttu-id="e333d-194">Isso causa um ajuste mais rígido, mas é degenerado para se ajustar à cena no caso de Dueling Frusta.</span><span class="sxs-lookup"><span data-stu-id="e333d-194">This causes a tighter fit, but degenerates to fit to scene in the case of dueling frusta.</span></span> <span data-ttu-id="e333d-195">Os exemplos de CascadedShadowMaps11 chamam essa técnica se ajustam à cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-195">The CascadedShadowMaps11 samples calls this technique fit to cascade.</span></span>

<span data-ttu-id="e333d-196">Esses dois métodos são mostrados na Figura 6.</span><span class="sxs-lookup"><span data-stu-id="e333d-196">These two methods are shown in Figure 6.</span></span> <span data-ttu-id="e333d-197">Ajustar à cascata desperdiça menos resolução.</span><span class="sxs-lookup"><span data-stu-id="e333d-197">Fit to cascade wastes less resolution.</span></span> <span data-ttu-id="e333d-198">O problema de ajustar à cascata é que a projeção ortográfica aumenta e diminui com base na orientação da exibição frustum.</span><span class="sxs-lookup"><span data-stu-id="e333d-198">The problem with fit to cascade is that the orthographic projection grows and shrinks based on the orientation of the view frustum.</span></span> <span data-ttu-id="e333d-199">A técnica ajustar à cena ajusta a projeção ortográfica pelo tamanho máximo da exibição frustum removendo os artefatos que aparecem quando a câmera de exibição é movida.</span><span class="sxs-lookup"><span data-stu-id="e333d-199">The fit to scene technique pads the orthographic projection by the max size of the view frustum removing the artifacts that appear when the view-camera moves.</span></span> <span data-ttu-id="e333d-200">[Técnicas comuns para melhorar os mapas de profundidade de sombra](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) abordam os artefatos que aparecem quando a luz se move na seção "movendo a luz em incrementos de tamanho de Texel".</span><span class="sxs-lookup"><span data-stu-id="e333d-200">[Common Techniques to Improve Shadow Depth Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) addresses the artifacts that appear when the light moves in the section "Moving the light in texel sized increments."</span></span>

<span data-ttu-id="e333d-201">**Figura 6. Ajustar à cena versus ajustar à cascata**</span><span class="sxs-lookup"><span data-stu-id="e333d-201">**Figure 6. Fit to scene vs. fit to cascade**</span></span>

![ajustar à cena em vez de ajustar à cascata](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a><span data-ttu-id="e333d-203">Renderizar o mapa de sombra</span><span class="sxs-lookup"><span data-stu-id="e333d-203">Render the Shadow Map</span></span>

<span data-ttu-id="e333d-204">O exemplo CascadedShadowMaps11 renderiza os mapas de sombra em um buffer grande.</span><span class="sxs-lookup"><span data-stu-id="e333d-204">The CascadedShadowMaps11 sample renders the shadow maps into one large buffer.</span></span> <span data-ttu-id="e333d-205">Isso ocorre porque o PCF em matrizes de textura é um recurso do Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="e333d-205">This is because PCF on texture arrays is a Direct3D 10.1 feature.</span></span> <span data-ttu-id="e333d-206">Para cada cascata, um visor é criado para cobrir a seção do buffer de profundidade correspondente a essa cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-206">For every cascade, a viewport is created that covers the section of the depth buffer corresponding to that cascade.</span></span> <span data-ttu-id="e333d-207">Um sombreador de pixel nulo está associado porque apenas a profundidade é necessária.</span><span class="sxs-lookup"><span data-stu-id="e333d-207">A null pixel shader is bound because only the depth is needed.</span></span> <span data-ttu-id="e333d-208">Por fim, o visor e a matriz de sombra corretos são definidos para cada cascata à medida que os mapas de profundidade são renderizados um de cada vez no buffer de sombra principal.</span><span class="sxs-lookup"><span data-stu-id="e333d-208">Finally, the correct viewport and shadow matrix are set for each cascade as the depth maps are rendered one at a time into the main shadow buffer.</span></span>

## <a name="render-the-scene"></a><span data-ttu-id="e333d-209">Renderizar a cena</span><span class="sxs-lookup"><span data-stu-id="e333d-209">Render the Scene</span></span>

<span data-ttu-id="e333d-210">O buffer que contém as sombras agora está associado ao sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="e333d-210">The buffer containing the shadows is now bound to the pixel shader.</span></span> <span data-ttu-id="e333d-211">Há dois métodos para selecionar a cascata implementada no exemplo CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="e333d-211">There are two methods for selecting the cascade implemented in the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="e333d-212">Esses dois métodos são explicados com o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="e333d-212">These two methods are explained with shader code.</span></span>

### <a name="interval-based-cascade-selection"></a><span data-ttu-id="e333d-213">Interval-Based seleção em cascata</span><span class="sxs-lookup"><span data-stu-id="e333d-213">Interval-Based Cascade Selection</span></span>

<span data-ttu-id="e333d-214">**Figura 7. Seleção em cascata baseada em intervalo**</span><span class="sxs-lookup"><span data-stu-id="e333d-214">**Figure 7. Interval-based cascade selection**</span></span>

![seleção em cascata baseada em intervalo](images/interval-based-cascade-selection.jpg)

<span data-ttu-id="e333d-216">Na seleção baseada em intervalo (Figura 7), o sombreador de vértice computa a posição em espaço Mundial do vértice.</span><span class="sxs-lookup"><span data-stu-id="e333d-216">In interval-based selection (Figure 7), the vertex shader computes the position in world-space of the vertex.</span></span>


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



<span data-ttu-id="e333d-217">O sombreador de pixel recebe a profundidade interpolada.</span><span class="sxs-lookup"><span data-stu-id="e333d-217">The pixel shader receives the interpolated depth.</span></span>


```C++
fCurrentPixelDepth = Input.vDepth;
```



<span data-ttu-id="e333d-218">A seleção em cascata baseada em intervalo usa uma comparação de vetor e um produto de ponto para determinar o cacade correto.</span><span class="sxs-lookup"><span data-stu-id="e333d-218">Interval-based cascade selection uses a vector comparison and a dot product to determine the correct cacade.</span></span> <span data-ttu-id="e333d-219">O \_ sinalizador contagem em cascata \_ especifica o número de cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-219">The CASCADE\_COUNT\_FLAG specifies the number of cascades.</span></span> <span data-ttu-id="e333d-220">Os \_ dados m fCascadeFrustumsEyeSpaceDepths \_ restringem a exibição de partições frustum.</span><span class="sxs-lookup"><span data-stu-id="e333d-220">The m\_fCascadeFrustumsEyeSpaceDepths\_data constrains the view frustum partitions.</span></span> <span data-ttu-id="e333d-221">Após a comparação, o fComparison contém um valor de 1 em que o pixel atual é maior que a barreira e um valor de 0 quando a cascata atual é menor.</span><span class="sxs-lookup"><span data-stu-id="e333d-221">After the comparison, the fComparison contains a value of 1 where the current pixel is larger than the barrier, and a value of 0 when the current cascade is smaller.</span></span> <span data-ttu-id="e333d-222">Um produto de ponto soma esses valores em um índice de matriz.</span><span class="sxs-lookup"><span data-stu-id="e333d-222">A dot product sums these values into an array index.</span></span>


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



<span data-ttu-id="e333d-223">Depois que a cascata é selecionada, a coordenada de textura deve ser transformada na cascata correta.</span><span class="sxs-lookup"><span data-stu-id="e333d-223">Once the cascade is selected, the texture coordinate must be transformed to the correct cascade.</span></span>


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



<span data-ttu-id="e333d-224">Essa coordenada de textura é usada para exemplificar a textura com a coordenada X e a coordenada Y.</span><span class="sxs-lookup"><span data-stu-id="e333d-224">This texture coordinate is then used to sample the texture with the X-coordinate and the Y-coordinate.</span></span> <span data-ttu-id="e333d-225">A coordenada Z é usada para fazer a comparação de profundidade final.</span><span class="sxs-lookup"><span data-stu-id="e333d-225">The Z-coordinate is used to do the final depth comparison.</span></span>

### <a name="map-based-cascade-selection"></a><span data-ttu-id="e333d-226">Map-Based seleção em cascata</span><span class="sxs-lookup"><span data-stu-id="e333d-226">Map-Based Cascade Selection</span></span>

<span data-ttu-id="e333d-227">A seleção baseada em mapa (Figura 8) testa os quatro lados da cascata para encontrar o mapa mais rígido que cobre o pixel específico.</span><span class="sxs-lookup"><span data-stu-id="e333d-227">Map-based selection (Figure 8) tests against the four sides of the cascades to find the tightest map that covers the specific pixel.</span></span> <span data-ttu-id="e333d-228">Em vez de calcular a posição no espaço de mundo, o sombreador de vértice calcula a posição do espaço de exibição para cada cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-228">Instead of calculating the position in world space, the vertex shader calculates the view-space position for every cascade.</span></span> <span data-ttu-id="e333d-229">O sombreador de pixel itera em cascata a fim de dimensionar e deslocar as coordenadas de textura para que elas indexem a cascata atual.</span><span class="sxs-lookup"><span data-stu-id="e333d-229">The pixel shader iterates over the cascades in order to scale and shift the texture coordinates so that they index the current cascade.</span></span> <span data-ttu-id="e333d-230">A coordenada de textura é então testada em relação aos limites de textura.</span><span class="sxs-lookup"><span data-stu-id="e333d-230">The texture coordinate is then tested against the texture bounds.</span></span> <span data-ttu-id="e333d-231">Quando os valores X e Y da coordenada de textura se enquadram dentro de uma cascata, eles são usados para exemplificar a textura.</span><span class="sxs-lookup"><span data-stu-id="e333d-231">When the X and Y values of the texture coordinate fall inside a cascade, they are used to sample the texture.</span></span> <span data-ttu-id="e333d-232">A coordenada Z é usada para fazer a comparação de profundidade final.</span><span class="sxs-lookup"><span data-stu-id="e333d-232">The Z-coordinate is used to do the final depth comparison.</span></span>

<span data-ttu-id="e333d-233">**Figura 8. Seleção de cascata baseada em mapa**</span><span class="sxs-lookup"><span data-stu-id="e333d-233">**Figure 8. Map-based cascade selection**</span></span>

![seleção de cascata baseada em mapa](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a><span data-ttu-id="e333d-235">Seleção de Interval-Based de seleção versus Map-Based</span><span class="sxs-lookup"><span data-stu-id="e333d-235">Interval-Based Selection vs. Map-Based Selection</span></span>

<span data-ttu-id="e333d-236">A seleção baseada em intervalo é ligeiramente mais rápida que a seleção baseada em mapa porque a seleção em cascata pode ser feita diretamente.</span><span class="sxs-lookup"><span data-stu-id="e333d-236">Interval-based selection is slightly faster than map-based selection because the cascade selection can be done directly.</span></span> <span data-ttu-id="e333d-237">A seleção baseada em mapa deve interceptar a coordenada de textura com os limites em cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-237">Map-based selection must intersect the texture coordinate with the cascade bounds.</span></span>

<span data-ttu-id="e333d-238">A seleção baseada em mapa usa a cascata com mais eficiência quando mapas de sombra não se alinham perfeitamente (veja a Figura 8).</span><span class="sxs-lookup"><span data-stu-id="e333d-238">Map-based selection uses the cascade more efficiently when shadow maps do not align perfectly (see Figure 8).</span></span>

## <a name="blend-between-cascades"></a><span data-ttu-id="e333d-239">Misturar entre cascata</span><span class="sxs-lookup"><span data-stu-id="e333d-239">Blend between Cascades</span></span>

<span data-ttu-id="e333d-240">VSMs (discutido mais adiante neste artigo) e técnicas de filtragem, como PCF, podem ser usadas com CSMs de baixa resolução para produzir sombras suaves.</span><span class="sxs-lookup"><span data-stu-id="e333d-240">VSMs (discussed later in this article) and filtering techniques such as PCF can be used with low-resolution CSMs to produce soft shadows.</span></span> <span data-ttu-id="e333d-241">Infelizmente, isso resulta em uma fenda visível (Figura 9) entre as camadas em cascata porque a resolução não corresponde.</span><span class="sxs-lookup"><span data-stu-id="e333d-241">Unfortunately, this results in a visible seam (Figure 9) between cascade layers because the resolution does not match.</span></span> <span data-ttu-id="e333d-242">A solução é criar uma banda entre mapas de sombra em que o teste de sombra é executado para ambas as cascatas.</span><span class="sxs-lookup"><span data-stu-id="e333d-242">The solution is to create a band between shadow maps where the shadow test is performed for both cascades.</span></span> <span data-ttu-id="e333d-243">Em seguida, o sombreador interpola linearmente entre os dois valores com base na localização do pixel na banda do Blend.</span><span class="sxs-lookup"><span data-stu-id="e333d-243">The shader then linearly interpolates between the two values based on the pixel's location in the blend band.</span></span> <span data-ttu-id="e333d-244">Os exemplos CascadedShadowMaps11 e VarianceShadows11 fornecem um controle deslizante de GUI que pode ser usado para aumentar e diminuir essa faixa de desfoque.</span><span class="sxs-lookup"><span data-stu-id="e333d-244">The samples CascadedShadowMaps11 and VarianceShadows11 provide a GUI slider that can be used to increase and decrease this blur band.</span></span> <span data-ttu-id="e333d-245">O sombreador executa uma ramificação dinâmica para que a grande maioria dos pixels só Leia da cascata atual.</span><span class="sxs-lookup"><span data-stu-id="e333d-245">The shader performs a dynamic branch so that the vast majority of pixels only read from the current cascade.</span></span>

<span data-ttu-id="e333d-246">**Figura 9. Fendas em cascata**</span><span class="sxs-lookup"><span data-stu-id="e333d-246">**Figure 9. Cascade seams**</span></span>

![fendas em cascata](images/cascade-seams.jpg)

<span data-ttu-id="e333d-248">Mantida Uma fenda visível pode ser vista onde as cascatas se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="e333d-248">(Left) A visible seam can be seen where cascades overlap.</span></span> <span data-ttu-id="e333d-249">Adequada Quando as cascatas são mescladas entre, nenhuma fenda ocorre.</span><span class="sxs-lookup"><span data-stu-id="e333d-249">(Right) When the cascades are blended between, no seam occurs.</span></span>

## <a name="filtering-shadow-maps"></a><span data-ttu-id="e333d-250">Filtrando mapas de sombra</span><span class="sxs-lookup"><span data-stu-id="e333d-250">Filtering Shadow Maps</span></span>

### <a name="pcf"></a><span data-ttu-id="e333d-251">PCF</span><span class="sxs-lookup"><span data-stu-id="e333d-251">PCF</span></span>

<span data-ttu-id="e333d-252">A filtragem de mapas de sombra comuns não produz sombras suaves e borradas.</span><span class="sxs-lookup"><span data-stu-id="e333d-252">Filtering ordinary shadow maps does not produce soft, blurred shadows.</span></span> <span data-ttu-id="e333d-253">O hardware de filtragem desfoca os valores de profundidade e, em seguida, compara esses valores borrados com o Texel de espaço claro.</span><span class="sxs-lookup"><span data-stu-id="e333d-253">The filtering hardware blurs the depth values, and then compares those blurred values to the light space texel.</span></span> <span data-ttu-id="e333d-254">A borda rígida resultante do teste de aprovação/reprovação ainda existe.</span><span class="sxs-lookup"><span data-stu-id="e333d-254">The hard edge resulting from the pass/fail test still exists.</span></span> <span data-ttu-id="e333d-255">O desfoque de mapas de sombra só serve para mover erroneamente a borda rígida.</span><span class="sxs-lookup"><span data-stu-id="e333d-255">Blurring shadow maps only serves to erroneously move the hard edge.</span></span> <span data-ttu-id="e333d-256">PCF habilita a filtragem em mapas de sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-256">PCF enables filtering on shadow maps.</span></span> <span data-ttu-id="e333d-257">A ideia geral do PCF é calcular uma porcentagem do pixel em sombra com base no número de subamostras que passam o teste de profundidade sobre o número total de subamostras.</span><span class="sxs-lookup"><span data-stu-id="e333d-257">The general idea of PCF is to calculate a percentage of the pixel in shadow based on the number of subsamples that pass the depth test over the total number of subsamples.</span></span>

<span data-ttu-id="e333d-258">O hardware do Direct3D 10 e do Direct3D 11 pode executar o PCF.</span><span class="sxs-lookup"><span data-stu-id="e333d-258">Direct3D 10 and Direct3D 11 hardware can perform PCF.</span></span> <span data-ttu-id="e333d-259">A entrada para uma amostra de PCF consiste na coordenada de textura e em um valor de profundidade de comparação.</span><span class="sxs-lookup"><span data-stu-id="e333d-259">The input to a PCF sampler consists of the texture-coordinate and a comparison depth value.</span></span> <span data-ttu-id="e333d-260">Para simplificar, o PCF é explicado com um filtro com quatro toques.</span><span class="sxs-lookup"><span data-stu-id="e333d-260">For simplicity, PCF is explained with a four-tap filter.</span></span> <span data-ttu-id="e333d-261">O amostra de textura lê a textura quatro vezes, semelhante a um filtro padrão.</span><span class="sxs-lookup"><span data-stu-id="e333d-261">The texture sampler reads the texture four times, similar to a standard filter.</span></span> <span data-ttu-id="e333d-262">No entanto, o resultado retornado é uma porcentagem dos pixels que passaram no teste de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-262">However, the returned result is a percentage of the pixels that passed the depth test.</span></span> <span data-ttu-id="e333d-263">A Figura 10 mostra como um pixel que passa um dos quatro testes de profundidade é 25% em sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-263">Figure 10 shows how a pixel that passes one of the four depth tests is 25 percent in shadow.</span></span> <span data-ttu-id="e333d-264">O valor real retornado é uma interpolação linear baseada nas coordenadas de subtexel das leituras de textura para produzir um gradiente suave.</span><span class="sxs-lookup"><span data-stu-id="e333d-264">The actual value returned is a linear interpolation based on the subtexel coordinates of the texture reads to produce a smooth gradient.</span></span> <span data-ttu-id="e333d-265">Sem essa interpolação linear, o PCF de quatro toques só poderá retornar cinco valores: {0,0, 0,25, 0,5, 0,75, 1,0}.</span><span class="sxs-lookup"><span data-stu-id="e333d-265">Without this linear interpolation, the four-tap PCF would only be able to return five values: { 0.0, 0.25, 0.5, 0.75, 1.0 }.</span></span>

<span data-ttu-id="e333d-266">**Figura 10. Imagem filtrada de PCF, com 25% do pixel selecionado coberto**</span><span class="sxs-lookup"><span data-stu-id="e333d-266">**Figure 10. PCF filtered image, with 25 percent of the selected pixel covered**</span></span>

![imagem filtrada de PCF, com 25% do pixel selecionado coberto](images/pcf-filtered-image.png)

<span data-ttu-id="e333d-268">Também é possível fazer o PCF sem suporte a hardware ou estender o PCF para kernels maiores.</span><span class="sxs-lookup"><span data-stu-id="e333d-268">It is also possible to do PCF without hardware support or extend PCF to larger kernels.</span></span> <span data-ttu-id="e333d-269">Algumas técnicas até amostram com um kernel ponderado.</span><span class="sxs-lookup"><span data-stu-id="e333d-269">Some techniques even sample with a weighted kernel.</span></span> <span data-ttu-id="e333d-270">Para fazer isso, crie um kernel (como um gaussiano) para uma grade N × N.</span><span class="sxs-lookup"><span data-stu-id="e333d-270">To do this, create a kernel (such as a Gaussian) for an N × N grid.</span></span> <span data-ttu-id="e333d-271">Os pesos devem somar até 1.</span><span class="sxs-lookup"><span data-stu-id="e333d-271">The weights must add up to 1.</span></span> <span data-ttu-id="e333d-272">Em seguida, a textura é seguida por amostras de N2.</span><span class="sxs-lookup"><span data-stu-id="e333d-272">The texture is then sampled N2 times.</span></span> <span data-ttu-id="e333d-273">Cada amostra é dimensionada pelos pesos correspondentes no kernel.</span><span class="sxs-lookup"><span data-stu-id="e333d-273">Each sample is scaled by the corresponding weights in the kernel.</span></span> <span data-ttu-id="e333d-274">O exemplo CascadedShadowMaps11 usa essa abordagem.</span><span class="sxs-lookup"><span data-stu-id="e333d-274">The CascadedShadowMaps11 sample uses this approach.</span></span>

### <a name="depth-bias"></a><span data-ttu-id="e333d-275">Tendência de profundidade</span><span class="sxs-lookup"><span data-stu-id="e333d-275">Depth Bias</span></span>

<span data-ttu-id="e333d-276">A tendência de profundidade se torna ainda mais importante quando kernels PCF grandes são usados.</span><span class="sxs-lookup"><span data-stu-id="e333d-276">Depth bias becomes even more important when large PCF kernels are used.</span></span> <span data-ttu-id="e333d-277">Ele só é válido para comparar a profundidade de espaço leve de um pixel em relação ao pixel que mapeia para o mapa de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-277">It is only valid to compare a pixel's light-space depth against the pixel it maps to in the depth map.</span></span> <span data-ttu-id="e333d-278">Os vizinhos do mapa de profundidade do Texel se referem a uma posição diferente.</span><span class="sxs-lookup"><span data-stu-id="e333d-278">The depth map texel's neighbors refer to a different position.</span></span> <span data-ttu-id="e333d-279">Essa profundidade provavelmente será semelhante, mas pode ser muito diferente dependendo da cena.</span><span class="sxs-lookup"><span data-stu-id="e333d-279">This depth is likely to be similar, but can be very different depending on the scene.</span></span> <span data-ttu-id="e333d-280">A Figura 11 realça os artefatos que ocorrem.</span><span class="sxs-lookup"><span data-stu-id="e333d-280">Figure 11 highlights the artifacts that occur.</span></span> <span data-ttu-id="e333d-281">Uma única profundidade é comparada a três texels vizinhas no mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-281">A single depth is compared to three neighboring texels in the shadow map.</span></span> <span data-ttu-id="e333d-282">Um dos testes de profundidade falha erroneamente porque sua profundidade não se correlaciona com a profundidade de espaço claro computada da geometria atual.</span><span class="sxs-lookup"><span data-stu-id="e333d-282">One of the depth tests erroneously fails because its depth does not correlate to the computed light-space depth of the current geometry.</span></span> <span data-ttu-id="e333d-283">A solução recomendada para esse problema é usar um deslocamento maior.</span><span class="sxs-lookup"><span data-stu-id="e333d-283">The recommended solution to this problem is to use a larger offset.</span></span> <span data-ttu-id="e333d-284">No entanto, muito grande parte de um deslocamento pode resultar em Peter panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e333d-284">Too large of an offset, however, can result in Peter Panning.</span></span> <span data-ttu-id="e333d-285">Calcular um grande plano próximo e plano distante ajuda a reduzir os efeitos do uso de um deslocamento.</span><span class="sxs-lookup"><span data-stu-id="e333d-285">Calculating a tight near plane and far plane helps reduce the effects of using an offset.</span></span>

<span data-ttu-id="e333d-286">**Figura 11. Auto-sombreamento errôneo**</span><span class="sxs-lookup"><span data-stu-id="e333d-286">**Figure 11. Erroneous self-shadowing**</span></span>

![auto-sombreamento errôneo](images/erroneous-self-shadowing.png)

<span data-ttu-id="e333d-288">Os resultados de sombreamento automático errôneos da comparação de pixels na profundidade de espaço leve para o texels no mapa de sombra que não se correlacionam.</span><span class="sxs-lookup"><span data-stu-id="e333d-288">The erroneous self-shadowing results from comparing pixels in the light-space depth to the texels in the shadow map that do not correlate.</span></span> <span data-ttu-id="e333d-289">A profundidade em espaço leve se correlaciona com a sombra Texel 2 no mapa de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-289">The depth in light-space correlates to shadow texel 2 in the depth map.</span></span> <span data-ttu-id="e333d-290">Texel 1 é maior que a intensidade de espaço leve, enquanto 2 é igual e 3 é menor.</span><span class="sxs-lookup"><span data-stu-id="e333d-290">Texel 1 is greater than the light-space depth while 2 is equal and 3 is less.</span></span> <span data-ttu-id="e333d-291">Texels 2 e 3 passam o teste de profundidade, enquanto o Texel 1 falha.</span><span class="sxs-lookup"><span data-stu-id="e333d-291">Texels 2 and 3 pass the depth test, while Texel 1 fails.</span></span>

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a><span data-ttu-id="e333d-292">Calculando uma tendência de profundidade de Per-Texel com campo DDX e DDY para grandes PCFs</span><span class="sxs-lookup"><span data-stu-id="e333d-292">Calculating a Per-Texel Depth Bias with DDX and DDY for Large PCFs</span></span>

<span data-ttu-id="e333d-293">Calcular uma tendência de profundidade por Texel com **campo DDX** e **ddy** para grandes PCFs é uma técnica que calcula a tendência de profundidade correta — pressupondo que a superfície seja planar — para o mapa de sombra adjacente Texel.</span><span class="sxs-lookup"><span data-stu-id="e333d-293">Calculating a per texel depth bias with **ddx** and **ddy** for large PCFs is a technique that calculates the correct depth bias—assuming the surface is planar—for the adjacent shadow map texel.</span></span>

<span data-ttu-id="e333d-294">Essa técnica se adapta à profundidade de comparação a um plano usando as informações derivadas.</span><span class="sxs-lookup"><span data-stu-id="e333d-294">This technique fits the comparison depth to a plane using the derivative information.</span></span> <span data-ttu-id="e333d-295">Como essa técnica é computacionalmente complexa, ela deve ser usada somente quando uma GPU tiver ciclos de computação para spare.</span><span class="sxs-lookup"><span data-stu-id="e333d-295">Because this technique is computationally complex, it should be used only when a GPU has compute cycles to spare.</span></span> <span data-ttu-id="e333d-296">Quando kernels muito grandes são usados, essa pode ser a única técnica que funciona para remover artefatos de sombreamento automático sem causar o Peter panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e333d-296">When very large kernels are used, this may be the only technique that works to remove self-shadowing artifacts without causing Peter Panning.</span></span>

<span data-ttu-id="e333d-297">A Figura 12 realça o problema.</span><span class="sxs-lookup"><span data-stu-id="e333d-297">Figure 12 highlights the problem.</span></span> <span data-ttu-id="e333d-298">A profundidade no espaço leve é conhecida por um Texel que está sendo comparado.</span><span class="sxs-lookup"><span data-stu-id="e333d-298">The depth in light-space is known for the one texel that is being compared.</span></span> <span data-ttu-id="e333d-299">As profundidades de espaço leve que correspondem ao texels vizinho no mapa de profundidade são desconhecidas.</span><span class="sxs-lookup"><span data-stu-id="e333d-299">The light-space depths that correspond to the neighboring texels in the depth map are unknown.</span></span>

<span data-ttu-id="e333d-300">**Figura 12. Mapa de cena e profundidade**</span><span class="sxs-lookup"><span data-stu-id="e333d-300">**Figure 12. Scene and depth map**</span></span>

![mapa de cena e profundidade](images/scene-and-depth-map.png)

<span data-ttu-id="e333d-302">A cena renderizada é mostrada à esquerda e o mapa de profundidade com um bloco Texel de exemplo é mostrado à direita.</span><span class="sxs-lookup"><span data-stu-id="e333d-302">The rendered scene is shown at left, and the depth map with a sample texel block is shown at right.</span></span> <span data-ttu-id="e333d-303">O Texel de espaço de olho é mapeado para o pixel rotulado como D no centro do bloco.</span><span class="sxs-lookup"><span data-stu-id="e333d-303">The eye-space texel maps to the pixel labeled D in the center of the block.</span></span> <span data-ttu-id="e333d-304">Essa comparação é precisa.</span><span class="sxs-lookup"><span data-stu-id="e333d-304">This comparison is accurate.</span></span> <span data-ttu-id="e333d-305">A profundidade correta no espaço de olho que se correlaciona com os pixels que o vizinho D é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e333d-305">The correct depth in eye space correlating to the pixels that neighbor D is unknown.</span></span> <span data-ttu-id="e333d-306">O mapeamento do texels vizinho de volta para o espaço de olho só será possível se considerarmos que o pixel pertence ao mesmo triângulo que D.</span><span class="sxs-lookup"><span data-stu-id="e333d-306">Mapping the neighboring texels back to eye space is possible only if we assume the pixel pertains to the same triangle as D.</span></span>

<span data-ttu-id="e333d-307">A profundidade é conhecida pelo Texel que se correlaciona com a posição de espaço leve.</span><span class="sxs-lookup"><span data-stu-id="e333d-307">The depth is known for the texel that correlates with the light-space position.</span></span> <span data-ttu-id="e333d-308">A profundidade é desconhecida para o texels vizinho no mapa de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-308">The depth is unknown for the neighboring texels in the depth map.</span></span>

<span data-ttu-id="e333d-309">Em um alto nível, essa técnica usa as operações HLSL **campo DDX** e **ddy** para encontrar a derivação da posição de espaço leve.</span><span class="sxs-lookup"><span data-stu-id="e333d-309">At a high level, this technique uses the **ddx** and **ddy** HLSL operations to find the derivative of the light-space position.</span></span> <span data-ttu-id="e333d-310">Isso não é trivial porque as operações derivadas retornam o gradiente da profundidade de espaço leve em relação ao espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="e333d-310">This is nontrivial because the derivative operations return the gradient of the light-space depth with respect to screen space.</span></span> <span data-ttu-id="e333d-311">Para converter isso em um gradiente da profundidade de espaço leve em relação ao espaço leve, uma matriz de conversão deve ser calculada.</span><span class="sxs-lookup"><span data-stu-id="e333d-311">To convert this to a gradient of the light-space depth with respect to light space, a conversion matrix must be calculated.</span></span>

### <a name="explanation-with-shader-code"></a><span data-ttu-id="e333d-312">Explicação com código de sombreador</span><span class="sxs-lookup"><span data-stu-id="e333d-312">Explanation with Shader Code</span></span>

<span data-ttu-id="e333d-313">Os detalhes do restante do algoritmo são fornecidos como uma explicação do código do sombreador que executa essa operação.</span><span class="sxs-lookup"><span data-stu-id="e333d-313">The details of the rest of the algorithm are given as an explanation of the shader code that performs this operation.</span></span> <span data-ttu-id="e333d-314">Esse código pode ser encontrado no exemplo CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="e333d-314">This code can be found in the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="e333d-315">A Figura 13 mostra como as coordenadas de textura de espaço leve são mapeadas para o mapa de profundidade e como as derivações em X e Y podem ser usadas para criar uma matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="e333d-315">Figure 13 shows how the light-space texture coordinates map to the depth map and how the derivatives in X and Y can be used to create a transformation matrix.</span></span>

<span data-ttu-id="e333d-316">**Figura 13. Espaço de tela para matriz de espaço leve**</span><span class="sxs-lookup"><span data-stu-id="e333d-316">**Figure 13. Screen-space to light-space matrix**</span></span>

![espaço de tela para matriz de espaço leve](images/screen-space-to-light-space-matrix.png)

<span data-ttu-id="e333d-318">Os derivativos da posição de espaço leve em X e Y são usados para criar essa matriz.</span><span class="sxs-lookup"><span data-stu-id="e333d-318">The derivatives of the light-space position in X and Y are used to create this matrix.</span></span>

<span data-ttu-id="e333d-319">A primeira etapa é calcular o derivativo da posição de exibição clara.</span><span class="sxs-lookup"><span data-stu-id="e333d-319">The first step is to calculate the derivative of the light-view-space position.</span></span>


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



<span data-ttu-id="e333d-320">As GPUs de classe do Direct3D 11 calculam esses derivativos executando 2 × 2 quatro pixels em paralelo e subtraindo as coordenadas de textura do vizinho em X para **campo DDX** e do vizinho em Y para **ddy**.</span><span class="sxs-lookup"><span data-stu-id="e333d-320">Direct3D 11 class GPUs calculate these derivatives by running 2 × 2 quad of pixels in parallel and subtracting the texture coordinates from the neighbor in X for **ddx** and from the neighbor in Y for **ddy**.</span></span> <span data-ttu-id="e333d-321">Esses dois derivativos compõem as linhas de uma matriz 2 × 2.</span><span class="sxs-lookup"><span data-stu-id="e333d-321">These two derivatives make up the rows of a 2 × 2 matrix.</span></span> <span data-ttu-id="e333d-322">Em sua forma atual, essa matriz poderia ser usada para converter pixels vizinhos de espaço na tela em interrupções de espaço leve.</span><span class="sxs-lookup"><span data-stu-id="e333d-322">In its current form, this matrix could be used to convert screen-space neighboring pixels to light-space slopes.</span></span> <span data-ttu-id="e333d-323">No entanto, o inverso dessa matriz é necessário.</span><span class="sxs-lookup"><span data-stu-id="e333d-323">However, the inverse of this matrix is needed.</span></span> <span data-ttu-id="e333d-324">Uma matriz que transforma os pixels vizinhos de espaço leve em inclinação de espaço na tela é necessária.</span><span class="sxs-lookup"><span data-stu-id="e333d-324">A matrix that transforms light-space neighboring pixels to screen-space slopes is needed.</span></span>


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



<span data-ttu-id="e333d-325">**Figura 14. Espaço leve para a tela-espaço**</span><span class="sxs-lookup"><span data-stu-id="e333d-325">**Figure 14. Light-space to screen-space**</span></span>

![espaço leve para a tela-espaço](images/light-space-to-screen-space.png)

<span data-ttu-id="e333d-327">Essa matriz é usada para transformar as duas texels acima e à direita da Texel atual.</span><span class="sxs-lookup"><span data-stu-id="e333d-327">This matrix is then used to transform the two texels above and to the right of the current texel.</span></span> <span data-ttu-id="e333d-328">Esses vizinhos são representados como um deslocamento do Texel atual.</span><span class="sxs-lookup"><span data-stu-id="e333d-328">These neighbors are represented as an offset from the current texel.</span></span>


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



<span data-ttu-id="e333d-329">A proporção que a matriz cria é, por fim, multiplicada pelas derivações de profundidade para calcular os deslocamentos de profundidade para os pixels vizinhos.</span><span class="sxs-lookup"><span data-stu-id="e333d-329">The ratio that the matrix creates is finally multiplied by the depth derivatives to calculate the depth offsets for the neighboring pixels.</span></span>


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



<span data-ttu-id="e333d-330">Esses pesos agora podem ser usados em um loop PCF para adicionar um deslocamento à posição.</span><span class="sxs-lookup"><span data-stu-id="e333d-330">These weights can now be used in a PCF loop to add an offset to the position.</span></span>


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a><span data-ttu-id="e333d-331">PCF e CSMs</span><span class="sxs-lookup"><span data-stu-id="e333d-331">PCF and CSMs</span></span>

<span data-ttu-id="e333d-332">O PCF não funciona em matrizes de textura no Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="e333d-332">PCF does not work on texture arrays in Direct3D 10.</span></span> <span data-ttu-id="e333d-333">Para usar o PCF, todas as cascata são armazenadas em um Atlas de textura grande.</span><span class="sxs-lookup"><span data-stu-id="e333d-333">To use PCF, all of the cascades are stored in one large texture atlas.</span></span>

### <a name="derivative-based-offset"></a><span data-ttu-id="e333d-334">Deslocamento de Derivative-Based</span><span class="sxs-lookup"><span data-stu-id="e333d-334">Derivative-Based Offset</span></span>

<span data-ttu-id="e333d-335">A adição dos deslocamentos baseados em derivações para CSMs apresenta alguns desafios.</span><span class="sxs-lookup"><span data-stu-id="e333d-335">Adding the derivative based offsets for CSMs presents some challenges.</span></span> <span data-ttu-id="e333d-336">Isso ocorre devido a um cálculo derivado dentro do controle de fluxo divergente.</span><span class="sxs-lookup"><span data-stu-id="e333d-336">This is due to a derivative calculation within divergent flow control.</span></span> <span data-ttu-id="e333d-337">O problema ocorre devido a uma maneira fundamental de operar as GPUs.</span><span class="sxs-lookup"><span data-stu-id="e333d-337">The problem occurs because of a fundamental way that GPUs operate.</span></span> <span data-ttu-id="e333d-338">As GPUs Direct3D11 operam em 2 × 2 quatro processadores de pixels.</span><span class="sxs-lookup"><span data-stu-id="e333d-338">Direct3D11 GPUs operate on 2 × 2 quads of pixels.</span></span> <span data-ttu-id="e333d-339">Para executar um derivativo, as GPUs geralmente subtraim a cópia do pixel atual de uma variável da cópia do pixel vizinho da mesma variável.</span><span class="sxs-lookup"><span data-stu-id="e333d-339">To perform a derivative, GPUs generally subtract the current pixel's copy of a variable from the neighboring pixel's copy of that same variable.</span></span> <span data-ttu-id="e333d-340">Como isso acontece varia de GPU para GPU.</span><span class="sxs-lookup"><span data-stu-id="e333d-340">How this happens varies from GPU to GPU.</span></span> <span data-ttu-id="e333d-341">As coordenadas de textura são determinadas por seleção baseada em mapa ou em cascata baseada em intervalo.</span><span class="sxs-lookup"><span data-stu-id="e333d-341">The texture coordinates are determined by map-based or interval-based cascade selection.</span></span> <span data-ttu-id="e333d-342">Alguns pixels em um pixel Quad escolhem uma cascata diferente do restante dos pixels.</span><span class="sxs-lookup"><span data-stu-id="e333d-342">Some pixels in a pixel quad choose a different cascade than the rest of the pixels.</span></span> <span data-ttu-id="e333d-343">Isso resulta em emendas visíveis entre mapas de sombra porque os deslocamentos com base em derivação agora estão completamente errados.</span><span class="sxs-lookup"><span data-stu-id="e333d-343">This results in visible seams between shadow maps because the derivative-based offsets are now completely wrong.</span></span> <span data-ttu-id="e333d-344">A solução é executar o derivativo em coordenadas de textura de espaço de exibição clara.</span><span class="sxs-lookup"><span data-stu-id="e333d-344">The solution is to perform the derivative on light-view space texture coordinates.</span></span> <span data-ttu-id="e333d-345">Essas coordenadas são as mesmas para cada cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-345">These coordinates are the same for every cascade.</span></span>

### <a name="padding-for-pcf-kernels"></a><span data-ttu-id="e333d-346">Preenchimento de kernels PCF</span><span class="sxs-lookup"><span data-stu-id="e333d-346">Padding for PCF Kernels</span></span>

<span data-ttu-id="e333d-347">Índice de kernels PCF fora de uma partição em cascata se o buffer de sombra não for preenchido.</span><span class="sxs-lookup"><span data-stu-id="e333d-347">PCF kernels index outside of a cascade partition if the shadow buffer is not padded.</span></span> <span data-ttu-id="e333d-348">A solução é preencher a borda externa da cascata por uma metade do tamanho do kernel PCF.</span><span class="sxs-lookup"><span data-stu-id="e333d-348">The solution is to pad the outer rim of the cascade by one-half the size of the PCF kernel.</span></span> <span data-ttu-id="e333d-349">Isso deve ser implementado no sombreador que seleciona a cascata e na matriz de projeção que deve renderizar a cascata grande o suficiente para que a borda seja preservada.</span><span class="sxs-lookup"><span data-stu-id="e333d-349">This must be implemented in the shader that selects the cascade and in the projection matrix that must render the cascade large enough that the border is preserved.</span></span>

## <a name="variance-shadow-maps"></a><span data-ttu-id="e333d-350">Mapas de sombra de variação</span><span class="sxs-lookup"><span data-stu-id="e333d-350">Variance Shadow Maps</span></span>

<span data-ttu-id="e333d-351">VSMs (consulte [variação de mapas de sombra](https://portal.acm.org/citation.cfm?doid=1111411.1111440) por Donnelly e Lauritzen para obter mais informações) habilitar Filtragem de mapa de sombra direta.</span><span class="sxs-lookup"><span data-stu-id="e333d-351">VSMs (see [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440) by Donnelly and Lauritzen for more information) enable direct shadow map filtering.</span></span> <span data-ttu-id="e333d-352">Ao usar o VSMs, toda a potência do hardware de filtragem de textura pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="e333d-352">When using VSMs, all of the power of the texture-filtering hardware can be used.</span></span> <span data-ttu-id="e333d-353">Triline e anisotropic (Figura 15) a filtragem pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="e333d-353">Trilinear and anisotropic (Figure 15) filtering can be used.</span></span> <span data-ttu-id="e333d-354">Além disso, VSMs pode ser borrado diretamente por meio de convolução.</span><span class="sxs-lookup"><span data-stu-id="e333d-354">Additionally, VSMs can be blurred directly through convolution.</span></span> <span data-ttu-id="e333d-355">VSMs têm algumas desvantagens; dois canais de dados de profundidade devem ser armazenados (profundidade e profundidade ao quadrado).</span><span class="sxs-lookup"><span data-stu-id="e333d-355">VSMs do have some drawbacks; two channels of depth data must be stored (depth and depth squared).</span></span> <span data-ttu-id="e333d-356">Quando as sombras se sobrepõem, o sangramento claro é comum.</span><span class="sxs-lookup"><span data-stu-id="e333d-356">When shadows overlap, light-bleeding is common.</span></span> <span data-ttu-id="e333d-357">No entanto, eles funcionam bem com resoluções mais baixas e podem ser combinados com CSMs.</span><span class="sxs-lookup"><span data-stu-id="e333d-357">They work well, however, with lower resolutions and can be combined with CSMs.</span></span>

<span data-ttu-id="e333d-358">**Figura 15. Filtragem de anisotropic**</span><span class="sxs-lookup"><span data-stu-id="e333d-358">**Figure 15. Anisotropic filtering**</span></span>

![filtragem de anisotropic](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a><span data-ttu-id="e333d-360">Detalhes do algoritmo</span><span class="sxs-lookup"><span data-stu-id="e333d-360">Algorithm Details</span></span>

<span data-ttu-id="e333d-361">O VSMs funciona renderizando a profundidade e a profundidade quadrada em um mapa de sombra de dois canais.</span><span class="sxs-lookup"><span data-stu-id="e333d-361">VSMs work by rendering the depth and the depth squared to a two-channel shadow map.</span></span> <span data-ttu-id="e333d-362">Esse mapa de sombra de dois canais pode ser desfocado e filtrado da mesma forma que uma textura normal.</span><span class="sxs-lookup"><span data-stu-id="e333d-362">This two-channel shadow map can then be blurred and filtered just like a normal texture.</span></span> <span data-ttu-id="e333d-363">Em seguida, o algoritmo usa a desigualdade do Chebychev no sombreador de pixel para estimar a fração da área de pixel que passaria no teste de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-363">The algorithm then uses Chebychev's Inequality in the pixel shader to estimate the fraction of pixel area that would pass the depth test.</span></span>

<span data-ttu-id="e333d-364">O sombreador de pixel busca os valores de profundidade e de profundidade quadrada.</span><span class="sxs-lookup"><span data-stu-id="e333d-364">The pixel shader fetches the depth and depth-squared values.</span></span>


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



<span data-ttu-id="e333d-365">A comparação de profundidade é executada.</span><span class="sxs-lookup"><span data-stu-id="e333d-365">The depth comparison is performed.</span></span>


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



<span data-ttu-id="e333d-366">Se a comparação de profundidade falhar, a porcentagem do pixel que está acesa será estimada.</span><span class="sxs-lookup"><span data-stu-id="e333d-366">If the depth comparison fails, the percentage of the pixel that is lit is estimated.</span></span> <span data-ttu-id="e333d-367">A variação é calculada como média de quadrados menos o quadrado-de-média.</span><span class="sxs-lookup"><span data-stu-id="e333d-367">Variance is calculated as average-of-squares minus square-of-average.</span></span>


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



<span data-ttu-id="e333d-368">O valor fPercentLit é estimado com a desigualdade de Chebychev.</span><span class="sxs-lookup"><span data-stu-id="e333d-368">The fPercentLit value is estimated with Chebychev's Inequality.</span></span>


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a><span data-ttu-id="e333d-369">Sangramento claro</span><span class="sxs-lookup"><span data-stu-id="e333d-369">Light Bleeding</span></span>

<span data-ttu-id="e333d-370">A maior desvantagem do VSMs é o sangramento claro (Figura 16).</span><span class="sxs-lookup"><span data-stu-id="e333d-370">The biggest drawback to VSMs is light bleeding (Figure 16).</span></span> <span data-ttu-id="e333d-371">A perda de luz ocorre quando vários contornos de sombra se occludem entre bordas.</span><span class="sxs-lookup"><span data-stu-id="e333d-371">Light bleeding occurs when multiple shadow casters occlude each other along edges.</span></span> <span data-ttu-id="e333d-372">VSMs sombrear as bordas de sombras com base em diparidades de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-372">VSMs shade the edges of shadows based on depth disparities.</span></span> <span data-ttu-id="e333d-373">Quando as sombras se sobrepõem, há uma diparidade de profundidade no centro de uma região que deve ser sombreada.</span><span class="sxs-lookup"><span data-stu-id="e333d-373">When shadows overlap each other, a depth disparity exists in the center of a region that should be shadowed.</span></span> <span data-ttu-id="e333d-374">Isso é um problema com o uso do algoritmo VSM.</span><span class="sxs-lookup"><span data-stu-id="e333d-374">This is a problem with using the VSM algorithm.</span></span>

<span data-ttu-id="e333d-375">**Figura 16. Sangramento de VSM**</span><span class="sxs-lookup"><span data-stu-id="e333d-375">**Figure 16. VSM light bleeding**</span></span>

![sangramento de VSM](images/vsm-light-bleeding.png)

<span data-ttu-id="e333d-377">Uma solução parcial para o problema é elevar o fPercentLit a uma potência.</span><span class="sxs-lookup"><span data-stu-id="e333d-377">A partial solution to the problem is to raise the fPercentLit to a power.</span></span> <span data-ttu-id="e333d-378">Isso tem o efeito de retardar o desfoque, o que pode causar artefatos em que a diparidade de profundidade é pequena.</span><span class="sxs-lookup"><span data-stu-id="e333d-378">This has the effect of dampening the blur, which can cause artifacts where depth disparity is small.</span></span> <span data-ttu-id="e333d-379">Às vezes, existe um valor mágico que alivia o problema.</span><span class="sxs-lookup"><span data-stu-id="e333d-379">Sometimes there exists a magical value that alleviates the problem.</span></span>


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



<span data-ttu-id="e333d-380">Uma alternativa para elevar o percentual de aceso a uma potência é evitar configurações em que as sombras se sobrepõem.</span><span class="sxs-lookup"><span data-stu-id="e333d-380">An alternative to raising the percent lit to a power is to avoid configurations where shadows overlap.</span></span> <span data-ttu-id="e333d-381">Até mesmo as configurações de sombra altamente ajustadas têm várias restrições em luz, câmera e geometria.</span><span class="sxs-lookup"><span data-stu-id="e333d-381">Even highly tuned shadow configurations have several constraints on light, camera, and geometry.</span></span> <span data-ttu-id="e333d-382">O sangramento claro também é reduzido com o uso de texturas de resolução mais alta.</span><span class="sxs-lookup"><span data-stu-id="e333d-382">Light bleeding is also lessened by using higher resolution textures.</span></span>

<span data-ttu-id="e333d-383">Os mapas de sombra de variação em camadas (LVSMs) resolvem o problema às custas de dividir o frustum em camadas perpendiculares à luz.</span><span class="sxs-lookup"><span data-stu-id="e333d-383">Layered variance shadow maps (LVSMs) solve the problem at the expense of breaking the frustum into layers that are perpendicular to the light.</span></span> <span data-ttu-id="e333d-384">O número de mapas necessários seria muito grande quando CSMs também estão sendo usados.</span><span class="sxs-lookup"><span data-stu-id="e333d-384">The number of maps required would be quite large when CSMs are also being used.</span></span>

<span data-ttu-id="e333d-385">Além disso, Andrew Lauritzen, coautor do artigo sobre VSMs e autor de um papel em LVSMs, abordou a combinação de mapas de sombra exponencial (ESMs) com VSMs para neutralizar a mistura de luz em um [Fórum de Beyond3D](https://forum.beyond3d.com/showthread.php?t=47427).</span><span class="sxs-lookup"><span data-stu-id="e333d-385">Additionally, Andrew Lauritzen, co-author of the paper on VSMs, and author of a paper on LVSMs, discussed combining exponential shadow maps (ESMs) with VSMs to counteract light blending in a [Beyond3D Forum](https://forum.beyond3d.com/showthread.php?t=47427).</span></span>

## <a name="vsms-with-csms"></a><span data-ttu-id="e333d-386">VSMs com CSMs</span><span class="sxs-lookup"><span data-stu-id="e333d-386">VSMs with CSMs</span></span>

<span data-ttu-id="e333d-387">O exemplo VarianceShadow11 combina VSMs e CSMs.</span><span class="sxs-lookup"><span data-stu-id="e333d-387">The sample VarianceShadow11 combines VSMs and CSMs.</span></span> <span data-ttu-id="e333d-388">A combinação é razoavelmente simples.</span><span class="sxs-lookup"><span data-stu-id="e333d-388">The combination is fairly straightforward.</span></span> <span data-ttu-id="e333d-389">O exemplo segue as mesmas etapas do exemplo CascadedShadowMaps11.</span><span class="sxs-lookup"><span data-stu-id="e333d-389">The sample follows the same steps as the CascadedShadowMaps11 sample.</span></span> <span data-ttu-id="e333d-390">Como o PCF não é usado, as sombras são desfocadas em uma convolução separáveis de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="e333d-390">Because PCF is not used, the shadows are blurred in a two-pass separable convolution.</span></span> <span data-ttu-id="e333d-391">Não usar o PCF também permite que o exemplo use matrizes de textura em vez de um Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="e333d-391">Not using PCF also enables the sample to use texture arrays instead of a texture atlas.</span></span> <span data-ttu-id="e333d-392">O PCF em matrizes de textura é um recurso do Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="e333d-392">PCF on texture arrays is a Direct3D 10.1 feature.</span></span>

### <a name="gradients-with-csms"></a><span data-ttu-id="e333d-393">Gradientes com CSMs</span><span class="sxs-lookup"><span data-stu-id="e333d-393">Gradients with CSMs</span></span>

<span data-ttu-id="e333d-394">O uso de gradientes com CSMs pode produzir uma fenda ao longo da borda entre duas cascatas, como mostrado na figura 17.</span><span class="sxs-lookup"><span data-stu-id="e333d-394">Using gradients with CSMs can produce a seam along the border between two cascades as seen in Figure 17.</span></span> <span data-ttu-id="e333d-395">A instrução de exemplo usa derivações entre pixels para calcular informações, como o nível de mipmap, necessário para o filtro.</span><span class="sxs-lookup"><span data-stu-id="e333d-395">The sample instruction uses derivatives between pixels to calculate information, such as the mipmap level, needed by the filter.</span></span> <span data-ttu-id="e333d-396">Isso causa um problema em particular para a seleção de mipmap ou a filtragem de anisotropic.</span><span class="sxs-lookup"><span data-stu-id="e333d-396">This causes a problem in particular for mipmap selection or anisotropic filtering.</span></span> <span data-ttu-id="e333d-397">Quando os pixels em um quad usam ramificações diferentes no sombreador, os derivativos calculados pelo hardware da GPU são inválidos.</span><span class="sxs-lookup"><span data-stu-id="e333d-397">When pixels in a quad take different branches in the shader, the derivatives calculated by the GPU hardware are invalid.</span></span> <span data-ttu-id="e333d-398">Isso resulta em uma fenda denteada ao longo do mapa de sombra.</span><span class="sxs-lookup"><span data-stu-id="e333d-398">This results in a jagged seam along the shadow map.</span></span>

<span data-ttu-id="e333d-399">**Figura 17. Fendas em bordas em cascata devido à filtragem de anisotropic com controle de fluxo divergente**</span><span class="sxs-lookup"><span data-stu-id="e333d-399">**Figure 17. Seams on cascade borders due to anisotropic filtering with divergent flow control**</span></span>

![fendas em bordas em cascata devido à filtragem de anisotropic com controle de fluxo divergente](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

<span data-ttu-id="e333d-401">Esse problema é resolvido com a computação dos derivativos na posição no espaço de exibição clara; a coordenada de espaço de exibição clara não é específica para a cascata selecionada.</span><span class="sxs-lookup"><span data-stu-id="e333d-401">This problem is solved by computing the derivatives on the position in light-view space; the light-view space coordinate is not specific to the selected cascade.</span></span> <span data-ttu-id="e333d-402">As derivações computadas podem ser dimensionadas pela parte de escala da matriz de textura de projeção para o nível de mipmap correto.</span><span class="sxs-lookup"><span data-stu-id="e333d-402">The computed derivatives can be scaled by the scale portion of the projection-texture matrix to the correct mipmap level.</span></span>


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a><span data-ttu-id="e333d-403">VSMs em comparação com as sombras padrão com PCF</span><span class="sxs-lookup"><span data-stu-id="e333d-403">VSMs Compared to Standard Shadows with PCF</span></span>

<span data-ttu-id="e333d-404">VSMs e PCF tentam aproximar a fração da área de pixel que passaria no teste de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e333d-404">Both VSMs and PCF attempt to approximate the fraction of pixel area that would pass the depth test.</span></span> <span data-ttu-id="e333d-405">O VSMs trabalha com filtragem de hardware e pode ser desfocado com kernels do separáveis.</span><span class="sxs-lookup"><span data-stu-id="e333d-405">VSMs work with filtering hardware and can be blurred with separable kernels.</span></span> <span data-ttu-id="e333d-406">Os kernels de convolução separáveis são consideravelmente mais baratos de implementar do que um kernel completo.</span><span class="sxs-lookup"><span data-stu-id="e333d-406">Separable convolution kernels are considerably cheaper to implement than a full kernel.</span></span> <span data-ttu-id="e333d-407">Além disso, VSMs comparar uma profundidade de espaço leve em relação a um valor no mapa de profundidade de espaço claro.</span><span class="sxs-lookup"><span data-stu-id="e333d-407">Additionally, VSMs compare one light-space depth against one value in the light-space depth map.</span></span> <span data-ttu-id="e333d-408">Isso significa que o VSMs não tem os mesmos problemas de deslocamento que o PCF.</span><span class="sxs-lookup"><span data-stu-id="e333d-408">This means that VSMs do not have the same offset problems as PCF.</span></span> <span data-ttu-id="e333d-409">Tecnicamente, VSMs são profundidade de amostragem em uma área maior, bem como a execução de uma análise estatística.</span><span class="sxs-lookup"><span data-stu-id="e333d-409">Technically, VSMs are sampling depth over a greater area, as well as performing a statistical analysis.</span></span> <span data-ttu-id="e333d-410">Isso é menos preciso do que PCF.</span><span class="sxs-lookup"><span data-stu-id="e333d-410">This is less precise than PCF.</span></span> <span data-ttu-id="e333d-411">Na prática, o VSMs faz um trabalho muito bom de mesclagem, o que resulta em menos deslocamento necessário.</span><span class="sxs-lookup"><span data-stu-id="e333d-411">In practice, VSMs do a very good job of blending, which results in less offset being necessary.</span></span> <span data-ttu-id="e333d-412">Conforme descrito acima, a desvantagem do número um para VSMs é o sangramento claro.</span><span class="sxs-lookup"><span data-stu-id="e333d-412">As described above, the number one drawback to VSMs is light bleeding.</span></span>

<span data-ttu-id="e333d-413">VSMs e PCF representam uma compensação entre a potência de computação da GPU e a largura de banda da textura da GPU.</span><span class="sxs-lookup"><span data-stu-id="e333d-413">VSMs and PCF represent a trade-off between GPU compute power and GPU texture bandwidth.</span></span> <span data-ttu-id="e333d-414">VSMs exigem que mais matemática seja executada para calcular a variância.</span><span class="sxs-lookup"><span data-stu-id="e333d-414">VSMs require more math to be performed to calculate the variance.</span></span> <span data-ttu-id="e333d-415">PCF requer mais largura de banda de memória de textura.</span><span class="sxs-lookup"><span data-stu-id="e333d-415">PCF requires more texture memory bandwidth.</span></span> <span data-ttu-id="e333d-416">Os kernels PCF grandes podem rapidamente se tornar afunilados pela largura de banda da textura.</span><span class="sxs-lookup"><span data-stu-id="e333d-416">Large PCF kernels can quickly become bottlenecked by texture bandwidth.</span></span> <span data-ttu-id="e333d-417">Com o aumento de energia da GPU aumentando mais rapidamente do que a largura de banda da GPU, os VSMs estão se tornando mais práticos dos dois algoritmos.</span><span class="sxs-lookup"><span data-stu-id="e333d-417">With GPU computation power growing more rapidly than GPU bandwidth, VSMs are becoming the more practical of the two algorithms.</span></span> <span data-ttu-id="e333d-418">O VSMs também parece melhor com mapas de sombra de resolução mais baixa devido à mesclagem e filtragem.</span><span class="sxs-lookup"><span data-stu-id="e333d-418">VSMs also look better with lower resolution shadow maps due to blending and filtering.</span></span>

## <a name="summary"></a><span data-ttu-id="e333d-419">Resumo</span><span class="sxs-lookup"><span data-stu-id="e333d-419">Summary</span></span>

<span data-ttu-id="e333d-420">O CSMs oferece uma solução para o problema de alias de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="e333d-420">CSMs offer a solution to the perspective aliasing problem.</span></span> <span data-ttu-id="e333d-421">Há várias configurações possíveis para obter a fidelidade visual necessária para um título.</span><span class="sxs-lookup"><span data-stu-id="e333d-421">There are several possible configurations to get the needed visual fidelity for a title.</span></span> <span data-ttu-id="e333d-422">O PCF e o VSMs são amplamente usados e devem ser combinados com CSMs para reduzir o alias.</span><span class="sxs-lookup"><span data-stu-id="e333d-422">PCF and VSMs are widely used and should be combined with CSMs to reduce aliasing.</span></span>

## <a name="references"></a><span data-ttu-id="e333d-423">Referências</span><span class="sxs-lookup"><span data-stu-id="e333d-423">References</span></span>

<span data-ttu-id="e333d-424">Donnelly, W. e Lauritzen, os [mapas de sombra. variância](https://portal.acm.org/citation.cfm?doid=1111411.1111440).</span><span class="sxs-lookup"><span data-stu-id="e333d-424">Donnelly, W. and Lauritzen, A. [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440).</span></span> <span data-ttu-id="e333d-425">No SI3D ' 06: procedimentos do Symposium 2006 em jogos e gráficos 3D interativos.</span><span class="sxs-lookup"><span data-stu-id="e333d-425">In SI3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games.</span></span> <span data-ttu-id="e333d-426">2006.</span><span class="sxs-lookup"><span data-stu-id="e333d-426">2006.</span></span> <span data-ttu-id="e333d-427">PP. 161 – 165.</span><span class="sxs-lookup"><span data-stu-id="e333d-427">pp. 161–165.</span></span> <span data-ttu-id="e333d-428">Nova York, NY, EUA: ACM Press.</span><span class="sxs-lookup"><span data-stu-id="e333d-428">New York, NY, USA: ACM Press.</span></span>

<span data-ttu-id="e333d-429">Lauritzen, Andrew e McCool, Michael.</span><span class="sxs-lookup"><span data-stu-id="e333d-429">Lauritzen, Andrew and McCool, Michael.</span></span> <span data-ttu-id="e333d-430">[Mapas de sombra de variância em camadas](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992).</span><span class="sxs-lookup"><span data-stu-id="e333d-430">[Layered variance shadow maps](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992).</span></span> <span data-ttu-id="e333d-431">Procedimentos de interface gráfica 2008, 28 de maio, 2008, Windsor, Ontário, Canadá.</span><span class="sxs-lookup"><span data-stu-id="e333d-431">Proceedings of graphics interface 2008, May 28–30, 2008, Windsor, Ontario, Canada.</span></span>

<span data-ttu-id="e333d-432">Engel, Woflgang F. section 4.</span><span class="sxs-lookup"><span data-stu-id="e333d-432">Engel, Woflgang F. Section 4.</span></span> <span data-ttu-id="e333d-433">Mapas de sombra em cascata.</span><span class="sxs-lookup"><span data-stu-id="e333d-433">Cascaded Shadow Maps.</span></span> <span data-ttu-id="e333d-434">ShaderX5, técnicas de renderização avançadas, Wolfgang F. Engel, Ed.</span><span class="sxs-lookup"><span data-stu-id="e333d-434">ShaderX5 , Advanced Rendering Techniques, Wolfgang F. Engel, Ed.</span></span> <span data-ttu-id="e333d-435">Charles River Media, Boston, Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="e333d-435">Charles River Media, Boston, Massachusetts.</span></span> <span data-ttu-id="e333d-436">2006.</span><span class="sxs-lookup"><span data-stu-id="e333d-436">2006.</span></span> <span data-ttu-id="e333d-437">PP. 197 – 206.</span><span class="sxs-lookup"><span data-stu-id="e333d-437">pp. 197–206.</span></span>

 

 