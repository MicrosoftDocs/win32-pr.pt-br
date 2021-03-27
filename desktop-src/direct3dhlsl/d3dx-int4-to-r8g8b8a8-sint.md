---
title: Função D3DX_INT4_to_R8G8B8A8_SINT
description: Empacota o XMINT4 determinado de volta para um \_ formato dxgi \_ R8G8B8A8 \_ Santo.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- Função D3DX_INT4_to_R8G8B8A8_SINT HLSL
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
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989278"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a>D3DX \_ INT4 \_ para \_ R8G8B8A8 \_ Santo function

Empacota o XMINT4 determinado de volta para um \_ formato dxgi \_ R8G8B8A8 \_ Santo.

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

Os dados do sombreador a serem empacotados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Os dados do sombreador embalado.

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

 

 





