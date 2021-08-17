---
title: Função D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
description: Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8A8 UNORM sRGB no formato dxgi para um XMFLOAT4. | Função D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
ms.assetid: f709267f-8dcd-47c8-b4cf-3cc903a08c35
keywords:
- Função D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b6fc32a06ff436046de76e212ef8f90a06338a55caa285865f12c98d6d4b068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793880"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4_inexact-function"></a>D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ \_ FLOAT4 \_ função inexata

Desempacota \_ \_ \_ \_ os dados do sombreador B8G8R8A8 UNORM sRGB no formato dxgi para um XMFLOAT4.

## <a name="syntax"></a>Sintaxe

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(
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

## <a name="remarks"></a>Comentários

Essa função usa instruções de sombreador que não têm precisão alta o suficiente para fornecer a resposta exata. A função alternativa [**D3DX \_ B8G8R8A8 \_ UNORM \_ sRGB \_ para \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md) usa uma tabela de pesquisa armazenada no sombreador para fornecer uma conversão exata de sRGB para float.

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

 

 





