---
title: Função D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
description: Compacta o XMFLOAT4 fornecido em um \_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB uint.
ms.assetid: 2fc36f19-44ce-43ba-9d9f-e8061f94a207
keywords:
- Função D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6661ea7bce5f5a10fec8c3d96bf178fc4e169ba53d013143b89c8114de71cc60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286832"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm_srgb-function"></a>D3DX \_ FLOAT4 \_ na \_ \_ função B8G8R8A8 UNORM \_ sRGB

Compacta o XMFLOAT4 fornecido em um \_ formato dxgi \_ B8G8R8A8 \_ UNORM \_ sRGB uint.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
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

 

 





