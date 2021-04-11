---
description: Ao renderizar a saída 2D usando vértices pré-aprovados, deve-se ter cuidado para garantir que cada área de Texel corresponda corretamente a uma área de pixel única, caso contrário, pode ocorrer distorção de textura.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mapeamento direto de texels para pixels (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163805"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="34fdf-103">Mapeamento direto de texels para pixels (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="34fdf-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="34fdf-104">Ao renderizar a saída 2D usando vértices pré-aprovados, deve-se ter cuidado para garantir que cada área de Texel corresponda corretamente a uma área de pixel única, caso contrário, pode ocorrer distorção de textura.</span><span class="sxs-lookup"><span data-stu-id="34fdf-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="34fdf-105">Ao compreender os conceitos básicos do processo que o Direct3D segue ao rasterizar e texturing triângulos, você pode garantir que seu aplicativo Direct3D processe corretamente a saída 2D.</span><span class="sxs-lookup"><span data-stu-id="34fdf-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![ilustração de uma exibição de resolução 6x6](images/maptex-fig1.png)

<span data-ttu-id="34fdf-107">O diagrama anterior mostra pixels modelados como quadrados.</span><span class="sxs-lookup"><span data-stu-id="34fdf-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="34fdf-108">Na realidade, no entanto, os pixels são pontos, e não quadrados.</span><span class="sxs-lookup"><span data-stu-id="34fdf-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="34fdf-109">Cada quadrado no diagrama anterior indica a área acesa pelo pixel, mas um pixel é sempre apenas um ponto no centro de um quadrado.</span><span class="sxs-lookup"><span data-stu-id="34fdf-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="34fdf-110">Essa distinção, embora aparentemente pequena, é importante.</span><span class="sxs-lookup"><span data-stu-id="34fdf-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="34fdf-111">Uma ilustração melhor da mesma exibição é mostrada no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="34fdf-111">A better illustration of the same display is shown in the following diagram.</span></span>

![ilustração de uma exibição que consiste em pixels](images/maptex-fig2.png)

<span data-ttu-id="34fdf-113">O diagrama anterior mostra corretamente cada pixel físico como um ponto no centro de cada célula.</span><span class="sxs-lookup"><span data-stu-id="34fdf-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="34fdf-114">A coordenada de espaço da tela (0, 0) está localizada diretamente no pixel superior esquerdo e, portanto, no centro da célula superior esquerda.</span><span class="sxs-lookup"><span data-stu-id="34fdf-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="34fdf-115">O canto superior esquerdo da exibição, portanto, em (-0,5,-0,5) porque é de 0,5 células à esquerda e 0,5 células para cima do pixel superior esquerdo.</span><span class="sxs-lookup"><span data-stu-id="34fdf-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="34fdf-116">O Direct3D processará um quad com os cantos em (0, 0) e (4, 4), conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="34fdf-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![ilustração de um contorno de um quádruplo não rasterizado entre (0, 0) e (4, 4)](images/maptex-fig3.png)

<span data-ttu-id="34fdf-118">A ilustração anterior mostra onde o quádruplo matemático está em relação à exibição, mas não mostra qual será a aparência do Quad quando o Direct3D o rasteriza e o envia para a exibição.</span><span class="sxs-lookup"><span data-stu-id="34fdf-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="34fdf-119">Na verdade, é impossível que uma tela de varredura preencha o quad exatamente conforme mostrado, pois as bordas do Quad não coincidem com os limites entre células de pixel.</span><span class="sxs-lookup"><span data-stu-id="34fdf-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="34fdf-120">Em outras palavras, como cada pixel só pode exibir uma única cor, cada célula de pixel é preenchida com apenas uma única cor; se a exibição fosse renderizar o quad exatamente como mostrado, as células de pixel ao longo da borda do Quad precisarão mostrar duas cores distintas: azul, quando coberto pelo Quad e branco, onde apenas o plano de fundo está visível.</span><span class="sxs-lookup"><span data-stu-id="34fdf-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="34fdf-121">Em vez disso, o hardware de gráficos é tarefa com a determinação de quais pixels devem ser preenchidos para aproximar o quad.</span><span class="sxs-lookup"><span data-stu-id="34fdf-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="34fdf-122">Esse processo é chamado de rasterização e é detalhado em [regras de rasterização (Direct3D 9)](rasterization-rules.md).</span><span class="sxs-lookup"><span data-stu-id="34fdf-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="34fdf-123">Para esse caso em particular, o quad rasterizado é mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="34fdf-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![ilustração de um quad desenhado não texturizado de (0, 0) a (4, 4)](images/maptex-fig4.png)

<span data-ttu-id="34fdf-125">Observe que o quad passado para o Direct3D tem cantos em (0, 0) e (4, 4), mas a saída rasterizada (a ilustração anterior) tem cantos em (-0,5,-0,5) e (3,5, 3,5).</span><span class="sxs-lookup"><span data-stu-id="34fdf-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="34fdf-126">Compare as duas ilustrações anteriores para a renderização de diferenças.</span><span class="sxs-lookup"><span data-stu-id="34fdf-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="34fdf-127">Você pode ver que a exibição realmente renderiza o tamanho correto, mas foi deslocada por-0,5 células nas direções x e y.</span><span class="sxs-lookup"><span data-stu-id="34fdf-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="34fdf-128">No entanto, com exceção das técnicas de várias amostras, essa é a melhor aproximação possível para o quad.</span><span class="sxs-lookup"><span data-stu-id="34fdf-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="34fdf-129">(Consulte o [exemplo de antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) para uma cobertura completa de várias amostras.) Lembre-se de que, se o rasterizador preencher cada célula o quádruplo cruzado, a área resultante será da dimensão 5 x 5 em vez dos 4 x 4 desejados.</span><span class="sxs-lookup"><span data-stu-id="34fdf-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="34fdf-130">Se você assumir que as coordenadas de tela se originam no canto superior esquerdo da grade de exibição em vez do pixel superior esquerdo, o quad aparecerá exatamente como esperado.</span><span class="sxs-lookup"><span data-stu-id="34fdf-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="34fdf-131">No entanto, a diferença fica clara quando o quad recebe uma textura.</span><span class="sxs-lookup"><span data-stu-id="34fdf-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="34fdf-132">A ilustração a seguir mostra a textura 4 x 4 que você mapeará diretamente para o quad.</span><span class="sxs-lookup"><span data-stu-id="34fdf-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![ilustração de uma textura 4x4](images/maptex-fig5.png)

<span data-ttu-id="34fdf-134">Como a textura é 4 x 4 texels e a quádrupla é de 4 x 4 pixels, você pode esperar que o quádruplo texturizado apareça exatamente como a textura, independentemente do local na tela em que o Quad é desenhado.</span><span class="sxs-lookup"><span data-stu-id="34fdf-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="34fdf-135">No entanto, esse não é o caso; até mesmo pequenas alterações na posição influenciam como a textura é exibida.</span><span class="sxs-lookup"><span data-stu-id="34fdf-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="34fdf-136">A ilustração a seguir mostra como um quad entre (0, 0) e (4, 4) é exibido depois de ser rasterizado e texturizado.</span><span class="sxs-lookup"><span data-stu-id="34fdf-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![ilustração de um quad com textura texturizado de (0, 0) e (4, 4)](images/maptex-fig6.png)

<span data-ttu-id="34fdf-138">O quad desenhado na ilustração anterior mostra a saída texturizada (com um modo de filtragem linear e um modo de endereçamento fixe) com a estrutura de tópicos rasterizada sobreposta.</span><span class="sxs-lookup"><span data-stu-id="34fdf-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="34fdf-139">O restante deste artigo explica exatamente por que a saída tem a aparência que ela faz, em vez de se parecer com a textura, mas para aqueles que desejam a solução, aqui está: as bordas da entrada Quad precisam estar sobre as linhas de limite entre células de pixel.</span><span class="sxs-lookup"><span data-stu-id="34fdf-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="34fdf-140">Simplesmente deslocando as coordenadas x e y em 0,5 unidades, as células de Texel abordarão perfeitamente as células de pixel e o quad poderá ser perfeitamente recriado na tela.</span><span class="sxs-lookup"><span data-stu-id="34fdf-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="34fdf-141">(A última ilustração neste tópico mostra o quad nas coordenadas corrigidas.)</span><span class="sxs-lookup"><span data-stu-id="34fdf-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="34fdf-142">Os detalhes de por que a saída rasterizada só tem ligeira semelhança com a textura de entrada estão diretamente relacionadas à maneira como os endereços e as texturas dos exemplos do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="34fdf-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="34fdf-143">O que segue pressupõe que você tenha uma boa compreensão do [espaço de coordenadas de textura](texture-coordinates.md) e da filtragem de [textura bilinear](bilinear-texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="34fdf-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="34fdf-144">Voltando à nossa investigação da saída de pixel estranho, faz sentido rastrear a cor de saída de volta para o sombreador de pixel: o sombreador de pixel é chamado para cada pixel selecionado para fazer parte da forma rasterizada.</span><span class="sxs-lookup"><span data-stu-id="34fdf-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="34fdf-145">O azul sólido quádruplo ilustrado em uma ilustração anterior poderia ter um sombreador especialmente simples:</span><span class="sxs-lookup"><span data-stu-id="34fdf-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="34fdf-146">Para o quad texturizado, o sombreador de pixel precisa ser alterado ligeiramente:</span><span class="sxs-lookup"><span data-stu-id="34fdf-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



<span data-ttu-id="34fdf-147">Esse código pressupõe que a textura 4 x 4 é armazenada em MyTexture.</span><span class="sxs-lookup"><span data-stu-id="34fdf-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="34fdf-148">Como mostrado, a amostra de textura myamostrador é definida para executar a filtragem bilinear em MyTexture.</span><span class="sxs-lookup"><span data-stu-id="34fdf-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="34fdf-149">O sombreador de pixel é chamado uma vez para cada pixel rasterizado, e cada vez que a cor retornada é a cor de textura amostrada em vTexCoord.</span><span class="sxs-lookup"><span data-stu-id="34fdf-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="34fdf-150">Cada vez que o sombreador de pixel é chamado, o argumento vTexCoord é definido como as coordenadas de textura nesse pixel.</span><span class="sxs-lookup"><span data-stu-id="34fdf-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="34fdf-151">Isso significa que o sombreador está solicitando a amostra de textura da cor de textura filtrada no local exato do pixel, conforme detalhado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="34fdf-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![ilustração de locais de amostragem para coordenadas de textura](images/maptex-fig7.png)

<span data-ttu-id="34fdf-153">A textura (mostrada como sobreposta) é amostrada diretamente em locais de pixel (mostrados como pontos pretos).</span><span class="sxs-lookup"><span data-stu-id="34fdf-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="34fdf-154">As coordenadas de textura não são afetadas pela rasterização (elas permanecem no espaço de tela projetado do quádruplo original).</span><span class="sxs-lookup"><span data-stu-id="34fdf-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="34fdf-155">Os pontos pretos mostram onde estão os pixels de rasterização.</span><span class="sxs-lookup"><span data-stu-id="34fdf-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="34fdf-156">As coordenadas de textura em cada pixel são facilmente determinadas com a interpolação das coordenadas armazenadas em cada vértice: o pixel em (0, 0) coincide com o vértice em (0, 0); Portanto, as coordenadas de textura nesse pixel são simplesmente as coordenadas de textura armazenadas nesse vértice, UV (0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="34fdf-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="34fdf-157">Para o pixel em (3, 1), as coordenadas interpoladas são UV (0,75, 0,25) porque esse pixel está localizado em três quartos da largura da textura e um quarto de sua altura.</span><span class="sxs-lookup"><span data-stu-id="34fdf-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="34fdf-158">Essas coordenadas interpoladas são as que são passadas para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="34fdf-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="34fdf-159">O texels não se alinha com os pixels neste exemplo; cada pixel (e, portanto, cada ponto de amostragem) está posicionado no canto de quatro texels.</span><span class="sxs-lookup"><span data-stu-id="34fdf-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="34fdf-160">Como o modo de filtragem é definido como linear, a amostra calculará a média das cores dos quatro texels compartilhando esse canto.</span><span class="sxs-lookup"><span data-stu-id="34fdf-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="34fdf-161">Isso explica por que o pixel esperado para ser vermelho é, na verdade, de três quartos cinzas, além de um quarto de vermelho, o pixel esperado para ser verde é um meio-meio-meio do vermelho, além de um quarto de verde e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="34fdf-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="34fdf-162">Para corrigir esse problema, tudo o que você precisa fazer é mapear corretamente o Quad para os pixels para os quais ele será rasterizado e, assim, mapear corretamente o texels para pixels.</span><span class="sxs-lookup"><span data-stu-id="34fdf-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="34fdf-163">A ilustração a seguir mostra os resultados do desenho do mesmo Quad entre (-0,5,-0,5) e (3,5, 3,5), que é o quad planejado desde o início.</span><span class="sxs-lookup"><span data-stu-id="34fdf-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![ilustração de um quad texturizado que corresponde ao Quad rasterizado](images/maptex-fig8.png)

<span data-ttu-id="34fdf-165">A ilustração anterior demonstra que o quad (mostrado descrito a partir de (-0,5,-0,5) a (3,5, 3,5)) corresponde exatamente à área rasterizada.</span><span class="sxs-lookup"><span data-stu-id="34fdf-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="34fdf-166">Resumo</span><span class="sxs-lookup"><span data-stu-id="34fdf-166">Summary</span></span>

<span data-ttu-id="34fdf-167">Em resumo, pixels e texels são realmente pontos, não blocos sólidos.</span><span class="sxs-lookup"><span data-stu-id="34fdf-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="34fdf-168">O espaço da tela é originado no pixel superior esquerdo, mas as coordenadas de textura se originam no canto superior esquerdo da grade da textura.</span><span class="sxs-lookup"><span data-stu-id="34fdf-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="34fdf-169">Mais importante, lembre-se de subtrair 0,5 unidades dos componentes x e y de suas posições de vértice ao trabalhar no espaço de tela transformado para alinhar corretamente o texels com pixels.</span><span class="sxs-lookup"><span data-stu-id="34fdf-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="34fdf-170">O código a seguir é um exemplo de deslocamento dos vértices de um quadrado de 256 por 256 para exibir corretamente uma textura 256 por 256 no espaço da tela transformada.</span><span class="sxs-lookup"><span data-stu-id="34fdf-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a><span data-ttu-id="34fdf-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34fdf-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34fdf-172">Coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="34fdf-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



