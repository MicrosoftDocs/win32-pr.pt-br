---
description: A compactação de bloco é uma técnica de compactação de textura para reduzir o tamanho da textura.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compactação de bloco (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561266"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="aa1d4-103">Compactação de bloco (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="aa1d4-104">A compactação de bloco é uma técnica de compactação de textura para reduzir o tamanho da textura.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="aa1d4-105">Quando comparado com uma textura com 32 bits por cor, uma textura compactada em bloco pode ser até 75% menor.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="aa1d4-106">Os apps geralmente ganham um aumento no desempenho ao usar a compactação de bloco devido o menor volume de memória.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="aa1d4-107">Mesmo com perdas, a compactação de bloco funciona bem e é recomendada para todas as texturas que são transformadas e filtradas pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="aa1d4-108">Texturas que são mapeadas diretamente na tela (elementos de interface do usuário como ícones e texto) não são uma ótima opção para compactação porque os artefatos são mais perceptíveis.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="aa1d4-109">Uma textura compactada em bloco deve ser criada como um múltiplo do tamanho de 4 em todas as dimensões e não pode ser usada como uma saída do pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="aa1d4-110">Como o bloqueio de compactação funciona?</span><span class="sxs-lookup"><span data-stu-id="aa1d4-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="aa1d4-111">Armazenando dados descompactados</span><span class="sxs-lookup"><span data-stu-id="aa1d4-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="aa1d4-112">Armazenando dados compactados</span><span class="sxs-lookup"><span data-stu-id="aa1d4-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="aa1d4-113">Usando compactação de bloco</span><span class="sxs-lookup"><span data-stu-id="aa1d4-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="aa1d4-114">Tamanho virtual versus tamanho físico</span><span class="sxs-lookup"><span data-stu-id="aa1d4-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="aa1d4-115">Algoritmos de compactação</span><span class="sxs-lookup"><span data-stu-id="aa1d4-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="aa1d4-116">BC1</span><span class="sxs-lookup"><span data-stu-id="aa1d4-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="aa1d4-117">BC2</span><span class="sxs-lookup"><span data-stu-id="aa1d4-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="aa1d4-118">BC3</span><span class="sxs-lookup"><span data-stu-id="aa1d4-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="aa1d4-119">BC4</span><span class="sxs-lookup"><span data-stu-id="aa1d4-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="aa1d4-120">BC5</span><span class="sxs-lookup"><span data-stu-id="aa1d4-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="aa1d4-121">Conversão de formato usando o Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="aa1d4-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="aa1d4-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa1d4-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="aa1d4-123">Como o bloqueio de compactação funciona?</span><span class="sxs-lookup"><span data-stu-id="aa1d4-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="aa1d4-124">A compactação de bloco é uma técnica para reduzir a quantidade de memória necessária para armazenar dados de cor.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="aa1d4-125">Armazenando algumas cores no tamanho original e outras cores usando um esquema de codificação, você pode reduzir significativamente a quantidade de memória necessária para armazenar a imagem.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="aa1d4-126">Como o hardware decodifica automaticamente os dados compactados, não há nenhuma penalidade de desempenho para o uso de texturas compactadas.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="aa1d4-127">Para ver como funciona a compactação, examine os dois exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="aa1d4-128">O primeiro exemplo descreve a quantidade de memória usada para armazenar dados não compactados; o segundo exemplo descreve a quantidade de memória usada para armazenar dados compactados.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="aa1d4-129">Armazenando dados descompactados</span><span class="sxs-lookup"><span data-stu-id="aa1d4-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="aa1d4-130">A ilustração a seguir representa uma textura de 4 × 4 não compactada.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="aa1d4-131">Suponha que cada cor contenha um componente único de cor (vermelho, por exemplo) e é armazenado em um byte de memória.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![ilustração de uma textura 4x4 não compactada](images/d3d10-block-compress-1.png)

<span data-ttu-id="aa1d4-133">Os dados não compactados são dispostos na memória sequencialmente e exigem 16 bytes, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![ilustração de dados descompactados na memória sequencial](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="aa1d4-135">Armazenando dados compactados</span><span class="sxs-lookup"><span data-stu-id="aa1d4-135">Storing Compressed Data</span></span>

<span data-ttu-id="aa1d4-136">Agora que você já viu quanta memória uma imagem descompactada utiliza, dê uma olhada na quantidade de memória poupada por uma imagem compactada.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="aa1d4-137">O formato de compactação [BC1](#bc1) armazena 2 cores (1 byte cada) e 16 índices de 3 bits (48 bits, ou 6 bytes) que são usados para interpolar as cores originais na textura, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![ilustração do formato de compactação BC1](images/d3d10-block-compress-3.png)

<span data-ttu-id="aa1d4-139">O espaço total obrigatório para armazenar os dados compactados é de 8 bytes, que é uma economia de memória de 50% em relação ao exemplo não compactado.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="aa1d4-140">A economia é ainda maior quando mais de um componente de cor é usado.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="aa1d4-141">A economia de memória substancial proporcionada pelo compactação de bloco pode causar um aumento no desempenho.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="aa1d4-142">Esse desempenho impacta a qualidade da imagem (devido à interpolação de cores); no entanto, a baixa qualidade geralmente não é perceptível.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="aa1d4-143">A próxima seção mostra como o Direct3D 10 torna mais fácil usar a compactação de bloco em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="aa1d4-144">Usando compactação de bloco</span><span class="sxs-lookup"><span data-stu-id="aa1d4-144">Using Block Compression</span></span>

<span data-ttu-id="aa1d4-145">Crie uma textura compactada por bloco, assim como uma textura não compactada (consulte [criar uma textura de um arquivo](d3d10-graphics-programming-guide-resources-creating-textures.md)), exceto que você especificar um formato compactado por bloco.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="aa1d4-146">Em seguida, crie uma exibição para associar a textura ao pipeline.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="aa1d4-147">Como uma textura compactada por bloco pode ser usada somente como uma entrada para um estágio de sombreador, você deseja criar uma exibição de recurso de sombreador chamando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="aa1d4-148">Use uma textura compactada em bloco da mesma maneira que você usaria uma textura não compactada.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="aa1d4-149">Se seu aplicativo receberá um ponteiro de memória para dados compactados em bloco, você precisa levar em conta a memória preenchimento em uma minimapa que faz com que o tamanho declarado ser diferente do tamanho real.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="aa1d4-150">Tamanho virtual versus tamanho físico</span><span class="sxs-lookup"><span data-stu-id="aa1d4-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="aa1d4-151">Se você tiver o código do app que usa um ponteiro de memória para percorrer a memória de um bloco de textura compactado, há uma consideração importante que pode exigir uma modificação no código do seu app.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="aa1d4-152">Uma textura compactada em bloco deve ser um múltiplo de 4 em todas as dimensões porque os algoritmos de compactação de bloco operam em blocos de texel de 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="aa1d4-153">Isso será um problema para um mipmap cujas dimensões iniciais são divisíveis por 4, mas os níveis subdivididos não são.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="aa1d4-154">O diagrama a seguir mostra a diferença na área entre o tamanho virtual (declarado) e o tamanho físico (real) de cada nível de mipmap.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![diagrama de níveis de mipmap não compactados e compactados](images/d3d10-block-compress-pad.png)

<span data-ttu-id="aa1d4-156">O lado esquerdo do diagrama mostra os tamanhos de nível de mipmap que são gerados para uma textura de 60 × 40 não compactada.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="aa1d4-157">O tamanho de nível superior é retirado da chamada de API que gera a textura; cada nível subsequente é metade do tamanho do nível anterior.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="aa1d4-158">Para uma textura descompactada, não há nenhuma diferença entre o tamanho virtual (declarado) e o tamanho físico (real).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="aa1d4-159">O lado direito do diagrama mostra os tamanhos de nível de mipmap que são gerados para a mesma textura de 60 × 40 com compactação.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="aa1d4-160">Observe que o segundo e o terceiro nível possuem preenchimento de memória para gerar os fatores de tamanho 4 em cada nível.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="aa1d4-161">Isso é necessário para que os algoritmos possam operar em blocos de 4 × 4 texel.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="aa1d4-162">Isso é evidente se você considerar os níveis de mipmap menores que 4 × 4; o tamanho desses níveis muito pequenos de mipmap será arredondado para cima para o fator mais próximo de 4 quando a memória de textura for alocada.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="aa1d4-163">O hardware de amostragem usa o tamanho virtual; quando é feito uma amostragem da textura, o preenchimento de memória é ignorado.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="aa1d4-164">Para níveis de mipmap menores que 4 × 4, somente os quatro primeiros texels são usados para um mapa 2 x 2, e apenas o primeiro texel é usado por um bloco 1 × 1.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="aa1d4-165">No entanto, não há nenhuma estrutura de API que expõe o tamanho físico (incluindo o preenchimento de memória).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="aa1d4-166">Resumindo, tome cuidado ao usar blocos de memória alinhados ao copiar regiões que contêm dados compactados em bloco.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="aa1d4-167">Para fazer isso em um app que obtém um ponteiro de memória, certifique-se de que o ponteiro usa a densidade de superfície para levar em conta o tamanho da memória física.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="aa1d4-168">Algoritmos de compactação</span><span class="sxs-lookup"><span data-stu-id="aa1d4-168">Compression Algorithms</span></span>

<span data-ttu-id="aa1d4-169">As técnicas de compactação de bloco no Direct3D dividem os dados de textura descompactados em blocos de 4 × 4, compactam cada bloco e armazenam os dados.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="aa1d4-170">Por esse motivo, as texturas a serem compactadas devem ter dimensões de textura que são múltiplas de 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![diagrama de compactação de bloco](images/d3d10-compression-1.png)

<span data-ttu-id="aa1d4-172">O diagrama acima mostra uma textura particionada em blocos de texel.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="aa1d4-173">O primeiro bloco mostra o layout de 16 texels rotulado como a-p, mas todos os blocos tem a mesma organização dos dados.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="aa1d4-174">O Direct3D implementa vários esquemas de compactação, cada um implementa um equilíbrio diferente entre os vários componentes armazenados, o número de bits por componente e a quantidade de memória consumida.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="aa1d4-175">Use esta tabela para ajudar a escolher o formato que funciona melhor com o tipo de dados e a resolução de dados que melhor se adapta ao seu app.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="aa1d4-176">Dados de origem</span><span class="sxs-lookup"><span data-stu-id="aa1d4-176">Source Data</span></span>                     | <span data-ttu-id="aa1d4-177">Resolução de compactação de dados (em bits)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="aa1d4-178">Escolha esse formato de compactação</span><span class="sxs-lookup"><span data-stu-id="aa1d4-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="aa1d4-179">Alfa e cor de três componentes</span><span class="sxs-lookup"><span data-stu-id="aa1d4-179">Three-component color and alpha</span></span> | <span data-ttu-id="aa1d4-180">Cor (5:6:5), alfa (1) ou nenhum alfa</span><span class="sxs-lookup"><span data-stu-id="aa1d4-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="aa1d4-181">BC1</span><span class="sxs-lookup"><span data-stu-id="aa1d4-181">BC1</span></span>                            |
| <span data-ttu-id="aa1d4-182">Alfa e cor de três componentes</span><span class="sxs-lookup"><span data-stu-id="aa1d4-182">Three-component color and alpha</span></span> | <span data-ttu-id="aa1d4-183">Cor (5:6:5), alfa (4)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="aa1d4-184">BC2</span><span class="sxs-lookup"><span data-stu-id="aa1d4-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="aa1d4-185">Alfa e cor de três componentes</span><span class="sxs-lookup"><span data-stu-id="aa1d4-185">Three-component color and alpha</span></span> | <span data-ttu-id="aa1d4-186">Cor (5:6:5), alfa (8)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="aa1d4-187">BC3</span><span class="sxs-lookup"><span data-stu-id="aa1d4-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="aa1d4-188">Cor de um componente</span><span class="sxs-lookup"><span data-stu-id="aa1d4-188">One-component color</span></span>             | <span data-ttu-id="aa1d4-189">Um componente (8)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-189">One component (8)</span></span>                     | [<span data-ttu-id="aa1d4-190">BC4</span><span class="sxs-lookup"><span data-stu-id="aa1d4-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="aa1d4-191">Cor de dois componentes</span><span class="sxs-lookup"><span data-stu-id="aa1d4-191">Two-component color</span></span>             | <span data-ttu-id="aa1d4-192">Dois componentes (8:8)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="aa1d4-193">BC5</span><span class="sxs-lookup"><span data-stu-id="aa1d4-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="aa1d4-194">BC1</span><span class="sxs-lookup"><span data-stu-id="aa1d4-194">BC1</span></span>

<span data-ttu-id="aa1d4-195">Use o primeiro formato de compactação de bloco (BC1) (o \_ formato dxgi \_ BC1 não \_ tipado, \_ formato DXGI \_ BC1 \_ UNORM ou dxgi \_ BC1 \_ UNORM \_ sRGB) para armazenar dados de três componentes coloridos usando uma cor 5:6:5 (5 bits vermelho, 6 bits verde, 5 bits azul).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="aa1d4-196">Isso vale até mesmo quando os dados também contêm alfa de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="aa1d4-197">Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, o formato BC1 reduz a memória necessária de 48 bytes (16 cores × 3 componentes/cor × 1 byte/componente) para 8 bytes de memória.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="aa1d4-198">O algoritmo funciona em blocos de texels de 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="aa1d4-199">Em vez de armazenar 16 cores, o algoritmo salva 2 cores de referência (cor \_ 0 e cor \_ 1) e índices de cores de 16 2 bits (bloqueia a – p), conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![diagrama do layout da compactação BC1](images/d3d10-compression-bc1.png)

<span data-ttu-id="aa1d4-201">Os índices de cor (a–p) são usados para procurar as cores originais em uma tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="aa1d4-202">A tabela de cores contém 4 cores.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-202">The color table contains 4 colors.</span></span> <span data-ttu-id="aa1d4-203">As duas primeiras cores — cor \_ 0 e cor \_ 1 — são as cores mínimas e máximas.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="aa1d4-204">As outras duas cores, cor \_ 2 e cor \_ 3, são cores intermediárias calculadas com interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="aa1d4-205">As quatro cores recebem valores de índice de 2 bits que serão salvos em blocos a–p.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="aa1d4-206">Por fim, todas as cores nos blocos a–p são comparadas com as quatro cores na tabela de cores e o índice para a cor mais próxima é armazenado nos blocos de 2 bits.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="aa1d4-207">Esse algoritmo se compromete a dados que também contêm alfa de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="aa1d4-208">A única diferença é que a cor \_ 3 é definida como 0 (que representa uma cor transparente) e \_ a cor 2 é uma mistura linear de cor \_ 0 e cor \_ 1.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa1d4-209">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="aa1d4-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="aa1d4-210">Esse formato existe tanto no Direct3D 9 quanto no 10.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="aa1d4-211">No Direct3D 9, o formato BC1 é chamado de D3DFMT_DXT1.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="aa1d4-212">No Direct3D 10, o formato BC1 é representado por DXGI_FORMAT_BC1_UNORM ou DXGI_FORMAT_BC1_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="aa1d4-213">BC2</span><span class="sxs-lookup"><span data-stu-id="aa1d4-213">BC2</span></span>

<span data-ttu-id="aa1d4-214">Use o formato BC2 (um \_ formato dxgi \_ BC2 sem \_ tipo, \_ formato DXGI \_ BC2 \_ UNORM ou dxgi \_ BC2 \_ UNORM \_ sRGB) para armazenar dados que contêm dados de cor e alfa com coerência baixa (use [BC3](#bc3) para dados alfa altamente coerentes).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="aa1d4-215">O formato BC2 armazena dados RGB como uma cor 5:6:5 (5 bits de vermelho, 6 bits de verde, 5 bits de azul) e alfa como um valor de 4 bits separado.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="aa1d4-216">Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 64 bytes (16 cores × 4 componentes/cor × 1 byte/componente) para 16 bytes de memória.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="aa1d4-217">O formato BC2 armazena cores com o mesmo número de bits e dados de layout como o formato [BC1](#bc1), no entanto, o BC2 requer 64-bits adicionais de memória para armazenar os dados alfa, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![diagrama do layout da compactação BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa1d4-219">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="aa1d4-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="aa1d4-220">Esse formato existe tanto no Direct3D 9 quanto no 10.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="aa1d4-221">No Direct3D 9, o formato BC2 é chamado de D3DFMT_DXT2 e D3DFMT_DXT3.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="aa1d4-222">No Direct3D 10, o formato BC2 é representado por DXGI_FORMAT_BC2_UNORM ou DXGI_FORMAT_BC2_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="aa1d4-223">BC3</span><span class="sxs-lookup"><span data-stu-id="aa1d4-223">BC3</span></span>

<span data-ttu-id="aa1d4-224">Use o formato BC3 (um \_ formato dxgi \_ BC3 sem \_ tipo, \_ formato DXGI \_ BC3 \_ UNORM ou dxgi \_ BC3 \_ UNORM \_ sRGB) para armazenar dados de cores altamente coerentes (use [BC2](#bc2) com dados alfa menos coerentes).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="aa1d4-225">O formato BC3 armazena dados de cor usando cor 5:6:5 (5 bits de vermelho, 6 bits de verde, 5 bits de azul) e dados alfa usando um byte.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="aa1d4-226">Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 64 bytes (16 cores × 4 componentes/cor × 1 byte/componente) para 16 bytes de memória.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="aa1d4-227">O formato BC3 armazena cores com o mesmo número de bits e layout de dados que o formato [BC1](#bc1), no entanto, o BC3 requer 64 bits adicionais de memória para armazenar os dados alfa.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="aa1d4-228">O formato BC3 manipula o alfa armazenando dois valores de referência e interpolando entre eles (da mesma forma como o BC1 armazena cor RGB).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="aa1d4-229">O algoritmo funciona em blocos de texels de 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="aa1d4-230">Em vez de armazenar 16 valores Alfa, o algoritmo armazena 2 Alfas de referência (alfa \_ 0 e alfa \_ 1) e índices de cores de 16 3 bits (alfa a até p), conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![diagrama do layout da compactação BC3](images/d3d10-compression-bc3.png)

<span data-ttu-id="aa1d4-232">O formato BC3 usa os índices de alfa (a–p) para procurar as cores originais em uma tabela de pesquisa que contém 8 valores.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="aa1d4-233">Os dois primeiros valores — Alfa \_ 0 e alfa \_ 1 — são os valores mínimo e máximo; os outros seis valores intermediários são calculados usando interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="aa1d4-234">O algoritmo determina o número de valores alfa interpolados examinando os dois valores alfa de referência.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="aa1d4-235">Se alfa \_ 0 for maior que alfa \_ 1, BC3 interpolará 6 valores Alfa; caso contrário, ele interpolará 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="aa1d4-236">Quando o BC3 interpola apenas 4 valores alfa, ele define dois valores alfa adicionais (0 para totalmente transparente e 255 para totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="aa1d4-237">O BC3 compacta os valores alfabéticos na área de texel de 4 × 4, armazenando o código de bit correspondente aos valores alfa interpolados que melhor correspondem ao alfa original para um determinado texel.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa1d4-238">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="aa1d4-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="aa1d4-239">No Direct3D 9, o formato BC3 é chamado de D3DFMT_DXT4 e D3DFMT_DXT5.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="aa1d4-240">No Direct3D 10, o formato BC3 é representado por DXGI_FORMAT_BC3_UNORM ou DXGI_FORMAT_BC3_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="aa1d4-241">BC4</span><span class="sxs-lookup"><span data-stu-id="aa1d4-241">BC4</span></span>

<span data-ttu-id="aa1d4-242">Use o formato BC4 para armazenar dados de cor de um componente usando 8 bits para cada cor.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="aa1d4-243">Como resultado da maior precisão (em comparação com [BC1](#bc1)), o BC4 é ideal para armazenar dados de ponto flutuante no intervalo de \[ 0 a 1 \] usando o formato dxgi \_ \_ BC4 \_ UNORM e \[ -1 a + 1 \] usando o formato dxgi \_ BC4 SNORM \_ \_ Format.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="aa1d4-244">Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 16 bytes (16 cores × 1 componentes/cor × 1 byte/componente) para 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="aa1d4-245">O algoritmo funciona em blocos de texels de 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="aa1d4-246">Em vez de armazenar 16 cores, o algoritmo armazena 2 cores de referência (vermelho \_ 0 e vermelho \_ 1) e índices de cores de 16 3 bits (vermelho a por meio do Red p), conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![diagrama do layout da compactação BC4](images/d3d10-compression-bc4.png)

<span data-ttu-id="aa1d4-248">O algoritmo usa os índices de 3 bits para procurar as cores em uma tabela de cores que contém 8 cores.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="aa1d4-249">As duas primeiras cores — vermelho \_ 0 e vermelho \_ 1 — são as cores mínimas e máximas.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="aa1d4-250">O algoritmo calcula as cores restantes usando interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="aa1d4-251">O algoritmo determina o número de valores de cor interpolados examinando os dois valores de referência.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="aa1d4-252">Se o vermelho \_ 0 for maior que o vermelho \_ 1, BC4 interpolará 6 valores de cor; caso contrário, ele interpolará 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="aa1d4-253">Quando o BC4 interpola apenas 4 valores de cor, ele define dois valores de cor adicional (0.0f para totalmente transparente e 1.0f para totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="aa1d4-254">O BC4 compacta os valores alfabéticos na área de texel de 4 × 4, armazenando o código de bit correspondente aos valores alfa interpolados que melhor correspondem ao alfa original para um determinado texel.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="aa1d4-255">BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="aa1d4-256">BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="aa1d4-257">BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-257">BC4\_UNORM</span></span>

<span data-ttu-id="aa1d4-258">A interpolação dos dados de componente único é feita como no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="aa1d4-259">As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="aa1d4-260">BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-260">BC4\_SNORM</span></span>

<span data-ttu-id="aa1d4-261">O \_ formato dxgi \_ BC4 \_ SNORM é exatamente o mesmo, exceto que os dados são codificados no intervalo de SNORM e quando quatro valores de cor são interpolados.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="aa1d4-262">A interpolação dos dados de componente único é feita como no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="aa1d4-263">As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="aa1d4-264">BC5</span><span class="sxs-lookup"><span data-stu-id="aa1d4-264">BC5</span></span>

<span data-ttu-id="aa1d4-265">Use o formato BC5 para armazenar dados de cor de dois componentes usando 8 bits para cada cor.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="aa1d4-266">Como resultado da maior precisão (em comparação com [BC1](#bc1)), o BC5 é ideal para armazenar dados de ponto flutuante no intervalo de \[ 0 a 1 \] usando o formato dxgi \_ \_ BC5 \_ UNORM e \[ -1 a + 1 \] usando o formato dxgi \_ BC5 SNORM \_ \_ Format.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="aa1d4-267">Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 32 bytes (16 cores × 2 componentes/cor × 1 byte/componente) para 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="aa1d4-268">O algoritmo funciona em blocos de texels de 4 × 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="aa1d4-269">Em vez de armazenar 16 cores para ambos os componentes, o algoritmo armazena 2 cores de referência para cada componente (vermelho \_ 0, vermelho \_ 1, verde \_ 0 e verde \_ 1) e índices de cores de 16 3 bits para cada componente (vermelho a por meio de p vermelho e verde a até verde p), conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![diagrama do layout da compactação Bc5](images/d3d10-compression-bc5.png)

<span data-ttu-id="aa1d4-271">O algoritmo usa os índices de 3 bits para procurar as cores em uma tabela de cores que contém 8 cores.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="aa1d4-272">As duas primeiras cores — vermelho \_ 0 e vermelho \_ 1 (ou verde \_ 0 e verde \_ 1) — são as cores mínimas e máximas.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="aa1d4-273">O algoritmo calcula as cores restantes usando interpolação linear.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="aa1d4-274">O algoritmo determina o número de valores de cor interpolados examinando os dois valores de referência.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="aa1d4-275">Se o vermelho \_ 0 for maior que o vermelho \_ 1, BC5 interpolará 6 valores de cor; caso contrário, ele interpolará 4.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="aa1d4-276">Quando o BC5 interpola apenas 4 valores de cor, ele define os dois valores de cor restantes em 0.0f e 1.0f.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="aa1d4-277">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="aa1d4-278">BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="aa1d4-279">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-279">BC5\_UNORM</span></span>

<span data-ttu-id="aa1d4-280">A interpolação dos dados de componente único é feita como no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="aa1d4-281">Os cálculos para os componentes verdes são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="aa1d4-282">As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="aa1d4-283">BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-283">BC5\_SNORM</span></span>

<span data-ttu-id="aa1d4-284">O \_ formato dxgi \_ BC5 \_ SNORM é exatamente o mesmo, exceto que os dados são codificados no intervalo de SNORM e quando 4 valores de dados são interpolados, os dois valores adicionais são-1,0 f e 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="aa1d4-285">A interpolação dos dados de componente único é feita como no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="aa1d4-286">Os cálculos para os componentes verdes são semelhantes.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="aa1d4-287">As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="aa1d4-288">Conversão de formato usando o Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="aa1d4-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="aa1d4-289">O Direct3D 10,1 permite cópias entre texturas de tipo preestruturadas e texturas compactadas de bloco das mesmas larguras de bits.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="aa1d4-290">As funções que podem fazer isso são [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span><span class="sxs-lookup"><span data-stu-id="aa1d4-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="aa1d4-291">A partir do Direct3D 10,1, você pode usar [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar entre alguns tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="aa1d4-292">Esse tipo de operação de cópia executa um tipo de conversão de formato que reinterpreta os dados de recursos como um tipo de formato diferente.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="aa1d4-293">Considere este exemplo que mostra a diferença entre a reinterpretação de dados com o comportamento de um tipo mais comum de conversão:</span><span class="sxs-lookup"><span data-stu-id="aa1d4-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="aa1d4-294">Para reinterpretar ' f ' como o tipo de ' u ', use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span><span class="sxs-lookup"><span data-stu-id="aa1d4-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="aa1d4-295">Na reinterpretação anterior, o valor subjacente dos dados não muda; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta o flutuante como um inteiro sem sinal.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="aa1d4-296">Para executar o tipo mais comum de conversão, use a atribuição:</span><span class="sxs-lookup"><span data-stu-id="aa1d4-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="aa1d4-297">Na conversão anterior, o valor subjacente dos dados muda.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="aa1d4-298">A tabela a seguir lista os formatos de destino e origem permitidos que você pode usar nesse tipo de reinterpretação de conversão de formatos.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="aa1d4-299">Você deve codificar os valores corretamente para que a reinterpretação funcione conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="aa1d4-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="aa1d4-300">Largura de bit</span><span class="sxs-lookup"><span data-stu-id="aa1d4-300">Bit Width</span></span> | <span data-ttu-id="aa1d4-301">Recurso não compactado</span><span class="sxs-lookup"><span data-stu-id="aa1d4-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="aa1d4-302">Recurso compactado em bloco</span><span class="sxs-lookup"><span data-stu-id="aa1d4-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1d4-303">32</span><span class="sxs-lookup"><span data-stu-id="aa1d4-303">32</span></span>        | <span data-ttu-id="aa1d4-304">\_Formato dxgi \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="aa1d4-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="aa1d4-305">\_Formato dxgi \_ R32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="aa1d4-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="aa1d4-306">\_Formato dxgi \_ R9G9B9E5 \_ SHAREDEXP</span><span class="sxs-lookup"><span data-stu-id="aa1d4-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="aa1d4-307">64</span><span class="sxs-lookup"><span data-stu-id="aa1d4-307">64</span></span>        | <span data-ttu-id="aa1d4-308">\_Formato dxgi \_ R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="aa1d4-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="aa1d4-309">\_Formato dxgi \_ R16G16B16A16 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="aa1d4-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="aa1d4-310">\_Formato dxgi \_ R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="aa1d4-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="aa1d4-311">\_Formato dxgi \_ R32G32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="aa1d4-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="aa1d4-312">\_Formato dxgi \_ BC1 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="aa1d4-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="aa1d4-313">\_Formato dxgi \_ BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="aa1d4-314">\_Formato dxgi \_ BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="aa1d4-315">128</span><span class="sxs-lookup"><span data-stu-id="aa1d4-315">128</span></span>       | <span data-ttu-id="aa1d4-316">\_Formato dxgi \_ R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="aa1d4-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="aa1d4-317">\_Formato dxgi \_ R32G32B32A32 \_ Santo</span><span class="sxs-lookup"><span data-stu-id="aa1d4-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="aa1d4-318">\_Formato dxgi \_ BC2 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="aa1d4-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="aa1d4-319">\_Formato dxgi \_ BC3 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="aa1d4-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="aa1d4-320">\_Formato dxgi \_ BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="aa1d4-321">\_Formato dxgi \_ BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="aa1d4-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="aa1d4-322">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa1d4-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa1d4-323">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aa1d4-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
