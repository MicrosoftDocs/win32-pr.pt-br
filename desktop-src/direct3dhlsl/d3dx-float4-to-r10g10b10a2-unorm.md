---
title: Função D3DX_FLOAT4_to_R10G10B10A2_UNORM
description: Compacta o XMFLOAT4 fornecido de volta em um \_ formato dxgi \_ R10G10B10A2 \_ UNORM.
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- Função D3DX_FLOAT4_to_R10G10B10A2_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3303a419ffd5f53364aa509557832307f9014b1a37767c513b8b8c18900a687f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516364"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a>D3DX \_ FLOAT4 \_ \_ R10G10B10A2 \_ UNORM function

Compacta o XMFLOAT4 fornecido de volta em um \_ formato dxgi \_ R10G10B10A2 \_ UNORM.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Os dados do sombreador a serem empacotados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





