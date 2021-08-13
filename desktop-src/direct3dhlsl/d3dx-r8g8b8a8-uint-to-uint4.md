---
title: Função D3DX_R8G8B8A8_UINT_to_UINT4
description: Desempacota \_ o formato dxgi \_ R8G8B8A8 \_ dados do sombreador uint para um XMUINT4.
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- Função D3DX_R8G8B8A8_UINT_to_UINT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f97c46400f1ba08f1b9e72b867cb66fda37e7bb4cd3a2b2b871271a6858a4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286561"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a>D3DX \_ R8G8B8A8 \_ uint \_ to \_ UINT4 function

Desempacota \_ o formato dxgi \_ R8G8B8A8 \_ dados do sombreador uint para um XMUINT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*packedInput* 
</dt> <dd>

Os dados do sombreador embalado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 





