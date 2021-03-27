---
title: Função D3DX_FLOAT2_to_R16G16_SNORM
description: Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ SNORM.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- Função D3DX_FLOAT2_to_R16G16_SNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930628"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>D3DX \_ FLOAT2 \_ \_ R16G16 \_ SNORM function

Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ SNORM.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Os dados do sombreador desempacotado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Os dados do sombreador embalado.

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

 

 





