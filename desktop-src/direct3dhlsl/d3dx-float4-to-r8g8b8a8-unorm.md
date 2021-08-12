---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM função
description: Desempacotar dados do sombreador UNORM DXGI \_ FORMAT \_ R8G8B8A8 \_ para um XMFLOAT4. | D3DX_FLOAT4_to_R8G8B8A8_UNORM função
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM função HLSL
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
ms.openlocfilehash: b21f753c2f08294c2f82bdbfc12bfad5de618d89817bca279fa4b7d3d4578c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286626"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a>Função UNORM D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_

Desempacotar dados do sombreador UNORM DXGI \_ FORMAT \_ R8G8B8A8 \_ para um XMFLOAT4.

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

 

 





