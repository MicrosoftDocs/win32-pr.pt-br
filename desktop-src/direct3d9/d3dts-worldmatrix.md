---
description: Mapas índices no intervalo de 0 a 255 para os estados de transformação correspondentes.
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
ms.openlocfilehash: 03a93753790378a7066f4a3ffa6bc6b7fb8139b77f9096886161013653312bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850056"
---
# <a name="d3dts_worldmatrix-macro"></a>\_Macro D3DTS WORLDMATRIX

Mapas índices no intervalo de 0 a 255 para os estados de transformação correspondentes.

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

## <a name="return-value"></a>Valor retornado

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

 

 
