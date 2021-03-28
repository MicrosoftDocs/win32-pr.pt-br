---
title: Função D3DX_R16G16_SNORM_to_FLOAT2
description: Desempacota \_ o formato dxgi \_ R16G16 \_ SNORM dados do sombreador para um XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- Função D3DX_R16G16_SNORM_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3d45f486d2c44e2cbe319e920ab4bdec764fd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989304"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a>D3DX \_ R16G16 \_ SNORM \_ \_ FLOAT2 function

Desempacota \_ o formato dxgi \_ R16G16 \_ SNORM dados do sombreador para um XMFLOAT2.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Os dados do sombreador embalado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Os dados do sombreador desempacotado.

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

 

 





