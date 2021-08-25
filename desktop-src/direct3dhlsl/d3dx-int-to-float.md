---
title: D3DX_INT_to_FLOAT função
description: Converte um valor INT em FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT função HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d49320c2b7bfd53b2fa4e0303a7d2e9bf6c22427557ee3827aed31f5915d1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855486"
---
# <a name="d3dx_int_to_float-function"></a>Função D3DX \_ INT \_ to \_ FLOAT

Converte um valor INT em FLOAT.

## <a name="syntax"></a>Sintaxe

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*\_V* 
</dt> <dd>

O valor v.

</dd> <dt>

*\_Escala* 
</dt> <dd>

O valor de escala.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor int convertido.

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

 

 





