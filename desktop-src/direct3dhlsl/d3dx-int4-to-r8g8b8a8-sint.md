---
title: D3DX_INT4_to_R8G8B8A8_SINT função
description: Empacota o XMINT4 determinado de volta em um SINT DXGI \_ FORMAT \_ R8G8B8A8. \_
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- D3DX_INT4_to_R8G8B8A8_SINT função HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdeb7a92bff374d7b93d647971afd52746fbb768d9a33ec7c3a5c33b1c493523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515860"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a>Função SINT D3DX \_ INT4 \_ \_ a R8G8B8A8 \_

Empacota o XMINT4 determinado de volta em um SINT DXGI \_ FORMAT \_ R8G8B8A8. \_

## <a name="syntax"></a>Sintaxe

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
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

 

 





