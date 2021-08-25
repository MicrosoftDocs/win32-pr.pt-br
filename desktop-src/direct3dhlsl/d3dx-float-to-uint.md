---
title: D3DX_FLOAT_to_UINT função
description: Converte um valor FLOAT em UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT função HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37665d3630979dee3fad7c109152a852883455f5de40c064faa8f1ea4f0645cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855616"
---
# <a name="d3dx_float_to_uint-function"></a>Função D3DX \_ FLOAT \_ to \_ UINT

Converte um valor FLOAT em UINT.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*\_V* 
</dt> <dd>

O vetor v.

</dd> <dt>

*\_Escala* 
</dt> <dd>

O valor de escala.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor FLOAT convertido

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

 

 





