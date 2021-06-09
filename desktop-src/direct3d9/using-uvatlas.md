---
description: Muitas técnicas de renderização e geração de conteúdo exigem um mapa exclusivo e não sobreposto de um sinal 2D (como uma textura) em uma malha.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Usando o UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826324"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="6cafa-103">Usando o UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6cafa-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="6cafa-104">O UVAtlas foi originalmente enviado na biblioteca D3DX9 utilitário preterida agora.</span><span class="sxs-lookup"><span data-stu-id="6cafa-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="6cafa-105">A versão mais recente está disponível na [ferramenta de Command-Line (uvatlas.exe) de UV do Atlas](https://github.com/Microsoft/UVAtlas).</span><span class="sxs-lookup"><span data-stu-id="6cafa-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="6cafa-106">Muitas técnicas de renderização e geração de conteúdo exigem um mapa exclusivo e não sobreposto de um sinal 2D (como uma textura) em uma malha.</span><span class="sxs-lookup"><span data-stu-id="6cafa-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="6cafa-107">Essas técnicas incluem:</span><span class="sxs-lookup"><span data-stu-id="6cafa-107">Such techniques include:</span></span>

-   <span data-ttu-id="6cafa-108">Mapeamento normal/de deslocamento</span><span class="sxs-lookup"><span data-stu-id="6cafa-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="6cafa-109">Simulações de simulação de espaço de textura e mapas leves</span><span class="sxs-lookup"><span data-stu-id="6cafa-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="6cafa-110">Pintura da superfície</span><span class="sxs-lookup"><span data-stu-id="6cafa-110">Surface painting</span></span>
-   <span data-ttu-id="6cafa-111">Textura-iluminação de espaço</span><span class="sxs-lookup"><span data-stu-id="6cafa-111">Texture-space lighting</span></span>

<span data-ttu-id="6cafa-112">A geração manual de um mapeamento UV exclusivo é sempre demorada e entediante; Isso é especialmente verdadeiro quando a geometria de entrada é complexa e eficiente/de textura de distorção. a utilização de espaço é desejada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="6cafa-113">A ilustração a seguir mostra uma malha de exemplo e seu Atlas de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cafa-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Mostra uma malha de exemplo e seu Atlas de textura correspondente.](images/uvatlas1.jpg)

<span data-ttu-id="6cafa-115">Este exemplo mostra uma malha (à esquerda) e o mapa normal de um espaço UV correspondente (à direita).</span><span class="sxs-lookup"><span data-stu-id="6cafa-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="6cafa-116">Observe que o Atlas de textura contém vários grupos ou clusters de dados; cada cluster é chamado de gráfico e, no exemplo acima, exibe contém os dados normais de uma parte da malha.</span><span class="sxs-lookup"><span data-stu-id="6cafa-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="6cafa-117">As APIs D3DX UVAtlas geram automaticamente um Atlas de textura ideal e não sobreposto.</span><span class="sxs-lookup"><span data-stu-id="6cafa-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="6cafa-118">As APIs fornecem parâmetros de entrada que permitem:</span><span class="sxs-lookup"><span data-stu-id="6cafa-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="6cafa-119">Minimize o Stretch, distorção e subamostramento de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="6cafa-120">Maximize a densidade de empacotamento de espaço de textura para uso eficiente da memória.</span><span class="sxs-lookup"><span data-stu-id="6cafa-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="6cafa-121">Forneça uma amostragem uniforme em toda a malha, minimizando descontinuidades na frequência de amostragem.</span><span class="sxs-lookup"><span data-stu-id="6cafa-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="6cafa-122">Como o UVAtlas funciona</span><span class="sxs-lookup"><span data-stu-id="6cafa-122">How UVAtlas Works</span></span>

