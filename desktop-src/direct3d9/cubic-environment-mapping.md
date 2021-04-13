---
description: Mapas de ambiente cúbico – às vezes chamados de mapas de cubo – são texturas que contêm dados de imagem representando a cena em torno de um objeto, como se o objeto estivesse no centro de um cubo.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Mapeamento de ambiente cúbico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecac83db067224195883485bcbd282aa82ae4b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370496"
---
# <a name="cubic-environment-mapping-direct3d-9"></a><span data-ttu-id="0cd07-103">Mapeamento de ambiente cúbico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cd07-103">Cubic Environment Mapping (Direct3D 9)</span></span>

<span data-ttu-id="0cd07-104">Mapas de ambiente cúbico – às vezes chamados de mapas de cubo – são texturas que contêm dados de imagem representando a cena em torno de um objeto, como se o objeto estivesse no centro de um cubo.</span><span class="sxs-lookup"><span data-stu-id="0cd07-104">Cubic environment maps - sometimes referred to as cube maps - are textures that contain image data representing the scene surrounding an object, as if the object were in the center of a cube.</span></span> <span data-ttu-id="0cd07-105">Cada face do mapa de ambiente cúbico cobre um campo de exibição de 90 graus na horizontal e na vertical, e há seis faces por mapa de cubo.</span><span class="sxs-lookup"><span data-stu-id="0cd07-105">Each face of the cubic environment map covers a 90-degree field of view in the horizontal and vertical, and there are six faces per cube map.</span></span> <span data-ttu-id="0cd07-106">A orientação das faces é mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cd07-106">The orientation of the faces is shown in the following illustration.</span></span>

![ilustração de um cubo com eixos de coordenadas centrais perpendiculares a rostos de cubo](images/cubemap-cube.png)

<span data-ttu-id="0cd07-108">Cada face do cubo é orientada perpendicularmente ao plano x/y, y/z ou x/z, no espaço de mundo.</span><span class="sxs-lookup"><span data-stu-id="0cd07-108">Each face of the cube is oriented perpendicular to the x/y, y/z, or x/z plane, in world space.</span></span> <span data-ttu-id="0cd07-109">A ilustração a seguir mostra como cada plano corresponde a uma face.</span><span class="sxs-lookup"><span data-stu-id="0cd07-109">The following illustration shows how each plane corresponds to a face.</span></span>

![ilustração de rostos de cubo com projeções de coordenadas de planos](images/cube-faces.png)

<span data-ttu-id="0cd07-111">Os mapas de ambiente cúbico são implementados como uma série de objetos de textura.</span><span class="sxs-lookup"><span data-stu-id="0cd07-111">Cubic environment maps are implemented as a series of texture objects.</span></span> <span data-ttu-id="0cd07-112">Os aplicativos podem usar imagens estáticas para o mapeamento de ambiente cúbico ou podem renderizar nas faces do mapa do cubo para executar o mapeamento de ambiente dinâmico.</span><span class="sxs-lookup"><span data-stu-id="0cd07-112">Applications can use static images for cubic environment mapping, or they can render into the faces of the cube map to perform dynamic environment mapping.</span></span> <span data-ttu-id="0cd07-113">Essa técnica requer que as superfícies de mapa de cubo sejam superfícies de destino de renderização válidas, criadas com o \_ sinalizador D3DUSAGE RENDERTARGET definido.</span><span class="sxs-lookup"><span data-stu-id="0cd07-113">This technique requires that the cube-map surfaces be valid render-target surfaces, created with the D3DUSAGE\_RENDERTARGET flag set.</span></span>

<span data-ttu-id="0cd07-114">As faces de um mapa de cubo não precisam conter renderizações extremamente detalhadas da cena ao redor.</span><span class="sxs-lookup"><span data-stu-id="0cd07-114">The faces of a cube map don't need to contain extremely detailed renderings of the surrounding scene.</span></span> <span data-ttu-id="0cd07-115">Na maioria dos casos, os mapas de ambiente são aplicados a superfícies curvas.</span><span class="sxs-lookup"><span data-stu-id="0cd07-115">In most cases, environment maps are applied to curved surfaces.</span></span> <span data-ttu-id="0cd07-116">Considerando a quantidade de curvatura usada pela maioria dos aplicativos, a distorção refletida resultante faz com que detalhes extremos no mapa do ambiente sejam dispendiosos em termos de sobrecarga de memória e renderização.</span><span class="sxs-lookup"><span data-stu-id="0cd07-116">Given the amount of curvature used by most applications, the resulting reflective distortion makes extreme detail in the environment map wasteful in terms of memory and rendering overhead.</span></span>

