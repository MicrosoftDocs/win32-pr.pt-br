---
title: Função D3DX_FLOAT4_to_R8G8B8A8_UNORM
description: Desempacota \_ o formato dxgi \_ R8G8B8A8 \_ UNORM dados do sombreador para um XMFLOAT4. | Função D3DX_FLOAT4_to_R8G8B8A8_UNORM
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- Função D3DX_FLOAT4_to_R8G8B8A8_UNORM HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664097"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a>D3DX \_ FLOAT4 \_ \_ R8G8B8A8 \_ UNORM function

Desempacota \_ o formato dxgi \_ R8G8B8A8 \_ UNORM dados do sombreador para um XMFLOAT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
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

 

 





