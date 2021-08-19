---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB função
description: Empacota o XMFLOAT4 determinado de volta em um FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB.
ms.assetid: 66580428-6f06-4e0c-bf89-01f03c7304ad
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB função HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e930935e34ff1aa76c99949949e12b5c57254eeea59262cf2ec7828482965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516274"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm_srgb-function"></a>Função SRGB D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_

Empacota o XMFLOAT4 determinado de volta em um FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Os dados do sombreador a ser empacotado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Os dados de sombreador empacotados.

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

 

 





