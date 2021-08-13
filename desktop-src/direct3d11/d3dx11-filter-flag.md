---
title: D3DX11_FILTER_FLAG enumeração (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Sinalizadores de filtragem de textura.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- D3DX11_FILTER_FLAG enumeração Direct3D 11
- LPD3DX11_FILTER_FLAG ponteiro de enumeração Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02ddbf1785d1032ab28a990d022950b2f28acc4b032ecdc9a72d5704665c03b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536997"
---
# <a name="d3dx11_filter_flag-enumeration"></a>Enumeração D3DX11 \_ FILTER \_ FLAG

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Sinalizadores de filtragem de textura.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11 \_ FILTER \_ NONE**
</dt> <dd>

Nenhuma colocação em escala ou filtragem ocorrerá. Os pixels fora dos limites da imagem de origem são presumidos como preto transparente.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**PONTO DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Cada pixel de destino é calculado pela amostragem do pixel mais próximo da imagem de origem.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ FILTER \_ LINEAR**
</dt> <dd>

Cada pixel de destino é calculado pela amostragem dos quatro pixels mais próximos da imagem de origem. Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**TRIÂNGULO DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Cada pixel na imagem de origem contribui igualmente para a imagem de destino. Esse é o mais lento dos filtros.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**CAIXA DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Cada pixel é calculado pela média de uma caixa de 2x2(x2) de pixels da imagem de origem. Esse filtro funciona somente quando as dimensões do destino são metade das da origem, como é o caso com mipmaps.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ FILTER \_ MIRROR \_ U**
</dt> <dd>

Pixels fora da borda da textura no eixo u devem ser espelhados, não empacotados.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11 \_ FILTER \_ MIRROR \_ V**
</dt> <dd>

Os pixels da borda da textura no eixo v devem ser espelhados, não empacotados.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11 \_ FILTER \_ MIRROR \_ W**
</dt> <dd>

Pixels fora da borda da textura no eixo w devem ser espelhados, não empacotados.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**ESPELHO DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Especificar esse sinalizador é o mesmo que especificar os sinalizadores D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V e \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**DITHER DE FILTRO D3DX11 \_ \_**
</dt> <dd>

A imagem resultante deve ser dithered usando um algoritmo dither ordenado 4x4. Isso acontece ao converter de um formato para outro.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**DIFUSÃO DITHER DE FILTRO D3DX11 \_ \_ \_**
</dt> <dd>

Faça dithering difuso na imagem ao alterar de um formato para outro.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ FILTER \_ SRGB \_ IN**
</dt> <dd>

Os dados de entrada estão no espaço de cores RGB (sRGB) padrão. Consulte Observações.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ FILTER \_ SRGB \_ OUT**
</dt> <dd>

Os dados de saída estão no espaço de cores RGB (sRGB) padrão. Consulte Observações.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**SRGB DE FILTRO D3DX11 \_ \_**
</dt> <dd>

O mesmo que especificar SRGB DE FILTRO D3DX \_ \_ EM FILTRO \_ \| D3DX \_ \_ SRGB \_ OUT. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

D3DX11 executa automaticamente a correção gama (para converter dados de cores do espaço RGB para o espaço RGB padrão) ao carregar dados de textura. Isso é feito automaticamente, por exemplo, quando os dados RGB são carregados de um arquivo .png em uma textura sRGB. Use os sinalizadores de filtro SRGB para indicar se os dados não precisam ser convertidos em espaço sRGB.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





