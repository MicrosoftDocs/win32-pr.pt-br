---
description: Inicializa uma cor com os valores Alfa, vermelho, verde e azul fornecidos.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: Macro D3DCOLOR_ARGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298534"
---
# <a name="d3dcolor_argb-macro"></a>\_Macro ARGB D3DCOLOR

Inicializa uma cor com os valores Alfa, vermelho, verde e azul fornecidos.

## <a name="syntax"></a>Sintaxe


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

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

Retorna o valor de [D3DCOLOR](d3dcolor.md) que corresponde aos valores ARGB fornecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_RGBA D3DCOLOR**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




