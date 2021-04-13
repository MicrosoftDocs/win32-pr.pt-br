---
description: Usando o mapeamento de relevo (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Usando o mapeamento de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456863"
---
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="4a5b5-103">Usando o mapeamento de relevo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4a5b5-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="4a5b5-104">Detectando suporte para mapeamento de rebatida</span><span class="sxs-lookup"><span data-stu-id="4a5b5-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="4a5b5-105">Um dispositivo pode executar o mapeamento de relevo se ele der suporte à \_ operação de mesclagem de textura D3DTOP BUMPENVMAP ou D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="4a5b5-106">Use [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com D3DUSAGE de \_ consulta \_ LEGACYBUMPMAP para ver se há suporte para um formato para o mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="4a5b5-107">Além disso, os aplicativos devem verificar os recursos do dispositivo para certificar-se de que o dispositivo dá suporte a um número apropriado de estágios de mesclagem, geralmente pelo menos três e expõe pelo menos um formato de pixel de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="4a5b5-108">O exemplo de código a seguir verifica os recursos do dispositivo para detectar o suporte para o mapeamento de relevo no dispositivo atual, usando os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="4a5b5-109">Criando uma textura de mapa de relevo</span><span class="sxs-lookup"><span data-stu-id="4a5b5-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="4a5b5-110">Você cria uma textura de mapa de relevo como qualquer outra textura.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="4a5b5-111">Seu aplicativo verifica o suporte para o mapeamento de rebatida e recupera um formato de pixel válido, conforme discutido em detectando suporte para mapeamento de rebatida.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="4a5b5-112">Depois que a superfície for criada, você poderá carregar cada pixel com os valores Delta apropriados e a luminância, se o formato da superfície incluir luminância.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="4a5b5-113">Os valores para cada componente de pixel são descritos nos [formatos de pixel do mapa de relevo (Direct3D 9)](bump-map-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="4a5b5-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="4a5b5-114">Configurando parâmetros de mapeamento de relevo</span><span class="sxs-lookup"><span data-stu-id="4a5b5-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="4a5b5-115">Quando seu aplicativo tiver criado um mapa de relevo e definir o conteúdo de cada pixel, você poderá se preparar para a renderização configurando parâmetros de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="4a5b5-116">Os parâmetros de mapeamento de relevo incluem a definição das texturas necessárias e suas operações de mesclagem, bem como os controles de transformação e luminância para o mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="4a5b5-117">Defina o mapa de textura base, se usado, o mapa de relevo e as texturas de mapa de ambiente em estágios de mesclagem de textura.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="4a5b5-118">Defina as operações de mesclagem de cor e alfa para cada estágio de textura.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="4a5b5-119">Defina a matriz de transformação mapa de relevo.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="4a5b5-120">Defina a escala de luminância e os valores de deslocamento conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="4a5b5-121">O exemplo de código a seguir define três texturas (o mapa de textura base, o mapa de relevo e um mapa de ambiente especular) para os estágios de mesclagem de textura apropriados.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="4a5b5-122">Depois de definir as texturas para seus estágios de mesclagem, o exemplo de código a seguir prepara as operações de mesclagem e os argumentos para cada estágio.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



<span data-ttu-id="4a5b5-123">Quando as operações de mesclagem e os argumentos são definidos, o exemplo de código a seguir define a matriz de mapeamento de choque 2x2 para a matriz de identidade definindo os \_ Membros D3DTSS BUMPENVMAPMAT00 e D3DTSS \_ BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) como 1,0.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="4a5b5-124">Definir a matriz para a identidade faz com que o sistema use os valores Delta no mapa de rebatidas sem modificações, mas isso não é um requisito.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



<span data-ttu-id="4a5b5-125">Se você definir a operação de mapeamento de relevo para incluir luminescência (D3DTOP \_ BUMPENVMAPLUMINANCE), deverá definir os controles de luminância.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="4a5b5-126">Os controles de luminância configuram como o sistema computa a luminância antes de modulating a cor da textura no próximo estágio.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="4a5b5-127">Para obter detalhes, consulte [fórmulas de mapeamento de relevo (Direct3D 9)](bump-mapping-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="4a5b5-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



<span data-ttu-id="4a5b5-128">Depois que o aplicativo configura os parâmetros de mapeamento de relevo, ele pode ser renderizado normalmente e os polígonos renderizados recebem efeitos de mapeamento de relevo.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="4a5b5-129">Observe que o exemplo anterior mostra parâmetros definidos para mapeamento de ambiente especular.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="4a5b5-130">Ao executar o mapeamento de luz difusa, os aplicativos definem a operação de mesclagem de textura para o último estágio para D3DTOP \_ modular.</span><span class="sxs-lookup"><span data-stu-id="4a5b5-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="4a5b5-131">Para obter mais informações, consulte [mapas de luz difusa (Direct3D 9)](diffuse-light-maps.md).</span><span class="sxs-lookup"><span data-stu-id="4a5b5-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a5b5-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a5b5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a5b5-133">Mapeamento de relevo</span><span class="sxs-lookup"><span data-stu-id="4a5b5-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 
