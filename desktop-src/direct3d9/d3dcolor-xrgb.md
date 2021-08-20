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
ms.openlocfilehash: a31801236720d0a01eefe7f41ac6bd260c1364bb81c437cf6a85088c1c022b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527596"
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

## <a name="return-value"></a>Valor retornado

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

 

 




