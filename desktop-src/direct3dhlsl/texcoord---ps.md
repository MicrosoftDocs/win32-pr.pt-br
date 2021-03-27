---
title: texcoord-PS
description: Interpreta dados de coordenadas de textura (UVW1) como dados de cor (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641289"
---
# <a name="texcoord---ps"></a>texcoord-PS

Interpreta dados de coordenadas de textura (UVW1) como dados de cor (RGBA).

## <a name="syntax"></a>Syntax



| texcoord DST |
|--------------|



 

onde

-   DST é o registro de destino.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução interpreta o conjunto de coordenadas de textura (UVW1) correspondente ao número de registro de destino como dados de cor (RGBA). Se o conjunto de coordenadas de textura contiver menos de três componentes, os componentes ausentes serão definidos como 0. O quarto componente é sempre definido como 1. Todos os valores são clampeddos entre 0 e 1.

A vantagem do texcoord é que ele fornece uma maneira de passar dados de vértice interpolados a alta precisão diretamente no sombreador de pixel. No entanto, quando os dados são gravados no registro de destino, alguma precisão será perdida, dependendo do número de bits usados pelo hardware para os registros.

Nenhuma textura é amostrada por essa instrução. Somente as coordenadas de textura definidas neste estágio de textura são relevantes.

Todos os dados de textura (como posição, normal e direção da fonte de luz) podem ser mapeados por um sombreador de vértice em uma coordenada de textura. Isso é feito associando uma textura a um registro de textura usando [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) e especificando como a amostragem de textura é feita usando [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Se o pipeline de função fixa for usado, não se esqueça de fornecer o \_ sinalizador TSS TEXCOORDINDEX.

Essa instrução é usada da seguinte maneira:


```
texcoord tn
```



Um TN ( [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) ) contém quatro valores de cor (RGBA). Os dados também podem ser considerados como dados de vetor (xyzw). texcoord recuperará três desses valores (XYZ) do conjunto de coordenadas de textura x, e o quarto componente (w) é definido como 1. O endereço de textura é copiado do conjunto de coordenadas de textura n. O resultado é clamped entre 0 e 1.

Este exemplo é apenas uma ilustração. O código C que acompanha o sombreador não foi otimizado para desempenho.

Aqui está um sombreador de exemplo usando texcoord.


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



A saída renderizada do sombreador de pixel é mostrada na ilustração a seguir. Os valores de coordenadas (u, v, w, 1) são mapeados para os canais (RGB). O canal alfa é definido como 1. Nos cantos da ilustração, a coordenada (0, 0, 0, 1) é interpretada como preta; (1, 0, 0, 1) é vermelho; (0, 1, 0, 1) é verde; e (1, 1, 0, 1) contém verde e vermelho, produzindo amarelo.

![ilustração da saída renderizada do sombreador de pixel de exemplo](images/pstexcoord.jpg)

O código adicional é necessário para usar este sombreador e um cenário de exemplo é mostrado abaixo.


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 