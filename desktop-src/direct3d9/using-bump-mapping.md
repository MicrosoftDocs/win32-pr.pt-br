---
description: Usando mapeamento de aumento (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Usando mapeamento de aumento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195a99ffaa29d416aea93c5599f1fb461cd78a9961bd9c69f3f02ae3e8fe4719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025826"
---
# <a name="using-bump-mapping-direct3d-9"></a>Usando mapeamento de aumento (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Detectando suporte para mapeamento de aumento

Um dispositivo poderá executar o mapeamento de elevação se ele for compatível com a operação de mesclagem de \_ texturaS BUMPENVMAP ou D3DTOP \_ BUMPENVMAPLUMINANCE. Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com D3DUSAGE \_ QUERY LEGACYBUMPMAP para ver se há suporte para um formato para mapeamento \_ de aumento.

Além disso, os aplicativos devem verificar as funcionalidades do dispositivo para garantir que o dispositivo dá suporte a um número apropriado de estágios de mesclagem, geralmente três, e expõe pelo menos um formato de pixel de mapeamento de aumento.

O exemplo de código a seguir verifica as funcionalidades do dispositivo para detectar suporte para mapeamento de aumento no dispositivo atual, usando os critérios determinados.


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



## <a name="creating-a-bump-map-texture"></a>Criando uma textura do mapa de elevações

Você cria uma textura do mapa de aumento como qualquer outra textura. Seu aplicativo verifica o suporte para mapeamento de aumento e recupera um formato de pixel válido, conforme discutido em Detectando suporte para mapeamento de aumento.

Depois que a superfície for criada, você poderá carregar cada pixel com os valores delta apropriados e luminância, se o formato da superfície incluir luminância. Os valores para cada componente de pixel são descritos em Formatos de Pixel do Mapa [de Aumento (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Configurando parâmetros de mapeamento de aumento

Quando seu aplicativo tiver criado um mapa de elevações e definido o conteúdo de cada pixel, você poderá se preparar para renderização configurando parâmetros de mapeamento de aumento. Os parâmetros de mapeamento de aumento incluem a definição das texturas necessárias e suas operações de mesclagem, bem como os controles de transformação e luminância para o mapa de aumento em si.

1.  De definir o mapa de textura base, se usado, o mapa de elevações e as texturas do mapa de ambiente em estágios de mesclagem de textura.
2.  Definir as operações de combinação de cores e alfa para cada estágio de textura.
3.  Definir a matriz de transformação do mapa de aumento.
4.  De definir os valores de escala e deslocamento de luminância conforme necessário.

O exemplo de código a seguir define três texturas (o mapa de textura base, o mapa de elevações e um mapa de ambiente especular) para os estágios apropriados de mesclagem de textura.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Depois de definir as texturas para seus estágios de mesclagem, o exemplo de código a seguir prepara as operações de mesclagem e os argumentos para cada estágio.


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



Quando as operações de mesclagem e os argumentos são definidos, o exemplo de código a seguir define a matriz de mapeamento de elevação 2x2 para a matriz de identidade definindo os membros D3DTSS \_ BUMPENVMAPMAT00 e D3DTSS \_ BUMPENVMAPMAT11 [**de D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) como 1.0. Definir a matriz como a identidade faz com que o sistema use os valores delta no mapa de aumento sem modificações, mas isso não é um requisito.


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



Se você definir a operação de mapeamento de aumento para incluir luminância (D3DTOP BUMPENVMAPLUMINANCE), deverá definir os controles \_ de luminância. Os controles de luminância configuram como o sistema calcula a luminância antes de modular a cor da textura no próximo estágio. Para obter detalhes, consulte [Fórmulas de mapeamento de aumento (Direct3D 9)](bump-mapping-formulas.md).


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



Depois que o aplicativo configurar parâmetros de mapeamento de aumento, ele poderá renderizar normalmente e os polígonos renderizados receberão efeitos de mapeamento de aumento.

Observe que o exemplo anterior mostra parâmetros definidos para mapeamento de ambiente especular. Ao executar o mapeamento de luz difuso, os aplicativos configuram a operação de mesclagem de textura para o último estágio como D3DTOP \_ MODULARTE. Para obter mais informações, consulte [Luz difusa Mapas (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de aumento](bump-mapping.md)
</dt> </dl>

 

 