## <a name="mipmapped-cubic-environment-maps"></a><span data-ttu-id="0cd07-117">Mapas de ambiente mipmapped cúbico</span><span class="sxs-lookup"><span data-stu-id="0cd07-117">Mipmapped Cubic Environment Maps</span></span>

<span data-ttu-id="0cd07-118">Os mapas de cubo podem ser mipmapped.</span><span class="sxs-lookup"><span data-stu-id="0cd07-118">Cube maps can be mipmapped.</span></span> <span data-ttu-id="0cd07-119">Para criar um mapa de cubo mipmapped, defina o parâmetro níveis do método [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) como o número de níveis que você deseja.</span><span class="sxs-lookup"><span data-stu-id="0cd07-119">To create a mipmapped cube map, set the Levels parameter of the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method to the number of levels that you want.</span></span> <span data-ttu-id="0cd07-120">Você pode prever a topografia dessas superfícies, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cd07-120">You can envision the topography of these surfaces as shown in the following diagram.</span></span>

![diagrama de um mapa de cubo mipmapped com n níveis de MIP](images/cubemap-mipped.png)

<span data-ttu-id="0cd07-122">Os aplicativos que criam mapas de ambiente cúbico mipmapped podem acessar cada face chamando o método [**GetCubeMapSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0cd07-122">Applications that create mipmapped cubic environment maps can access each face by calling the [**GetCubeMapSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="0cd07-123">Comece definindo o valor apropriado do tipo enumerado [**D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md) , conforme discutido em [criando superfícies de mapa de ambiente cúbico (Direct3D 9)](creating-cubic-environment-map-surfaces.md).</span><span class="sxs-lookup"><span data-stu-id="0cd07-123">Start by setting the appropriate value from the [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated type, as discussed in [Creating Cubic Environment Map Surfaces (Direct3D 9)](creating-cubic-environment-map-surfaces.md).</span></span> <span data-ttu-id="0cd07-124">Em seguida, selecione o nível a ser recuperado definindo o parâmetro de nível **GetCubeMapSurface** para o nível de mipmap que você deseja.</span><span class="sxs-lookup"><span data-stu-id="0cd07-124">Next, select the level to retrieve by setting the **GetCubeMapSurface** level parameter to the mipmap level that you want.</span></span> <span data-ttu-id="0cd07-125">Lembre-se de que 0 corresponde à imagem de nível superior.</span><span class="sxs-lookup"><span data-stu-id="0cd07-125">Remember that 0 corresponds with the top-level image.</span></span>

## <a name="texture-coordinates-for-cubic-environment-maps"></a><span data-ttu-id="0cd07-126">Coordenadas de textura para mapas de ambiente cúbico</span><span class="sxs-lookup"><span data-stu-id="0cd07-126">Texture Coordinates for Cubic Environment Maps</span></span>

<span data-ttu-id="0cd07-127">As coordenadas de textura que indexam um mapa de ambiente cúbico não são coordenadas simples de u, v Style, conforme usadas quando as texturas padrão são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="0cd07-127">Texture coordinates that index a cubic environment map aren't simple u, v style coordinates, as used when standard textures are applied.</span></span> <span data-ttu-id="0cd07-128">Na verdade, os mapas de ambiente cúbico não usam coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0cd07-128">In fact, cubic environment maps don't use texture coordinates at all.</span></span> <span data-ttu-id="0cd07-129">No lugar de um conjunto de coordenadas de textura, os mapas de ambiente cúbico exigem um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="0cd07-129">In place of a set of texture coordinates, cubic environment maps require a 3D vector.</span></span> <span data-ttu-id="0cd07-130">Você deve tomar cuidado para especificar um formato de vértice adequado.</span><span class="sxs-lookup"><span data-stu-id="0cd07-130">You must take care to specify a proper vertex format.</span></span> <span data-ttu-id="0cd07-131">Além de informar ao sistema Quantos conjuntos de coordenadas de textura seu aplicativo usa, você deve fornecer informações sobre quantos elementos estão em cada conjunto.</span><span class="sxs-lookup"><span data-stu-id="0cd07-131">In addition to telling the system how many sets of texture coordinates your application uses, you must provide information about how many elements are in each set.</span></span> <span data-ttu-id="0cd07-132">O Direct3D oferece o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="0cd07-132">Direct3D offers the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros for this purpose.</span></span> <span data-ttu-id="0cd07-133">Essas macros aceitam um único parâmetro, identificando o índice do conjunto de coordenadas de textura para o qual o tamanho está sendo descrito.</span><span class="sxs-lookup"><span data-stu-id="0cd07-133">These macros accept a single parameter, identifying the index of the texture coordinate set for which the size is being described.</span></span> <span data-ttu-id="0cd07-134">No caso de um vetor 3D, você inclui o padrão de bits criado pela macro D3DFVF \_ TEXCOORDSIZE3.</span><span class="sxs-lookup"><span data-stu-id="0cd07-134">In the case of a 3D vector, you include the bit pattern created by the D3DFVF\_TEXCOORDSIZE3 macro.</span></span> <span data-ttu-id="0cd07-135">O exemplo de código a seguir mostra como essa macro é usada.</span><span class="sxs-lookup"><span data-stu-id="0cd07-135">The following code example shows how this macro is used.</span></span>


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



<span data-ttu-id="0cd07-136">Em alguns casos, como o mapeamento de luz difusa, você usa o vértice de espaço de câmera normal para o vetor.</span><span class="sxs-lookup"><span data-stu-id="0cd07-136">In some cases, such as diffuse light mapping, you use the camera-space vertex normal for the vector.</span></span> <span data-ttu-id="0cd07-137">Em outros casos, como o mapeamento de ambiente especular, você usa um vetor de reflexão.</span><span class="sxs-lookup"><span data-stu-id="0cd07-137">In other cases, like specular environment mapping, you use a reflection vector.</span></span> <span data-ttu-id="0cd07-138">Como os normais de vértice transformados são amplamente compreendidos, as informações aqui se concentram em calcular um vetor de reflexo.</span><span class="sxs-lookup"><span data-stu-id="0cd07-138">Because transformed vertex normals are widely understood, the information here concentrates on computing a reflection vector.</span></span>

<span data-ttu-id="0cd07-139">A computação de um vetor de reflexo por conta própria requer a compreensão da posição de cada vértice e de um vetor do ponto de vista para esse vértice.</span><span class="sxs-lookup"><span data-stu-id="0cd07-139">Computing a reflection vector on your own requires understanding of the position of each vertex, and of a vector from the viewpoint to that vertex.</span></span> <span data-ttu-id="0cd07-140">O Direct3D pode calcular automaticamente os vetores de reflexo para sua geometria.</span><span class="sxs-lookup"><span data-stu-id="0cd07-140">Direct3D can automatically compute the reflection vectors for your geometry.</span></span> <span data-ttu-id="0cd07-141">O uso desse recurso poupa memória porque você não precisa incluir coordenadas de textura para o mapa de ambiente.</span><span class="sxs-lookup"><span data-stu-id="0cd07-141">Using this feature saves memory because you don't need to include texture coordinates for the environment map.</span></span> <span data-ttu-id="0cd07-142">Ele também reduz a largura de banda e, no caso de um dispositivo de HAL T&L, ele pode ser significativamente mais rápido do que os cálculos que seu aplicativo pode fazer por conta própria.</span><span class="sxs-lookup"><span data-stu-id="0cd07-142">It also reduces bandwidth and, in the case of a T&L HAL Device, it can be significantly faster than the computations that your application can make on its own.</span></span> <span data-ttu-id="0cd07-143">Para usar esse recurso, no estágio de textura que contém o mapa de ambiente cúbico, defina o \_ estado de estágio de textura D3DTSS TEXCOORDINDEX como uma combinação do \_ membro D3DTSS TCI \_ CAMERASPACEREFLECTIONVECTOR de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) e o índice de um conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0cd07-143">To use this feature, in the texture stage that contains the cubic environment map, set the D3DTSS\_TEXCOORDINDEX texture stage state to a combination of the D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR member of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) and the index of a texture coordinate set.</span></span> <span data-ttu-id="0cd07-144">Em algumas situações, como o mapeamento de luz difusa, você pode usar o \_ membro D3DTSS TCI \_ CAMERASPACENORMAL de **D3DTEXTURESTAGESTATETYPE**, o que faz com que o sistema use o vértice transformado, câmera-espaço, normal como o vetor de endereçamento para a textura.</span><span class="sxs-lookup"><span data-stu-id="0cd07-144">In some situations, like diffuse light mapping, you might use the D3DTSS\_TCI\_CAMERASPACENORMAL member of **D3DTEXTURESTAGESTATETYPE**, which causes the system to use the transformed, camera-space, vertex normal as the addressing vector for the texture.</span></span> <span data-ttu-id="0cd07-145">O índice é usado apenas pelo sistema para determinar o modo de disposição para a textura.</span><span class="sxs-lookup"><span data-stu-id="0cd07-145">The index is only used by the system to determine the wrapping mode for the texture.</span></span>

<span data-ttu-id="0cd07-146">O exemplo de código a seguir mostra como esse valor é usado.</span><span class="sxs-lookup"><span data-stu-id="0cd07-146">The following code example shows how this value is used.</span></span>


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



<span data-ttu-id="0cd07-147">Quando você habilita a geração de coordenadas de textura automática, o sistema usa uma das duas fórmulas para calcular o vetor de reflexão para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="0cd07-147">When you enable automatic texture coordinate generation, the system uses one of two formulas to compute the reflection vector for each vertex.</span></span> <span data-ttu-id="0cd07-148">Quando o \_ estado de RENDERIZAÇÃO D3DRS LOCALVIEWER é definido como **true**, a fórmula a seguir é usada.</span><span class="sxs-lookup"><span data-stu-id="0cd07-148">When the D3DRS\_LOCALVIEWER render state is set to **TRUE**, the following formula is used.</span></span>

![fórmula do vetor de reflexão (r = 2 (exn) n-e)](images/reflection-vector-local.png)

<span data-ttu-id="0cd07-150">Na fórmula anterior, R é o vetor de reflexo sendo computado, E é o vetor de posição-para-olho normalizado e N é o vértice de espaço de câmera normal.</span><span class="sxs-lookup"><span data-stu-id="0cd07-150">In the preceding formula, R is the reflection vector being computed, E is the normalized position-to-eye vector, and N is the camera-space vertex normal.</span></span>

<span data-ttu-id="0cd07-151">Quando o \_ estado de RENDERIZAÇÃO D3DRS LOCALVIEWER é definido como **false**, o sistema usa a fórmula a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cd07-151">When the D3DRS\_LOCALVIEWER render state is set to **FALSE**, the system uses the following formula.</span></span>

![fórmula do vetor de reflexão (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

<span data-ttu-id="0cd07-153">Os elementos R e N nesta fórmula são idênticos à fórmula anterior.</span><span class="sxs-lookup"><span data-stu-id="0cd07-153">The R and N elements in this formula are identical to the previous formula.</span></span> <span data-ttu-id="0cd07-154">O elemento N<sub>z</sub> é a Z de espaço Mundial do vértice normal e I é o vetor (0, 0, 1) de um ponto de vista infinitamente distante.</span><span class="sxs-lookup"><span data-stu-id="0cd07-154">The N<sub>Z</sub> element is the world-space z of the vertex normal, and I is the vector (0,0,1) of an infinitely distant viewpoint.</span></span> <span data-ttu-id="0cd07-155">O sistema usa o vetor de reflexo de uma das fórmulas para selecionar e tratar a face apropriada do mapa do cubo.</span><span class="sxs-lookup"><span data-stu-id="0cd07-155">The system uses the reflection vector from either formula to select and address the appropriate face of the cube map.</span></span>

> [!Note]  
> <span data-ttu-id="0cd07-156">Na maioria dos casos, os aplicativos devem habilitar a normalização automática de Normals de vértice.</span><span class="sxs-lookup"><span data-stu-id="0cd07-156">In most cases, applications should enable automatic normalization of vertex normals.</span></span> <span data-ttu-id="0cd07-157">Para fazer isso, defina D3DRS \_ NORMALIZENORMALS como **true**.</span><span class="sxs-lookup"><span data-stu-id="0cd07-157">To do this, set D3DRS\_NORMALIZENORMALS to **TRUE**.</span></span> <span data-ttu-id="0cd07-158">Se você não habilitar esse estado de renderização, a aparência do mapa de ambiente será drasticamente diferente do que você pode esperar.</span><span class="sxs-lookup"><span data-stu-id="0cd07-158">If you do not enable this render state, the appearance of the environment map will be drastically different than you might expect.</span></span>

 

<span data-ttu-id="0cd07-159">Informações adicionais estão contidas no tópico a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cd07-159">Additional information is contained in the following topic.</span></span>

-   [<span data-ttu-id="0cd07-160">Criando superfícies de mapa de ambiente cúbico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0cd07-160">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a><span data-ttu-id="0cd07-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0cd07-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cd07-162">Mapeamento de ambiente</span><span class="sxs-lookup"><span data-stu-id="0cd07-162">Environment Mapping</span></span>](environment-mapping.md)
</dt> </dl>

 

 
