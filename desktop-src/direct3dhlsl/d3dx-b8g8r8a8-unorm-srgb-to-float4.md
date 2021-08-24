---
title: Função D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
description: Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8A8 UNORM sRGB no formato dxgi para um XMFLOAT4. | Função D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- Função D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620823a572b7eb23f05bdda83866aae982f326dfb70ca6856309abc9d96f05b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516592"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 function

Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8A8 UNORM sRGB no formato dxgi para um XMFLOAT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
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

 

 





