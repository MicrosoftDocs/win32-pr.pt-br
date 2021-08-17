---
title: Função D3DX_R16G16_UNORM_to_FLOAT2
description: Desempacota \_ o formato dxgi \_ R16G16 \_ UNORM dados do sombreador para um XMFLOAT2.
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- Função D3DX_R16G16_UNORM_to_FLOAT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aab22773a643ad7ef233871c673b92a60aeed722b78be15e4bd0918ed836fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727368"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a>D3DX \_ R16G16 \_ UNORM \_ \_ FLOAT2 function

Desempacota \_ o formato dxgi \_ R16G16 \_ UNORM dados do sombreador para um XMFLOAT2.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
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

 

 





