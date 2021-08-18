---
title: D3DX_SRGB_to_FLOAT_inexact função
description: Converte um valor SRGB em FLOAT. | D3DX_SRGB_to_FLOAT_inexact função
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact função HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9dd841e022da85d609c203f57288af62a6c99ecc9f56079982308a095285f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515687"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a>Função \_ \_ \_ inexact D3DX SRGB para FLOAT \_

Converte um valor SRGB em FLOAT.

## <a name="syntax"></a>Sintaxe

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Val* 
</dt> <dd>

Valor SRGB a ser convertido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor SRGB convertido.

## <a name="remarks"></a>Comentários

Essa função não tem uma precisão alta o suficiente para dar a resposta exata. A função alternativa [**D3DX \_ SRGB \_ para \_ FLOAT**](d3dx-srgb-to-float.md) usa uma tabela de lookup para dar um SRGB exato para conversão float.

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

 

 





