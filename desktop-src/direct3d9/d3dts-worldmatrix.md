---
description: Mapeia índices no intervalo de 0 a 255 para os Estados de transformação correspondentes.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Macro D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506468"
---
# <a name="d3dts_worldmatrix-macro"></a>\_Macro D3DTS WORLDMATRIX

Mapeia índices no intervalo de 0 a 255 para os Estados de transformação correspondentes.

## <a name="syntax"></a>Sintaxe


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*index* 
</dt> <dd>

Um valor de índice no intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) que mapeia para o *índice* fornecido.

## <a name="remarks"></a>Comentários

Os Estados de transformação no intervalo de 256 a 511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
