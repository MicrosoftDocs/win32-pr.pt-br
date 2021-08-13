---
title: D3DX_UINT4_to_R10G10B10A2_UINT função
description: Empacota o XMINT4 determinado de volta em um formato DXGI \_ \_ R10G10B10A2 \_ UINT.
ms.assetid: fe10c62e-2d84-4f6b-886b-247ee344f6c7
keywords:
- D3DX_UINT4_to_R10G10B10A2_UINT função HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R10G10B10A2_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33420ca720ce2e605a378340926f86651a39e6e7f4c787c83d5e4ba2b15a8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286471"
---
# <a name="d3dx_uint4_to_r10g10b10a2_uint-function"></a>Função \_ UINT4 D3DX \_ para \_ R10G10B10A2 \_

Empacota o XMINT4 determinado de volta em um formato DXGI \_ \_ R10G10B10A2 \_ UINT.

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_UINT4_to_R10G10B10A2_UINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Os dados do sombreador a ser empacotado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 





