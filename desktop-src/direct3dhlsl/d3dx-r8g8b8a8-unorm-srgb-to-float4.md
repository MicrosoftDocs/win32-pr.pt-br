---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 função
description: Desempacotar dados de sombreador \_ \_ SRGB UNORM FORMAT R8G8B8A8 DXGI para \_ \_ um XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 função
ms.assetid: 67ad1768-aeb9-4c01-ae3e-0cd79476a459
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4 função HLSL
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
ms.openlocfilehash: bf2775c73d60317aa1e0892f16903ddf3270c99def0fe0a55b750079a2c7c3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986846"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4-function"></a>Função D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ para \_ FLOAT4

Desempacotar dados de sombreador \_ \_ SRGB UNORM FORMAT R8G8B8A8 DXGI para \_ \_ um XMFLOAT4.

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

 

 





