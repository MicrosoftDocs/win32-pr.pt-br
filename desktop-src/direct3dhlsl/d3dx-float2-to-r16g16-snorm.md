---
title: D3DX_FLOAT2_to_R16G16_SNORM função
description: Empacota o XMFLOAT2 determinado de volta em um SNORM DXGI \_ FORMAT \_ R16G16. \_
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM função HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9ad7d4ff95113d4d684cba7cc348c2d60a536e12171afa6ad421724a668e63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024996"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a>Função SNORM D3DX \_ FLOAT2 \_ a \_ R16G16 \_

Empacota o XMFLOAT2 determinado de volta em um SNORM DXGI \_ FORMAT \_ R16G16. \_

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*unpackedInput* 
</dt> <dd>

Os dados do sombreador desempacodados.

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

 

 





