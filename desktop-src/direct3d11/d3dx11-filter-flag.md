---
title: Enumeração de D3DX11_FILTER_FLAG (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Sinalizadores de filtragem de textura.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Enumeração D3DX11_FILTER_FLAG Direct3D 11
- Ponteiro de enumeração LPD3DX11_FILTER_FLAG Direct3D 11
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
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968697"
---
# <a name="d3dx11_filter_flag-enumeration"></a>Enumeração de sinalizador de \_ filtro D3DX11 \_

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Sinalizadores de filtragem de textura.

## <a name="syntax"></a>Syntax


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

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**Filtro de D3DX11 \_ \_ nenhum**
</dt> <dd>

Nenhum dimensionamento ou filtragem ocorrerá. Os pixels fora dos limites da imagem de origem são considerados pretos transparentes.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Ponto de filtro D3DX11 \_**
</dt> <dd>

Cada pixel de destino é computado por amostragem do pixel mais próximo da imagem de origem.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ filtro \_ linear**
</dt> <dd>

Cada pixel de destino é computado por amostragem dos quatro pixels mais próximos da imagem de origem. Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triângulo de filtro D3DX11 \_**
</dt> <dd>

Cada pixel na imagem de origem contribui igualmente para a imagem de destino. Esse é o mais lento dos filtros.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Caixa de filtro D3DX11 \_**
</dt> <dd>

Cada pixel é calculado pela média de uma caixa de pixels 2x2 (x2) da imagem de origem. Esse filtro funciona somente quando as dimensões do destino são metades da origem, como é o caso com mipmaps.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**\_Espelho do filtro D3DX11 \_ \_ U**
</dt> <dd>

Os pixels da borda da textura no eixo u devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**Espelho de filtro do D3DX11 \_ \_ \_ V**
</dt> <dd>

Os pixels da borda da textura no eixo v devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_Espelho de filtro D3DX11 \_ \_ W**
</dt> <dd>

Os pixels da borda da textura no eixo w devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Espelho de filtro D3DX11 \_**
</dt> <dd>

A especificação desse sinalizador é a mesma que especificar o D3DX do espelho do filtro do D3DX filtro do \_ \_ espelho V e do filtro do D3DX para \_ \_ \_ \_ \_ \_ espelhar os \_ sinalizadores.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Pontilhamento de filtro D3DX11 \_**
</dt> <dd>

A imagem resultante deve ser dificada usando um algoritmo de pontilhamento 4x4 ordenado. Isso acontece ao converter de um formato para outro.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_Difusão de \_ pontilhamento de filtro D3DX11 \_**
</dt> <dd>

Faça o pontilhado difuso na imagem ao alterar de um formato para outro.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ Filtrar \_ sRGB \_ em**
</dt> <dd>

Os dados de entrada estão no espaço de cores RGB padrão (sRGB). Consulte Observações.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtro \_ sRGB \_ out**
</dt> <dd>

Os dados de saída estão no espaço de cores RGB padrão (sRGB). Consulte Observações.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ filtro \_ sRGB**
</dt> <dd>

O mesmo que especificar D3DX \_ Filter \_ sRGB \_ no \| D3DX \_ Filter \_ sRGB \_ out. Consulte Observações.

</dd> </dl>

## <a name="remarks"></a>Comentários

O D3DX11 executa automaticamente a correção de gama (para converter dados de cores de espaço RGB em espaço RGB padrão) ao carregar dados de textura. Isso é feito automaticamente por instância quando dados RGB são carregados de um arquivo. png em uma textura sRGB. Use os sinalizadores de filtro SRGB para indicar se os dados não precisam ser convertidos em espaço sRGB.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





