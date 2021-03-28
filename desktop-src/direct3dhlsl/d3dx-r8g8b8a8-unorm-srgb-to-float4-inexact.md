---
title: Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Desempacota \_ \_ \_ \_ os dados do sombreador R8G8B8A8 UNORM sRGB no formato dxgi para um XMFLOAT4. | Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- Função D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d3d4a9d47eb520d151fe2e3388e99f401fc0a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930640"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ função inexata

Desempacota \_ \_ \_ \_ os dados do sombreador R8G8B8A8 UNORM sRGB no formato dxgi para um XMFLOAT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

## <a name="remarks"></a>Comentários

Essa função usa instruções de sombreador que não têm precisão alta o suficiente para fornecer a resposta exata. A função alternativa [**D3DX \_ R8G8B8A8 \_ UNORM \_ sRGB \_ para \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de sRGB para float.

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

 

 





