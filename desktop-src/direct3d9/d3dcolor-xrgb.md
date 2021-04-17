---
description: Inicializa uma cor com os valores vermelho, verde e azul fornecidos.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Macro D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370931"
---
# <a name="d3dcolor_xrgb-macro"></a>\_Macro D3DCOLOR XRGB

Inicializa uma cor com os valores vermelho, verde e azul fornecidos.

## <a name="syntax"></a>Sintaxe


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*r* 
</dt> <dd>

Componente vermelho da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*m* 
</dt> <dd>

Componente verde da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor de [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores RGB fornecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_ARGB D3DCOLOR**](d3dcolor-argb.md)
</dt> <dt>

[**\_RGBA D3DCOLOR**](d3dcolor-rgba.md)
</dt> </dl>

 

 




