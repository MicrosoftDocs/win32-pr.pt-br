---
title: D3DX_UINT2_to_R16G16_UINT função
description: Empacota o XMUINT2 determinado de volta em um UINT DXGI \_ FORMAT \_ R16G16. \_
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- D3DX_UINT2_to_R16G16_UINT função HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31d938f74874748715a0e90e4eace54f222699b61fbb4655238b2ebca8ace7ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986788"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a>Função UINT D3DX \_ UINT2 \_ \_ a R16G16 \_

Empacota o XMUINT2 determinado de volta em um UINT DXGI \_ FORMAT \_ R16G16. \_

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
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

 

 





