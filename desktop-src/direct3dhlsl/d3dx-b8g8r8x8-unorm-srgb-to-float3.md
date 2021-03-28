---
title: Função D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
description: Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8X8 UNORM sRGB no formato dxgi para um XMFLOAT3. | Função D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- Função D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 HLSL
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
ms.openlocfilehash: 277f10bc574e03a7bd608a333cba65f95a3e0b43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989270"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a>D3DX \_ B8G8R8X8 \_ UNORM \_ sRGB \_ to \_ FLOAT3 function

Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8X8 UNORM sRGB no formato dxgi para um XMFLOAT3.

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

 

 





