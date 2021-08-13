---
title: D3DX_R10G10B10A2_UNORM_to_FLOAT4 função
description: Desempacotar dados do sombreador DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM para um XMFLOAT4.
ms.assetid: 36efd611-1450-421a-a34f-fd874589de2a
keywords:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4 função HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3814bb8ed3bdcc1795a6452e88047c00f5d84cc6dbbfb835f4e4d0390df6c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286616"
---
# <a name="d3dx_r10g10b10a2_unorm_to_float4-function"></a>Função D3DX \_ R10G10B10A2 \_ UNORM \_ para \_ FLOAT4

Desempacotar dados do sombreador DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM para um XMFLOAT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Os dados de sombreador empacotados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 





