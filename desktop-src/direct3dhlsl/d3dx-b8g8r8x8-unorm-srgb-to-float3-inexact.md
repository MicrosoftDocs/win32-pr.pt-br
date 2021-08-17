---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact função
description: Desempacotar dados de sombreador \_ \_ SRGB UNORM FORMAT B8G8R8X8 \_ DXGI para um \_ XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact função
ms.assetid: caa64f89-7b9e-4bc0-82dc-31edfd31d495
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact função HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f696381402d8ad42c92310029631e66b457e3b211d22d8f9de3dd98c1f1312ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986866"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3_inexact-function"></a>Função \_ inexact D3DX B8G8R8X8 \_ UNORM \_ SRGB \_ para \_ FLOAT3 \_

Desempacotar dados de sombreador \_ \_ SRGB UNORM FORMAT B8G8R8X8 \_ DXGI para um \_ XMFLOAT3.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(
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

## <a name="remarks"></a>Comentários

Essa função usa instruções de sombreador que não têm precisão alta o suficiente para dar a resposta exata. A função alternativa [**D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ to \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md) usa uma tabela de lookup armazenada no sombreador para dar um SRGB exato para conversão float.

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

 

 





