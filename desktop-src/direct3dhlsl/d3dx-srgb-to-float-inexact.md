---
title: Função D3DX_SRGB_to_FLOAT_inexact
description: Converte um valor SRGB em FLOAT. | Função D3DX_SRGB_to_FLOAT_inexact
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- Função D3DX_SRGB_to_FLOAT_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968584"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>D3DX \_ sRGB \_ para \_ flutuar \_ função inexata

Converte um valor SRGB em FLOAT.

## <a name="syntax"></a>Sintaxe

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Val* 
</dt> <dd>

Valor SRGB a ser convertido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de SRGB convertido.

## <a name="remarks"></a>Comentários

Essa função não tem uma precisão alta o suficiente para fornecer a resposta exata. A função alternativa [**D3DX \_ sRGB \_ para \_ flutuar**](d3dx-srgb-to-float.md) usa uma tabela de pesquisa para fornecer uma conversão exata de sRGB para float.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert. inl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções](format-conversion-functions.md)
</dt> <dt>

[Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





