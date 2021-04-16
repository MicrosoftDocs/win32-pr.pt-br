---
title: Inverter Modelo, retângulos sujos, áreas roladas
description: DXGI 1,2 dá suporte a uma nova cadeia de permuta de flip-Model, retângulos sujos e áreas roladas. Explicamos os benefícios de usar a nova cadeia de permuta de flip-Model e de otimizar a apresentação especificando retângulos sujos e áreas roladas.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "104571703"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a><span data-ttu-id="b9714-104">Inverter Modelo, retângulos sujos, áreas roladas</span><span class="sxs-lookup"><span data-stu-id="b9714-104">Flip model, dirty rectangles, scrolled areas</span></span>

<span data-ttu-id="b9714-105">DXGI 1,2 dá suporte a uma nova cadeia de permuta de flip-Model, retângulos sujos e áreas roladas.</span><span class="sxs-lookup"><span data-stu-id="b9714-105">DXGI 1.2 supports a new flip-model swap chain, dirty rectangles, and scrolled areas.</span></span> <span data-ttu-id="b9714-106">Explicamos os benefícios de usar a nova cadeia de permuta de flip-Model e de otimizar a apresentação especificando retângulos sujos e áreas roladas.</span><span class="sxs-lookup"><span data-stu-id="b9714-106">We explain the benefits of using the new flip-model swap chain and of optimizing presentation by specifying dirty rectangles and scrolled areas.</span></span>

## <a name="dxgi-flip-model-presentation"></a><span data-ttu-id="b9714-107">Apresentação de modelo de flip-DXGI</span><span class="sxs-lookup"><span data-stu-id="b9714-107">DXGI flip-model presentation</span></span>

<span data-ttu-id="b9714-108">DXGI 1,2 adiciona suporte para o modelo de apresentação de flip para Direct3D 10 e APIs posteriores.</span><span class="sxs-lookup"><span data-stu-id="b9714-108">DXGI 1.2 adds support for the flip presentation model for Direct3D 10 and later APIs.</span></span> <span data-ttu-id="b9714-109">No Windows 7, o Direct3D 9EX primeiro adotou a [apresentação de flip-Model](../direct3darticles/direct3d-9ex-improvements.md) para evitar copiar desnecessariamente o buffer da cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="b9714-109">In Windows 7, Direct3D 9EX first adopted [flip-model presentation](../direct3darticles/direct3d-9ex-improvements.md) to avoid unnecessarily copying the swap-chain buffer.</span></span> <span data-ttu-id="b9714-110">Usando o modelo de flip, buffers de fundo são invertidos entre o tempo de execução e o Gerenciador de Janelas da Área de Trabalho (DWM), portanto o DWM sempre compõe diretamente do buffer de fundo em vez de copiar o conteúdo do buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="b9714-110">By using flip model, back buffers are flipped between the runtime and Desktop Window Manager (DWM), so DWM always composes directly from the back buffer instead of copying the back buffer content.</span></span>

