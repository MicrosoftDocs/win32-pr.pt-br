---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 função
description: Desempacotar dados de sombreador \_ \_ SRGB UNORM FORMAT B8G8R8X8 \_ DXGI para um \_ XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 função
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 função HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc5f638d827a7b6ebf3543b3cde212fd56b0ace41ffb69bf4b7f79b56c28dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793852"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>Função D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ para \_ FLOAT3

Desempacotar dados de sombreador \_ \_ SRGB UNORM FORMAT B8G8R8X8 \_ DXGI para um \_ XMFLOAT3.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Os dados de sombreador empacotados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Os dados do sombreador desempacodados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX \_ DXGIFormatConvert.inl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções](format-conversion-functions.md)
</dt> <dt>

[Desempacotar e empacotar formato DXGI \_ para In-Place edição de imagem](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





