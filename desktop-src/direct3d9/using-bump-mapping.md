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
# <a name="using-bump-mapping-direct3d-9"></a>Usando o mapeamento de relevo (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Detectando suporte para mapeamento de rebatida

Um dispositivo pode executar o mapeamento de relevo se ele der suporte à \_ operação de mesclagem de textura D3DTOP BUMPENVMAP ou D3DTOP \_ BUMPENVMAPLUMINANCE. Use [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) com D3DUSAGE de \_ consulta \_ LEGACYBUMPMAP para ver se há suporte para um formato para o mapeamento de relevo.

Além disso, os aplicativos devem verificar os recursos do dispositivo para certificar-se de que o dispositivo dá suporte a um número apropriado de estágios de mesclagem, geralmente pelo menos três e expõe pelo menos um formato de pixel de mapeamento de relevo.

O exemplo de código a seguir verifica os recursos do dispositivo para detectar o suporte para o mapeamento de relevo no dispositivo atual, usando os critérios especificados.


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



## <a name="creating-a-bump-map-texture"></a>Criando uma textura de mapa de relevo

Você cria uma textura de mapa de relevo como qualquer outra textura. Seu aplicativo verifica o suporte para o mapeamento de rebatida e recupera um formato de pixel válido, conforme discutido em detectando suporte para mapeamento de rebatida.

Depois que a superfície for criada, você poderá carregar cada pixel com os valores Delta apropriados e a luminância, se o formato da superfície incluir luminância. Os valores para cada componente de pixel são descritos nos [formatos de pixel do mapa de relevo (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Configurando parâmetros de mapeamento de relevo

Quando seu aplicativo tiver criado um mapa de relevo e definir o conteúdo de cada pixel, você poderá se preparar para a renderização configurando parâmetros de mapeamento de relevo. Os parâmetros de mapeamento de relevo incluem a definição das texturas necessárias e suas operações de mesclagem, bem como os controles de transformação e luminância para o mapa de relevo.

1.  Defina o mapa de textura base, se usado, o mapa de relevo e as texturas de mapa de ambiente em estágios de mesclagem de textura.
2.  Defina as operações de mesclagem de cor e alfa para cada estágio de textura.
3.  Defina a matriz de transformação mapa de relevo.
4.  Defina a escala de luminância e os valores de deslocamento conforme necessário.

O exemplo de código a seguir define três texturas (o mapa de textura base, o mapa de relevo e um mapa de ambiente especular) para os estágios de mesclagem de textura apropriados.


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



Quando as operações de mesclagem e os argumentos são definidos, o exemplo de código a seguir define a matriz de mapeamento de choque 2x2 para a matriz de identidade definindo os \_ Membros D3DTSS BUMPENVMAPMAT00 e D3DTSS \_ BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) como 1,0. Definir a matriz para a identidade faz com que o sistema use os valores Delta no mapa de rebatidas sem modificações, mas isso não é um requisito.


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



Se você definir a operação de mapeamento de relevo para incluir luminescência (D3DTOP \_ BUMPENVMAPLUMINANCE), deverá definir os controles de luminância. Os controles de luminância configuram como o sistema computa a luminância antes de modulating a cor da textura no próximo estágio. Para obter detalhes, consulte [fórmulas de mapeamento de relevo (Direct3D 9)](bump-mapping-formulas.md).


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



Depois que o aplicativo configura os parâmetros de mapeamento de relevo, ele pode ser renderizado normalmente e os polígonos renderizados recebem efeitos de mapeamento de relevo.

Observe que o exemplo anterior mostra parâmetros definidos para mapeamento de ambiente especular. Ao executar o mapeamento de luz difusa, os aplicativos definem a operação de mesclagem de textura para o último estágio para D3DTOP \_ modular. Para obter mais informações, consulte [mapas de luz difusa (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mapeamento de relevo](bump-mapping.md)
</dt> </dl>

 

 
