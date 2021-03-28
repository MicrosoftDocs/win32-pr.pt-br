---
title: Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
description: Desempacota \_ \_ \_ \_ os dados do sombreador R8G8B8A8 UNORM sRGB no formato dxgi para um XMFLOAT4. | Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e373ccb8035b19da7c44ee05a07dd0351ca8f48d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968573"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ to \_ FLOAT4 function

Desempacota \_ \_ \_ \_ os dados do sombreador R8G8B8A8 UNORM sRGB no formato dxgi para um XMFLOAT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(
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

 

 





