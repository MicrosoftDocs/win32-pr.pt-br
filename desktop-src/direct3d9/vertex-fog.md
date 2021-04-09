---
description: Quando o sistema executa o vértice fogging, ele aplica cálculos de neblina em cada vértice em um polígono e, em seguida, interpola os resultados em toda a face do polígono durante a rasterização.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Neblina de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087211"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="49d4a-103">Neblina de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="49d4a-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="49d4a-104">Quando o sistema executa o vértice fogging, ele aplica cálculos de neblina em cada vértice em um polígono e, em seguida, interpola os resultados em toda a face do polígono durante a rasterização.</span><span class="sxs-lookup"><span data-stu-id="49d4a-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="49d4a-105">Os efeitos de neblina de vértice são computados pelo mecanismo de iluminação e transformação de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="49d4a-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="49d4a-106">Para obter mais informações, consulte [parâmetros de neblina (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="49d4a-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="49d4a-107">Se seu aplicativo não usar o Direct3D para transformação e iluminação, o aplicativo deverá executar cálculos de neblina.</span><span class="sxs-lookup"><span data-stu-id="49d4a-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="49d4a-108">Nesse caso, coloque o fator de neblina que é calculado no componente alfa da cor especular para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="49d4a-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="49d4a-109">Você está livre para usar quaisquer fórmulas que desejar, com base em intervalo, volumétricos ou de outra forma.</span><span class="sxs-lookup"><span data-stu-id="49d4a-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="49d4a-110">O Direct3D usa o fator de neblina fornecido para interpolar em toda a face de cada polígono.</span><span class="sxs-lookup"><span data-stu-id="49d4a-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="49d4a-111">Os aplicativos que executam sua própria transformação e iluminação também devem executar seus próprios cálculos de neblina de vértice.</span><span class="sxs-lookup"><span data-stu-id="49d4a-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="49d4a-112">Como resultado, tal aplicativo precisa apenas habilitar a mesclagem de neblina e definir a cor de neblina por meio dos Estados de renderização associados, conforme descrito em [fusão de neblina (Direct3D 9)](fog-blending.md) e [cor de neblina (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="49d4a-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="49d4a-113">Ao usar um sombreador de vértice, você deve usar a neblina de vértice.</span><span class="sxs-lookup"><span data-stu-id="49d4a-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="49d4a-114">Isso é feito usando o sombreador de vértice para gravar a intensidade de neblina por vértice no registro oFog.</span><span class="sxs-lookup"><span data-stu-id="49d4a-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="49d4a-115">Depois que o sombreador de pixel é concluído, os dados de oFog são usados para interpolar linearmente com a cor de neblina.</span><span class="sxs-lookup"><span data-stu-id="49d4a-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="49d4a-116">Essa intensidade não está disponível em um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="49d4a-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="49d4a-117">Neblina Range-Based</span><span class="sxs-lookup"><span data-stu-id="49d4a-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="49d4a-118">O Direct3D usa cálculos de neblina com base em intervalos somente ao usar a neblina de vértice com o mecanismo de transformação e iluminação do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="49d4a-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="49d4a-119">Isso ocorre porque a neblina de pixel é implementada no driver de dispositivo e nenhum hardware existe atualmente para dar suporte à neblina baseada em intervalos por pixel.</span><span class="sxs-lookup"><span data-stu-id="49d4a-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="49d4a-120">Se seu aplicativo executar sua própria transformação e iluminação, ele deverá executar seus próprios cálculos de neblina, baseados em intervalo ou de outra forma.</span><span class="sxs-lookup"><span data-stu-id="49d4a-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="49d4a-121">Às vezes, usar a neblina pode introduzir artefatos gráficos que fazem com que os objetos sejam mesclados com a cor de neblina de maneiras não intuitivas.</span><span class="sxs-lookup"><span data-stu-id="49d4a-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="49d4a-122">Por exemplo, imagine uma cena na qual há dois objetos visíveis: um para cima o suficiente para ser afetado pela neblina e o outro quase suficiente para não ser afetado.</span><span class="sxs-lookup"><span data-stu-id="49d4a-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="49d4a-123">Se a área de exibição for girada em vigor, os efeitos de neblinas aparentes poderão mudar, mesmo se os objetos forem estáticos.</span><span class="sxs-lookup"><span data-stu-id="49d4a-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="49d4a-124">O diagrama a seguir mostra uma visão superior dessa situação.</span><span class="sxs-lookup"><span data-stu-id="49d4a-124">The following diagram shows a top-down view of such a situation.</span></span>

![diagrama de dois pontos de vista e como eles afetam a neblina para dois objetos](images/artifog.png)

<span data-ttu-id="49d4a-126">A neblina baseada em intervalo é outra maneira mais precisa, para determinar os efeitos de neblina.</span><span class="sxs-lookup"><span data-stu-id="49d4a-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="49d4a-127">Na neblina baseada em intervalo, o Direct3D usa a distância real do ponto de vista para um vértice para seus cálculos de neblina.</span><span class="sxs-lookup"><span data-stu-id="49d4a-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="49d4a-128">O Direct3D aumenta o efeito da neblina à medida que a distância entre os dois pontos aumenta, em vez da profundidade do vértice dentro da cena, evitando assim artefatos rotacionais.</span><span class="sxs-lookup"><span data-stu-id="49d4a-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="49d4a-129">Se o dispositivo atual der suporte à neblina baseada em intervalo, ele definirá o valor de FOGRANGE de D3DPRASTERCAPS \_ no membro RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando você chamar o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="49d4a-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="49d4a-130">Para habilitar a neblina baseada em intervalo, defina o \_ estado de RENDERIZAÇÃO D3DRS RANGEFOGENABLE como **true**.</span><span class="sxs-lookup"><span data-stu-id="49d4a-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="49d4a-131">A neblina baseada em intervalo é calculada pelo Direct3D durante a transformação e a iluminação.</span><span class="sxs-lookup"><span data-stu-id="49d4a-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="49d4a-132">Os aplicativos que não usam o mecanismo de transformação e iluminação do Direct3D também devem executar seus próprios cálculos de neblina de vértice.</span><span class="sxs-lookup"><span data-stu-id="49d4a-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="49d4a-133">Nesse caso, forneça o fator de neblina baseado em intervalo no componente alfa do componente especular para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="49d4a-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="49d4a-134">Usando a neblina de vértice</span><span class="sxs-lookup"><span data-stu-id="49d4a-134">Using Vertex Fog</span></span>

<span data-ttu-id="49d4a-135">Use as etapas a seguir para habilitar a neblina de vértice em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49d4a-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="49d4a-136">Habilite a mesclagem de neblina definindo D3DRS \_ FOGENABLE como **true**.</span><span class="sxs-lookup"><span data-stu-id="49d4a-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="49d4a-137">Defina a cor de neblina no \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="49d4a-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="49d4a-138">Escolha a fórmula de neblina desejada definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGVERTEXMODE como um membro do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="49d4a-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="49d4a-139">Defina os parâmetros de neblina conforme desejado para a fórmula de neblina selecionada nos Estados de renderização.</span><span class="sxs-lookup"><span data-stu-id="49d4a-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="49d4a-140">O exemplo a seguir, escrito em C++, mostra o que essas etapas podem parecer no código.</span><span class="sxs-lookup"><span data-stu-id="49d4a-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="49d4a-141">Alguns parâmetros de neblina são necessários como valores de ponto flutuante, mesmo que o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceite apenas valores DWORD no segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49d4a-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="49d4a-142">Este exemplo fornece com êxito os valores de ponto flutuante para esses métodos sem conversão de dados, convertendo os endereços das variáveis de ponto flutuante como ponteiros DWORD e, em seguida, desreferenciando-os.</span><span class="sxs-lookup"><span data-stu-id="49d4a-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49d4a-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49d4a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49d4a-144">Tipos de neblina</span><span class="sxs-lookup"><span data-stu-id="49d4a-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
