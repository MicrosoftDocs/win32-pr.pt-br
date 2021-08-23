---
title: Função D3DX_FLOAT2_to_R16G16_FLOAT
description: Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ float.
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- Função D3DX_FLOAT2_to_R16G16_FLOAT HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f96d9c2652966ef4b35f4c07ec13d1ea5b6f92af641c2e86a1bf4e0b12ca4487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516602"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a>D3DX \_ FLOAT2 \_ to \_ R16G16 \_ float function

Compacta o XMFLOAT2 fornecido de volta em um \_ formato dxgi \_ R16G16 \_ float.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Os dados do sombreador desempacotado.

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

 

 