<span data-ttu-id="b9714-111">As APIs DXGI 1,2 incluem uma interface da cadeia de permuta DXGI revisada, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span><span class="sxs-lookup"><span data-stu-id="b9714-111">DXGI 1.2 APIs include a revised DXGI swap-chain interface, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="b9714-112">Você pode usar vários métodos de interface [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) para criar o objeto **IDXGISwapChain1** apropriado a ser usado com um identificador [**HWND**](../winprog/windows-data-types.md) , um objeto [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)ou a estrutura [**Windows. UI. XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="b9714-112">You can use multiple [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) interface methods to create the appropriate **IDXGISwapChain1** object to use with an [**HWND**](../winprog/windows-data-types.md) handle, a [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) object, [DirectComposition](../directcomp/directcomposition-portal.md), or the [**Windows.UI.Xaml**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) framework.</span></span>

<span data-ttu-id="b9714-113">Selecione o modelo de apresentação inverter especificando o valor de enumeração [**\_ \_ \_ \_ seqüencial de inverter efeito de permuta dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) no membro **SwapEffect** da estrutura [**DESC1 da cadeia de \_ permuta \_ \_ dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e definindo o membro **BufferCount** da **cadeia de permuta de dxgi \_ \_ \_ DESC1** para um mínimo de 2.</span><span class="sxs-lookup"><span data-stu-id="b9714-113">You select the flip presentation model by specifying the [**DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) enumeration value in the **SwapEffect** member of the [**DXGI\_SWAP\_CHAIN\_DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) structure and by setting the **BufferCount** member of **DXGI\_SWAP\_CHAIN\_DESC1** to a minimum of 2.</span></span> <span data-ttu-id="b9714-114">Para obter mais informações sobre como usar o modelo de flip DXGI, consulte [modelo de flip-dxgi](dxgi-flip-model.md).</span><span class="sxs-lookup"><span data-stu-id="b9714-114">For more info about how to use DXGI flip model, see [DXGI flip model](dxgi-flip-model.md).</span></span> <span data-ttu-id="b9714-115">Devido à apresentação mais suave do modelo de apresentação invertida e outras funcionalidades novas, recomendamos que você use o modelo de apresentação de flip para todos os novos aplicativos que você escreve com o Direct3D 10 e as APIs posteriores.</span><span class="sxs-lookup"><span data-stu-id="b9714-115">Because of the flip presentation model's smoother presentation and other new functionality, we recommend that you use flip presentation model for all new apps that you write with Direct3D 10 and later APIs.</span></span>

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a><span data-ttu-id="b9714-116">Usando retângulos sujos e o retângulo de rolagem na apresentação da cadeia de permuta</span><span class="sxs-lookup"><span data-stu-id="b9714-116">Using dirty rectangles and the scroll rectangle in swap chain presentation</span></span>

<span data-ttu-id="b9714-117">Usando retângulos sujos e o retângulo de rolagem na apresentação da cadeia de permuta, você economiza o uso da largura de banda da memória e o uso relacionado da energia do sistema, pois a quantidade de dados de pixel que o sistema operacional precisa para desenhar o próximo quadro apresentado será reduzida se o sistema operacional não precisar desenhar o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="b9714-117">By using dirty rectangles and the scroll rectangle in swap chain presentation, you save on the usage of memory bandwidth and the related usage of system power because the amount of pixel data that the operating system needs to draw the next presented frame is reduced if the operating system doesn't need to draw the entire frame.</span></span> <span data-ttu-id="b9714-118">Para aplicativos que são frequentemente exibidos por meio de Conexão de Área de Trabalho Remota e outras tecnologias de acesso remoto, as economias são particularmente perceptíveis na qualidade da tela, pois essas tecnologias usam retângulos sujos e rolam metadados.</span><span class="sxs-lookup"><span data-stu-id="b9714-118">For apps that are often displayed via Remote Desktop Connection and other remote-accessing technologies, the savings are particularly noticeable in the display quality because these technologies use dirty rectangles and scroll metadata.</span></span>

<span data-ttu-id="b9714-119">Você pode usar a rolagem somente com cadeias de permuta DXGI que são executadas no modelo de apresentação de flip.</span><span class="sxs-lookup"><span data-stu-id="b9714-119">You can use scroll only with DXGI swap chains that run in flip presentation model.</span></span> <span data-ttu-id="b9714-120">Você pode usar retângulos sujos com cadeias de permuta DXGI que são executados no modelo de flip e BitBlt (definido com [**\_ \_ \_ sequencial de efeito de permuta dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="b9714-120">You can use dirty rectangles with DXGI swap chains that run in both flip model and bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span>

<span data-ttu-id="b9714-121">Neste cenário e ilustração, mostramos a funcionalidade de usar retângulos sujos e rolar.</span><span class="sxs-lookup"><span data-stu-id="b9714-121">In this scenario and illustration we show the functionality of using dirty rectangles and scroll.</span></span> <span data-ttu-id="b9714-122">Aqui, um aplicativo rolável contém texto e animação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b9714-122">Here, a scrollable app contains text and animating video.</span></span> <span data-ttu-id="b9714-123">O aplicativo usa retângulos sujos para apenas atualizar o vídeo de animação e a nova linha para a janela, em vez de atualizar a janela inteira.</span><span class="sxs-lookup"><span data-stu-id="b9714-123">The app uses dirty rectangles to just update the animating video and new line for the window, instead of updating the entire window.</span></span> <span data-ttu-id="b9714-124">O retângulo de rolagem permite que o sistema operacional Copie e traduza o conteúdo renderizado anteriormente no novo quadro e processe apenas a nova linha no novo quadro.</span><span class="sxs-lookup"><span data-stu-id="b9714-124">The scroll rectangle allows the operating system to copy and translate the previously rendered content on the new frame and to render only the new line on the new frame.</span></span>

<span data-ttu-id="b9714-125">O aplicativo executa a apresentação chamando o método [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) .</span><span class="sxs-lookup"><span data-stu-id="b9714-125">The app performs presentation by calling the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method.</span></span> <span data-ttu-id="b9714-126">Nesta chamada, o aplicativo passa um ponteiro para uma estrutura [**de \_ \_ parâmetros presente de dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) que inclui retângulos sujos e o número de retângulos sujos, ou o retângulo de rolagem e o deslocamento de rolagem associado, ou ambos os retângulos sujos e o retângulo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="b9714-126">In this call, the app passes a pointer to a [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) structure that includes dirty rectangles and the number of dirty rectangles, or the scroll rectangle and the associated scroll offset, or both dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="b9714-127">Nosso aplicativo passa 2 retângulos sujos e o retângulo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="b9714-127">Our app passes 2 dirty rectangles and the scroll rectangle.</span></span> <span data-ttu-id="b9714-128">O retângulo de rolagem é a área do quadro anterior que o sistema operacional precisa copiar para o quadro atual antes de renderizar o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-128">The scroll rectangle is the area of the previous frame that the operating system needs to copy to the current frame before it renders the current frame.</span></span> <span data-ttu-id="b9714-129">O aplicativo especifica o vídeo animador e a nova linha como retângulos sujos, e o sistema operacional os renderiza no quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-129">The app specifies the animating video and new line as dirty rectangles, and the operating system renders them on the current frame.</span></span>

![ilustração de sobreposição de retângulos de rolagem e sujos](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

<span data-ttu-id="b9714-131">O retângulo tracejado mostra o retângulo de rolagem no quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-131">The dashed rectangle shows the scroll rectangle in the current frame.</span></span> <span data-ttu-id="b9714-132">O retângulo de rolagem é especificado pelo membro **pScrollRect** dos [**\_ \_ parâmetros presentes de dxgi**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span><span class="sxs-lookup"><span data-stu-id="b9714-132">The scroll rectangle is specified by the **pScrollRect** member of [**DXGI\_PRESENT\_PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters).</span></span> <span data-ttu-id="b9714-133">A seta mostra o deslocamento de rolagem.</span><span class="sxs-lookup"><span data-stu-id="b9714-133">The arrow shows the scroll offset.</span></span> <span data-ttu-id="b9714-134">O deslocamento de rolagem é especificado pelo membro **pScrollOffset** dos **\_ \_ parâmetros presentes de dxgi**.</span><span class="sxs-lookup"><span data-stu-id="b9714-134">The scroll offset is specified by the **pScrollOffset** member of **DXGI\_PRESENT\_PARAMETERS**.</span></span> <span data-ttu-id="b9714-135">Os retângulos preenchidos mostram os retângulos sujos que o aplicativo atualizou com o novo conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b9714-135">Filled rectangles show dirty rectangles that the app updated with new content.</span></span> <span data-ttu-id="b9714-136">Os retângulos preenchidos são especificados pelos membros **DirtyRectsCount** e **pDirtyRects** dos **\_ \_ parâmetros presentes de dxgi**.</span><span class="sxs-lookup"><span data-stu-id="b9714-136">The filled rectangles are specified by the **DirtyRectsCount** and **pDirtyRects** members of **DXGI\_PRESENT\_PARAMETERS**.</span></span>

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a><span data-ttu-id="b9714-137">Exemplo 2-cadeia de permuta de modelo invertida de buffer com retângulos sujos e retângulo de rolagem</span><span class="sxs-lookup"><span data-stu-id="b9714-137">Sample 2-buffer flip-model swap chain with dirty rectangles and scroll rectangle</span></span>

<span data-ttu-id="b9714-138">A próxima ilustração e sequência mostra um exemplo de uma operação de apresentação de flip-Model DXGI que usa retângulos sujos e um retângulo de rolagem.</span><span class="sxs-lookup"><span data-stu-id="b9714-138">The next illustration and sequence shows an example of a DXGI flip-model presentation operation that uses dirty rectangles and a scroll rectangle.</span></span> <span data-ttu-id="b9714-139">Neste exemplo, usamos o número mínimo de buffers para apresentação de flip-Model, que é uma contagem de buffer de dois, um buffer frontal que contém o conteúdo de exibição do aplicativo e um buffer de fundo que contém o quadro atual que o aplicativo deseja renderizar.</span><span class="sxs-lookup"><span data-stu-id="b9714-139">In this example we use the minimum number of buffers for flip-model presentation, which is a buffer count of two, one front buffer that contains the app display content and one back buffer that contains the current frame that the app wants to render.</span></span>

1.  <span data-ttu-id="b9714-140">Conforme mostrado no buffer frontal no início do quadro, o aplicativo rolável inicialmente mostra um quadro com um vídeo de texto e animação.</span><span class="sxs-lookup"><span data-stu-id="b9714-140">As shown in the front buffer at the beginning of the frame, the scrollable app initially shows a frame with some text and animating video.</span></span>
2.  <span data-ttu-id="b9714-141">Para renderizar o próximo quadro, o aplicativo é renderizado no buffer de fundo os retângulos sujos que atualizam o vídeo de animação e a nova linha para a janela.</span><span class="sxs-lookup"><span data-stu-id="b9714-141">To render the next frame, the app renders onto the back buffer the dirty rectangles that update the animating video and the new line for the window.</span></span>
3.  <span data-ttu-id="b9714-142">Quando o aplicativo chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), ele especifica os retângulos sujos e o retângulo de rolagem e o deslocamento.</span><span class="sxs-lookup"><span data-stu-id="b9714-142">When the app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), it specifies the dirty rectangles and the scroll rectangle and offset.</span></span> <span data-ttu-id="b9714-143">Em seguida, o tempo de execução copia o retângulo de rolagem do quadro anterior menos os retângulos sujos atualizados para o buffer de fundo atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-143">The runtime next copies the scroll rectangle from the previous frame minus the updated dirty rectangles onto the current back buffer.</span></span>
4.  <span data-ttu-id="b9714-144">O tempo de execução finalmente permuta os buffers frontal e traseiro.</span><span class="sxs-lookup"><span data-stu-id="b9714-144">The runtime finally swaps the front and back buffers.</span></span>

![exemplo de cadeia de permuta de flip-Model com retângulos de rolagem e sujos](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a><span data-ttu-id="b9714-146">Acompanhamento de retângulos com problemas e retângulos de rolagem em vários quadros</span><span class="sxs-lookup"><span data-stu-id="b9714-146">Tracking dirty rectangles and scroll rectangles across multiple frames</span></span>

<span data-ttu-id="b9714-147">Ao usar retângulos sujos em seu aplicativo, você deve acompanhar os retângulos sujos para dar suporte à renderização incremental.</span><span class="sxs-lookup"><span data-stu-id="b9714-147">When you use dirty rectangles in your app, you must track the dirty rectangles to support incremental rendering.</span></span> <span data-ttu-id="b9714-148">Quando seu aplicativo chama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) com retângulos sujos, você deve garantir que cada pixel dentro dos retângulos sujos esteja atualizado.</span><span class="sxs-lookup"><span data-stu-id="b9714-148">When your app calls [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) with dirty rectangles, you must ensure that every pixel within the dirty rectangles is up to date.</span></span> <span data-ttu-id="b9714-149">Se você não estiver reprocessando completamente toda a área do retângulo sujo ou se não puder saber para determinadas áreas sujos, deverá copiar alguns dados do buffer de fundo totalmente coerente anterior para o buffer de fundo atual e obsoleto antes de iniciar a renderização.</span><span class="sxs-lookup"><span data-stu-id="b9714-149">If you aren't completely re-rendering the whole area of the dirty rectangle or if you can’t know for certain the areas that are dirtied, you must copy some data from the previous fully coherent back buffer to the current, stale back buffer before you start rendering.</span></span>

<span data-ttu-id="b9714-150">O tempo de execução copia apenas as diferenças entre as áreas atualizadas do quadro anterior e as áreas atualizadas do quadro atual para o buffer de fundo atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-150">The runtime copies only the differences between updated areas of the previous frame and updated areas of the current frame onto the current back buffer.</span></span> <span data-ttu-id="b9714-151">Se essas áreas se interseccionarem, o tempo de execução copiará apenas a diferença entre elas.</span><span class="sxs-lookup"><span data-stu-id="b9714-151">If these areas intersect, the runtime copies only the difference between them.</span></span> <span data-ttu-id="b9714-152">Como você pode ver no diagrama e na sequência a seguir, você deve copiar a interseção entre o retângulo sujo do quadro 1 e o retângulo sujo do quadro 2 para o retângulo sujo do quadro 2.</span><span class="sxs-lookup"><span data-stu-id="b9714-152">As you can see in the following diagram and sequence, you must copy the intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>

1.  <span data-ttu-id="b9714-153">Há um retângulo sujo no quadro 1.</span><span class="sxs-lookup"><span data-stu-id="b9714-153">Present dirty rectangle in frame 1.</span></span>
2.  <span data-ttu-id="b9714-154">Copie a interseção entre o retângulo sujo do quadro 1 e o retângulo sujo do quadro 2 para o retângulo sujo do quadro 2.</span><span class="sxs-lookup"><span data-stu-id="b9714-154">Copy intersection between the dirty rectangle from frame 1 and the dirty rectangle from frame 2 into frame 2’s dirty rectangle.</span></span>
3.  <span data-ttu-id="b9714-155">Há um retângulo sujo no quadro 2.</span><span class="sxs-lookup"><span data-stu-id="b9714-155">Present dirty rectangle in frame 2.</span></span>

![acompanhamento de retângulos de rolagem e sujos em vários quadros](images/track-dirty-rects-scroll-rects.png)

<span data-ttu-id="b9714-157">Para generalizar, para uma cadeia de permuta com N buffers, a área em que o tempo de execução copia do último quadro para o quadro atual no presente do quadro atual é:</span><span class="sxs-lookup"><span data-stu-id="b9714-157">To generalize, for a swap chain with N buffers, the area that the runtime copies from the last frame to the current frame on the current frame’s present is:</span></span>

![equação para calcular a área em que o tempo de execução copia](images/runtime-copy-equation.png)

<span data-ttu-id="b9714-159">em que buffer indica o índice de buffer em uma cadeia de permuta, começando com o índice de buffer atual em zero.</span><span class="sxs-lookup"><span data-stu-id="b9714-159">where buffer indicates the buffer index in a swap chain, starting with current buffer index at zero.</span></span>

<span data-ttu-id="b9714-160">Você pode manter o controle de todas as interseções entre o quadro anterior e os retângulos sujos do quadro atual mantendo uma cópia dos retângulos sujos do quadro anterior ou renderizando novamente os retângulos sujos do novo quadro com o conteúdo apropriado do quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="b9714-160">You can keep track of any intersections between the previous frame and the current frame’s dirty rectangles by keeping a copy of the previous frame’s dirty rectangles or by re-rendering the new frame’s dirty rectangles with the appropriate content from the previous frame.</span></span>

<span data-ttu-id="b9714-161">Da mesma forma, nos casos em que a cadeia de permuta tem mais de 2 buffers de fundo, você deve garantir que as áreas sobrepostas entre os retângulos sujos do buffer atual e os retângulos sujos de todos os quadros anteriores sejam copiados ou reprocessados.</span><span class="sxs-lookup"><span data-stu-id="b9714-161">Similarly, in the cases where the swap chain has more than 2 back buffers, you must ensure that overlapping areas between the current buffer’s dirty rectangles and the dirty rectangles of all previous frame’s are copied or re-rendered.</span></span>

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a><span data-ttu-id="b9714-162">Acompanhamento de uma única interseção entre 2 retângulos sujos</span><span class="sxs-lookup"><span data-stu-id="b9714-162">Tracking a single intersection between 2 dirty rectangles</span></span>

<span data-ttu-id="b9714-163">No caso mais simples, quando você atualiza um único retângulo sujo por quadro, os retângulos sujos em dois quadros podem se Interseccionar.</span><span class="sxs-lookup"><span data-stu-id="b9714-163">In the simplest case, when you update a single dirty rectangle per frame, the dirty rectangles across two frames might intersect.</span></span> <span data-ttu-id="b9714-164">Para descobrir se o retângulo sujo do quadro anterior e o retângulo sujo do quadro atual se sobrepõem, você precisa verificar se o retângulo sujo do quadro anterior está interseccionado com o retângulo sujo do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-164">To find out whether the dirty rectangle of the previous frame and the dirty rectangle of the current frame overlap, you need to verify whether the dirty rectangle of the previous frame intersects with the dirty rectangle of the current frame.</span></span> <span data-ttu-id="b9714-165">Você pode chamar a função [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) do GDI para determinar se duas estruturas [**Rect**](/previous-versions//dd162897(v=vs.85)) que representam os dois retângulos sujos se cruzam.</span><span class="sxs-lookup"><span data-stu-id="b9714-165">You can call the GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) function to determine whether two [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that represent the two dirty rectangles intersect.</span></span>

<span data-ttu-id="b9714-166">Nesse trecho de código, uma chamada para [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) retorna a interseção de dois retângulos sujos em outro [**Rect**](/previous-versions//dd162897(v=vs.85)) chamado dirtyRectCopy.</span><span class="sxs-lookup"><span data-stu-id="b9714-166">In this code snippet, a call to [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) returns the intersection of two dirty rectangles in another [**RECT**](/previous-versions//dd162897(v=vs.85)) called dirtyRectCopy.</span></span> <span data-ttu-id="b9714-167">Depois que o trecho de código determina que os dois retângulos sujos se cruzam, ele chama o método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar a região da interseção no quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-167">After the code snippet determines that the two dirty rectangles intersect, it calls the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy the region of intersection into the current frame.</span></span>

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

<span data-ttu-id="b9714-168">Se você usar esse trecho de código em seu aplicativo, o aplicativo estará pronto para chamar [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) para atualizar o quadro atual com o retângulo sujo atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-168">If you use this code snippet in your application, the app will then be ready to call [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) to update the current frame with the current dirty rectangle.</span></span>

### <a name="tracking-intersections-between-n-dirty-rectangles"></a><span data-ttu-id="b9714-169">Acompanhamento de interseções entre N retângulos sujos</span><span class="sxs-lookup"><span data-stu-id="b9714-169">Tracking intersections between N dirty rectangles</span></span>

<span data-ttu-id="b9714-170">Se você especificar vários retângulos sujos, que podem incluir um retângulo sujo para a linha de rolagem recentemente revelada, por quadro, você precisará verificar e rastrear as sobreposições que podem ocorrer entre todos os retângulos sujos do quadro anterior e todos os retângulos sujos do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-170">If you specify multiple dirty rectangles, which can include a dirty rectangle for the newly revealed scroll line, per frame, you need to verify and track any overlaps that might occur between all the dirty rectangles of the previous frame and all the dirty rectangles of the current frame.</span></span> <span data-ttu-id="b9714-171">Para calcular as interseções entre os retângulos sujos do quadro anterior e os retângulos sujos do quadro atual, você pode agrupar os retângulos sujos em regiões.</span><span class="sxs-lookup"><span data-stu-id="b9714-171">To calculate the intersections between the dirty rectangles of the previous frame and the dirty rectangles of the current frame, you can group the dirty rectangles into regions.</span></span>

<span data-ttu-id="b9714-172">Neste trecho de código, chamamos a função [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) do GDI para converter cada retângulo sujo em uma região retangular e, em seguida, chamamos a função [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) do GDI para combinar todas as regiões retangulares sujas em um grupo.</span><span class="sxs-lookup"><span data-stu-id="b9714-172">In this code snippet, we call the GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) function to convert each dirty rectangle into a rectangular region and then we call the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to combine all the dirty rectangular regions into a group.</span></span>

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

<span data-ttu-id="b9714-173">Agora você pode usar a função [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) do GDI para determinar a interseção entre a região suja do quadro anterior e a região suja do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-173">You can now use the GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) function to determine the intersection between the dirty region of the previous frame and the dirty region of the current frame.</span></span> <span data-ttu-id="b9714-174">Depois de obter a região de interseção, chame a função [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) do GDI para obter cada retângulo individual da região de interseção e, em seguida, chame o método [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) para copiar cada retângulo de interseção no buffer de fundo atual.</span><span class="sxs-lookup"><span data-stu-id="b9714-174">After you obtain the intersecting region, call the GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) function to obtain each individual rectangle from the intersecting region and then call the [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) method to copy each intersecting rectangle into the current back buffer.</span></span> <span data-ttu-id="b9714-175">O próximo trecho de código mostra como usar essas funções GDI e Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9714-175">The next code snippet shows how to use these GDI and Direct3D functions.</span></span>

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a><span data-ttu-id="b9714-176">Cadeia de troca de modelo BitBlt com retângulos sujos</span><span class="sxs-lookup"><span data-stu-id="b9714-176">Bitblt model swap chain with dirty rectangles</span></span>

<span data-ttu-id="b9714-177">Você pode usar retângulos sujos com cadeias de permuta DXGI que são executados no modelo BitBlt (definido com [**\_ \_ \_ sequencial de efeito de permuta dxgi**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span><span class="sxs-lookup"><span data-stu-id="b9714-177">You can use dirty rectangles with DXGI swap chains that run in bitblt model (set with [**DXGI\_SWAP\_EFFECT\_SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).</span></span> <span data-ttu-id="b9714-178">As cadeias de troca de modelo BitBlt que usam mais de um buffer também devem controlar os retângulos sujos sobrepostos entre quadros da mesma maneira como descrito em [acompanhamento de retângulos sujos e retângulos de rolagem em vários quadros](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) para cadeias de troca de modelo de flip.</span><span class="sxs-lookup"><span data-stu-id="b9714-178">Bitblt model swap chains that use more than one buffer must also track overlapping dirty rectangles across frames in the same way as described in [Tracking dirty rectangles and scroll rectangles across multiple frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) for flip model swap chains.</span></span> <span data-ttu-id="b9714-179">Cadeias de troca de modelo BitBlt com apenas um buffer não precisam rastrear retângulos sujos sobrepostos porque todo o buffer é redesenhado a cada quadro.</span><span class="sxs-lookup"><span data-stu-id="b9714-179">Bitblt model swap chains with just one buffer need not track overlapping dirty rectangles because the entire buffer is redrawn every frame.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9714-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9714-180">Related topics</span></span>

[<span data-ttu-id="b9714-181">Aprimoramentos de DXGI 1,2</span><span class="sxs-lookup"><span data-stu-id="b9714-181">DXGI 1.2 Improvements</span></span>](dxgi-1-2-improvements.md)
