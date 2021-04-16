---
description: Inicializa uma cor com os valores vermelho, verde, azul e alfa fornecidos.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Macro D3DCOLOR_RGBA (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750117"
---
# <a name="d3dcolor_rgba-macro"></a>\_Macro D3DCOLOR RGBA

Inicializa uma cor com os valores vermelho, verde, azul e alfa fornecidos.

## <a name="syntax"></a>Sintaxe


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
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

</dd> <dt>

*um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores RGBA fornecidos.

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

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




