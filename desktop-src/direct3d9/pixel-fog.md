---
description: A neblina de pixels obtém seu nome do fato de que ele é calculado por pixel no driver do dispositivo.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Sombra de pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825489"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="1dec2-103">Sombra de pixel (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1dec2-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="1dec2-104">A neblina de pixels obtém seu nome do fato de que ele é calculado por pixel no driver do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dec2-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="1dec2-105">Isso é diferente da sombra do vértice, que é computada pelo pipeline durante os cálculos de transformação e iluminação.</span><span class="sxs-lookup"><span data-stu-id="1dec2-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="1dec2-106">A neblina de pixel às vezes é chamada de neblina de tabela porque alguns drivers usam uma tabela de pesquisa precalculada para determinar o fator de neblina, usando a profundidade de cada pixel a ser aplicada em cálculos de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="1dec2-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="1dec2-107">Ele pode ser aplicado usando qualquer fórmula de neblina identificada por membros do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="1dec2-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="1dec2-108">As implementações dessas fórmulas são específicas do driver.</span><span class="sxs-lookup"><span data-stu-id="1dec2-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="1dec2-109">Se um driver não oferecer suporte a uma fórmula de neblina complexa, ele deverá degradar uma fórmula menos complexa.</span><span class="sxs-lookup"><span data-stu-id="1dec2-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="1dec2-110">Eye-Relative vs. profundidade baseada em Z</span><span class="sxs-lookup"><span data-stu-id="1dec2-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="1dec2-111">Para aliviar os artefatos gráficos relacionados à neblina causados por distribuição desigual de valores z em um buffer de profundidade, a maioria dos dispositivos de hardware usa profundidade relativa aos olhos em vez de valores de profundidade baseados em z para sombra de pixel.</span><span class="sxs-lookup"><span data-stu-id="1dec2-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="1dec2-112">A profundidade relativa aos olhos é essencialmente o elemento w de um conjunto de coordenadas homogêneos.</span><span class="sxs-lookup"><span data-stu-id="1dec2-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="1dec2-113">O Microsoft Direct3D usa o recíproco do elemento RHW de uma coordenada de espaço de dispositivo definida para reproduzir o verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="1dec2-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="1dec2-114">Se um dispositivo oferecer suporte à neblina de olho, ele definirá o sinalizador **D3DPRASTERCAPS \_ WFOG** no membro RasterCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando você chamar o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="1dec2-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="1dec2-115">Com exceção do rasterizador de referência, os dispositivos de software sempre usam z para calcular os efeitos de neblina de pixel.</span><span class="sxs-lookup"><span data-stu-id="1dec2-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="1dec2-116">Quando a neblina relativa a olho é suportada, o sistema usa automaticamente a profundidade relativa ao olho em vez da profundidade baseada em z se a matriz de projeção fornecida produza valores z no espaço de mundo equivalente aos valores w no espaço do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1dec2-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="1dec2-117">Você define a matriz de projeção chamando o método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) , usando o \_ valor de projeção D3DTS e passando uma estrutura [**D3DMATRIX**](d3dmatrix.md) que representa a matriz desejada.</span><span class="sxs-lookup"><span data-stu-id="1dec2-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="1dec2-118">Se a matriz de projeção não estiver em conformidade com esse requisito, os efeitos de neblina não serão aplicados corretamente.</span><span class="sxs-lookup"><span data-stu-id="1dec2-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="1dec2-119">Para obter detalhes sobre como produzir uma matriz compatível, consulte [transformação de projeção (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="1dec2-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="1dec2-120">Direct3D usa matriz de projeção atual definida em seus cálculos de profundidade com base em w.</span><span class="sxs-lookup"><span data-stu-id="1dec2-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="1dec2-121">Como resultado, um aplicativo deve definir uma matriz de projeção compatível para receber os recursos baseados em w, mesmo que não use o pipeline de transformação do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1dec2-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="1dec2-122">O Direct3D verifica a quarta coluna da matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="1dec2-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="1dec2-123">Se os coeficientes forem \[ 0, 0, 0, 1 \] (para uma projeção afim), o sistema usará valores de profundidade baseados em z para neblina.</span><span class="sxs-lookup"><span data-stu-id="1dec2-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="1dec2-124">Nesse caso, você também deve especificar as distâncias inicial e final para efeitos de neblina linear no espaço do dispositivo, que varia de 0,0 no ponto mais próximo para o usuário e 1,0 no ponto mais distante.</span><span class="sxs-lookup"><span data-stu-id="1dec2-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="1dec2-125">Usando a neblina de pixel</span><span class="sxs-lookup"><span data-stu-id="1dec2-125">Using Pixel Fog</span></span>

<span data-ttu-id="1dec2-126">Use as etapas a seguir para habilitar a neblina de pixel em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1dec2-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="1dec2-127">Habilite a mesclagem de neblina definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGENABLE como **true**.</span><span class="sxs-lookup"><span data-stu-id="1dec2-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="1dec2-128">Defina a cor de neblina desejada no \_ estado de RENDERIZAÇÃO D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="1dec2-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="1dec2-129">Escolha a fórmula de neblina a ser usada definindo o \_ estado de RENDERIZAÇÃO D3DRS FOGTABLEMODE para o membro correspondente do tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="1dec2-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="1dec2-130">Defina os parâmetros de neblina conforme desejado para o modo de neblina selecionado nos Estados de renderização associados.</span><span class="sxs-lookup"><span data-stu-id="1dec2-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="1dec2-131">Isso inclui as distâncias inicial e final para a neblina linear e densidade de neblina para o modo de neblina exponencial.</span><span class="sxs-lookup"><span data-stu-id="1dec2-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="1dec2-132">O exemplo a seguir mostra o que essas etapas podem parecer no código.</span><span class="sxs-lookup"><span data-stu-id="1dec2-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="1dec2-133">Alguns parâmetros de neblina são necessários como valores de ponto flutuante, mesmo que o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) aceite somente valores DWORD no segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1dec2-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="1dec2-134">O exemplo anterior fornece os valores de ponto flutuante para **IDirect3DDevice9:: Setrenderingstate** sem conversão de dados, convertendo os endereços das variáveis de ponto flutuante como ponteiros DWORD e, em seguida, desfazendo a referência a eles.</span><span class="sxs-lookup"><span data-stu-id="1dec2-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dec2-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dec2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dec2-136">Tipos de neblina</span><span class="sxs-lookup"><span data-stu-id="1dec2-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
