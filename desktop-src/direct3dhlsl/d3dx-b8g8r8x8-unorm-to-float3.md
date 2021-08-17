---
title: Função D3DX_B8G8R8X8_UNORM_to_FLOAT3
description: Desempacota \_ o formato dxgi \_ B8G8R8X8 \_ UNORM dados do sombreador para um XMFLOAT3.
ms.assetid: 0987d71a-89a4-4751-9f32-08e2490204d2
keywords:
- Função D3DX_B8G8R8X8_UNORM_to_FLOAT3 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac787be8dc856c9f4748b7d2934000c5e4271141284dbb36e45cc1309f111a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793808"
---
# <a name="d3dx_b8g8r8x8_unorm_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ \_ FLOAT3 function

Desempacota \_ o formato dxgi \_ B8G8R8X8 \_ UNORM dados do sombreador para um XMFLOAT3.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Os dados do sombreador embalado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