<span data-ttu-id="6cafa-123">As APIs do UVAtlas (consulte [funções do UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) geram um Atlas de textura Particionando uma superfície em gráficos e empacotando os gráficos em um Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="6cafa-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) e [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para executar essas etapas separadamente; ou use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) para particionar, parametrizar e empacotar em uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="6cafa-125">Particionando e parametrizando uma malha</span><span class="sxs-lookup"><span data-stu-id="6cafa-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="6cafa-126">Usando tempos de métricas integrados para controlar a parametrização</span><span class="sxs-lookup"><span data-stu-id="6cafa-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="6cafa-127">Usando dados de adjacência para vincos especificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="6cafa-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="6cafa-128">Empacotando gráficos em um Atlas</span><span class="sxs-lookup"><span data-stu-id="6cafa-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="6cafa-129">Particionando e parametrizando uma malha</span><span class="sxs-lookup"><span data-stu-id="6cafa-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="6cafa-130">Primeiro, a malha é particionada em gráficos e, em seguida, cada gráfico é parametrizado em seu próprio \[ 0, 1 \] UV-espaço.</span><span class="sxs-lookup"><span data-stu-id="6cafa-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="6cafa-131">Um cilindro pode ser parametrizado por um gráfico; uma esfera por outro lado exigirá dois gráficos, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cafa-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![ilustração de uma esfera particionada em dois gráficos](images/uvatlas3.jpg)

<span data-ttu-id="6cafa-133">Uma malha que pode ser parametrizada com um único gráfico é classificada como "homeomorphic para um disco", o que significa que você pode distribuir um disco infinitamente flexível e infinitamente expansível no gráfico e abordar a geometria perfeitamente.</span><span class="sxs-lookup"><span data-stu-id="6cafa-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="6cafa-134">Esse alongamento, chamado de homeomorphism, é uma função bidirecional; Isso significa que você pode ir de uma parametrização para a outra sem perder informações.</span><span class="sxs-lookup"><span data-stu-id="6cafa-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="6cafa-135">Poucas malhas do mundo real podem ser parametrizadas em duas dimensões sem separar a malha em clusters ou em gráficos.</span><span class="sxs-lookup"><span data-stu-id="6cafa-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="6cafa-136">A ilustração a seguir mostra outra malha de exemplo e seu Atlas de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cafa-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Mostra uma malha de exemplo com formas diferentes e seu Atlas de textura correspondente.](images/uvatlas2.jpg)

<span data-ttu-id="6cafa-138">Há dois parâmetros que determinam o número de gráficos criados:</span><span class="sxs-lookup"><span data-stu-id="6cafa-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="6cafa-139">O número máximo de gráficos permitidos para o Atlas</span><span class="sxs-lookup"><span data-stu-id="6cafa-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="6cafa-140">A quantidade máxima de ampliação permitida para cada gráfico</span><span class="sxs-lookup"><span data-stu-id="6cafa-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="6cafa-141">A quantidade de ampliação determinará o número de gráficos que são gerados e a qualidade geral da amostragem.</span><span class="sxs-lookup"><span data-stu-id="6cafa-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="6cafa-142">Stretch varia de 0,0 (sem Stretch) a 1,0 (qualquer quantidade de Stretch).</span><span class="sxs-lookup"><span data-stu-id="6cafa-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="6cafa-143">D3DXUVAtlasCreate e D3DXUVAtlasPartition retornam o Stretch máximo gerado pelo algoritmo.</span><span class="sxs-lookup"><span data-stu-id="6cafa-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="6cafa-144">A ilustração a seguir mostra outra malha de exemplo e seu Atlas de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="6cafa-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![ilustração de uma malha de exemplo e seu Atlas de textura correspondente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="6cafa-146">Usando tempos de métricas integrados para controlar a parametrização</span><span class="sxs-lookup"><span data-stu-id="6cafa-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="6cafa-147">A priorização de espaço de textura pode ser especificada por triângulo.</span><span class="sxs-lookup"><span data-stu-id="6cafa-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="6cafa-148">Os tempos de métrica integrados podem ser fornecidos para controlar como os triângulos são esticados no Atlas de espaço de textura resultante.</span><span class="sxs-lookup"><span data-stu-id="6cafa-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="6cafa-149">IMT pode ser especificado diretamente ou computado com base em um sinal de entrada usando as funções de computação IMT D3DX.</span><span class="sxs-lookup"><span data-stu-id="6cafa-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="6cafa-150">Uma métrica integrada tensor (ou IMT) é uma matriz 2x2 simétrica que descreve como um triângulo é esticado no Atlas.</span><span class="sxs-lookup"><span data-stu-id="6cafa-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="6cafa-151">Cada IMT é definido por 3 floats, chamá-los (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="6cafa-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="6cafa-152">Eles podem ser organizados em uma matriz de 2x2 simétrica como esta:</span><span class="sxs-lookup"><span data-stu-id="6cafa-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="6cafa-153">Em seguida, o IMT pode ser usado para localizar a distância entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="6cafa-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="6cafa-154">Considerando dois vetores v1 e v2, em que:</span><span class="sxs-lookup"><span data-stu-id="6cafa-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="6cafa-155">A distância entre v1 e V2 pode ser calculada como:</span><span class="sxs-lookup"><span data-stu-id="6cafa-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="6cafa-156">Em outras palavras, o vetor (s, t) pode ser a magnitude da ampliação em uma direção arbitrária no espaço de u-v.</span><span class="sxs-lookup"><span data-stu-id="6cafa-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="6cafa-157">Nesse caso, o vetor s é uma direção do primeiro ao segundo vértice, e t é o produto cruzado do normal e do s.</span><span class="sxs-lookup"><span data-stu-id="6cafa-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="6cafa-158">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="6cafa-158">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="6cafa-159">IMT pode ser especificado diretamente ou computado com base em um sinal de entrada usando as funções de computação IMT D3DX: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal e D3DXComputeIMTFromTexture \_ Graphics.</span><span class="sxs-lookup"><span data-stu-id="6cafa-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="6cafa-160">Especifique os dados do IMT diretamente se desejar controlar como a textura-espaço é alocada a triângulos individuais.</span><span class="sxs-lookup"><span data-stu-id="6cafa-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="6cafa-161">Ao fazer isso, aloque mais área no Atlas para áreas importantes de uma malha (como o logotipo facial ou conjunto de um caractere, ou regiões de uma cena perto do caminho de percurso de um jogador).</span><span class="sxs-lookup"><span data-stu-id="6cafa-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="6cafa-162">Ao especificar IMT que são múltiplos da matriz de identidade, os triângulos resultantes serão dimensionados uniformemente no espaço de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="6cafa-163">Por exemplo, dado um mapa normal de alta resolução, você pode calcular IMT para fornecer mais espaço de textura para áreas de sinal de frequência mais alta no mapa normal.</span><span class="sxs-lookup"><span data-stu-id="6cafa-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="6cafa-164">Os triângulos que são "simples" (mapeados para regiões constantes do mapa normal original) receberão menos espaço de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="6cafa-165">Os triângulos que contêm uma grande quantidade de detalhes do mapa normal receberão mais área de textura no resultado final.</span><span class="sxs-lookup"><span data-stu-id="6cafa-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="6cafa-166">Em seguida, você pode reamostrar o mapa normal em uma textura menor, mas manter detalhes, ou pode recalcular o mapa normal com o mapeamento UV ideal.</span><span class="sxs-lookup"><span data-stu-id="6cafa-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="6cafa-167">Usando dados de adjacência para vincos especificados pelo usuário</span><span class="sxs-lookup"><span data-stu-id="6cafa-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="6cafa-168">As informações de adjacência definidas pelo usuário podem ser fornecidas à função de particionamento para descrever os vincos predefinidos na malha e, portanto, definir um limite de gráfico entre rostos adjacentes.</span><span class="sxs-lookup"><span data-stu-id="6cafa-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="6cafa-169">Essa é uma maneira simples para o chamador especificar seu próprio particionamento de gráfico como entrada no algoritmo, o que refinará ainda mais os gráficos para trazer a ampliação para o máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="6cafa-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="6cafa-170">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6cafa-170">Example</span></span>

<span data-ttu-id="6cafa-171">Este exemplo ilustra como você pode usar as APIs UVAtlas e o DirectX Viewer (Dxviewer.exe) para localizar e corrigir descontinuidades em seu modelo que pode afetar drasticamente o tamanho do seu Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="6cafa-172">Você pode obter Dxviewer.exe e aprender sobre ele no SDK do DirectX.</span><span class="sxs-lookup"><span data-stu-id="6cafa-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="6cafa-173">Dxviewer.exe foi removido do SDK do DirectX após a versão de agosto de 2009 para que seja necessário ter pelo menos o SDK do DirectX de agosto de 2009.</span><span class="sxs-lookup"><span data-stu-id="6cafa-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="6cafa-174">Para obter informações sobre o SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="6cafa-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="6cafa-175">Suponha que você começou com algum modelo em seu software de geração de conteúdo favorito (Este exemplo usa um modelo de cabeçalho Dwarf que foi criado em Maya).</span><span class="sxs-lookup"><span data-stu-id="6cafa-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="6cafa-176">Exporte o modelo texturizado para um arquivo. x e crie um Atlas de textura com D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="6cafa-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="6cafa-177">O Atlas de textura resultante ficaria parecido com a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cafa-177">The resulting texture atlas would look something like the following illustration.</span></span>

![ilustração de um Atlas para um modelo Dwarf](images/uvatlas5.jpg)

<span data-ttu-id="6cafa-179">O Atlas tem 22 gráficos e um Stretch máximo de 0,994.</span><span class="sxs-lookup"><span data-stu-id="6cafa-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="6cafa-180">Agora, examine o modelo texturizado para ver como o Atlas de textura é mapeado para a geometria.</span><span class="sxs-lookup"><span data-stu-id="6cafa-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="6cafa-181">Para fazer isso, carregue o modelo na ferramenta de visualização:</span><span class="sxs-lookup"><span data-stu-id="6cafa-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="6cafa-182">Abra a ferramenta de visualização dos utilitários do DirectX.</span><span class="sxs-lookup"><span data-stu-id="6cafa-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="6cafa-183">Carregue o arquivo. x clicando no botão abrir.</span><span class="sxs-lookup"><span data-stu-id="6cafa-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="6cafa-184">Habilitando a opção de exibição de vinco clicando no botão exibir e selecionando vincos de pop-up.</span><span class="sxs-lookup"><span data-stu-id="6cafa-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="6cafa-185">A ilustração a seguir mostra o que você deve ver na ferramenta do visualizador.</span><span class="sxs-lookup"><span data-stu-id="6cafa-185">The following illustration shows what you should see in the viewer tool.</span></span>

![ilustração de uma malha texturizada na ferramenta do Visualizador](images/uvatlas6c.jpg)

<span data-ttu-id="6cafa-187">Cada linha é um vinco que é uma borda adjacente entre dois gráficos no Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="6cafa-188">O número de gráficos gerados pelo algoritmo é causado por pequenas diferenças, talvez devido a descontinuidades nos normais.</span><span class="sxs-lookup"><span data-stu-id="6cafa-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="6cafa-189">Essas pequenas diferenças podem ser reduzidas por dados de soldagem, ou seja, forçar os dados que são quase iguais a serem iguais.</span><span class="sxs-lookup"><span data-stu-id="6cafa-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="6cafa-190">Para soldar os Normals e o skinweights:</span><span class="sxs-lookup"><span data-stu-id="6cafa-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="6cafa-191">Execute a ferramenta Ops (dxops.exe) do DirectX com a seguinte linha de comando na malha (substituindo ' ModelName. x ' pelo nome do seu modelo):</span><span class="sxs-lookup"><span data-stu-id="6cafa-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="6cafa-192">Isso compara os Normals e skinweights, e onde eles diferem em valor inferior a 2, 1, os dados são feitos iguais.</span><span class="sxs-lookup"><span data-stu-id="6cafa-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="6cafa-193">A ilustração a seguir mostra um fechamento do olho para ver os vincos antes do soldagem (à esquerda) e os vincos após a soldagem (à direita):</span><span class="sxs-lookup"><span data-stu-id="6cafa-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![ilustração de vincos antes de soldagem](images/uvatlas6a.jpg)![ilustração de vincos após soldagem](images/uvatlas6b.jpg)

<span data-ttu-id="6cafa-196">Figura 7: removendo vincos por soldagem</span><span class="sxs-lookup"><span data-stu-id="6cafa-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="6cafa-197">Neste exemplo, a soldagem removeu 86 vértices da malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="6cafa-198">Com menos vincos na malha, você pode regenerar o Atlas, como mostra a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cafa-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![ilustração do novo Atlas com vincos removidos](images/uvatlas8.jpg)

<span data-ttu-id="6cafa-200">O Atlas tem apenas 7 gráficos e um Stretch máximo de aproximadamente 0, 776.</span><span class="sxs-lookup"><span data-stu-id="6cafa-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="6cafa-201">O novo Atlas agora se encaixa em uma textura menor (aproximadamente 30% menor neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="6cafa-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="6cafa-202">Empacotando gráficos em um Atlas</span><span class="sxs-lookup"><span data-stu-id="6cafa-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="6cafa-203">Depois que uma malha é particionada em gráficos com parâmetros individuais, os gráficos precisam ser empacotados com eficiência em um único mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="6cafa-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="6cafa-204">Isso é executado como a segunda etapa de D3DXUVAtlasCreate ou pode ser invocado explicitamente chamando D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="6cafa-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="6cafa-205">Os gráficos empacotados são separados por uma largura de medianiz especificada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6cafa-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="6cafa-206">A largura da medianiz é a quantidade de separação entre os gráficos e permite a interpolação bilinear e o mapeamento de MIP para evitar a renderização de artefatos em limites do gráfico.</span><span class="sxs-lookup"><span data-stu-id="6cafa-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="6cafa-207">O D3DX fornece uma interface para preencher automaticamente essas medianizes-consulte [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6cafa-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="6cafa-208">Integrando o UVAtlas ao seu pipeline</span><span class="sxs-lookup"><span data-stu-id="6cafa-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="6cafa-209">Além de ser chamado de artista antes da pintura de textura, essas funções podem ser integradas em um pipeline de arte automatizado.</span><span class="sxs-lookup"><span data-stu-id="6cafa-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="6cafa-210">Por exemplo, uma chamada UVAtlas pode ser emitida automaticamente depois que um ativo é atualizado, antes de executar uma simulação de PRT ou uma passagem de mapeamento normal.</span><span class="sxs-lookup"><span data-stu-id="6cafa-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="6cafa-211">Isso evita que seja necessário reparar manualmente o mapeamento UV de um objeto se a topologia da malha tiver sido modificada.</span><span class="sxs-lookup"><span data-stu-id="6cafa-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="6cafa-212">Confira a [ferramenta UV Command-Line do Atlas (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) , por exemplo, o uso das funções UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="6cafa-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cafa-213">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cafa-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cafa-214">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="6cafa-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
