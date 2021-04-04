---
description: Inicializa uma cor com os valores (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: Macro D3DCOLOR_XYUV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 12d539e44528c5e54a54209763e4cbe262cd16f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837923"
---
# <a name="d3dcolor_xyuv-macro"></a>\_Macro D3DCOLOR XYUV

Inicializa uma cor com os valores (y, u, v).

## <a name="syntax"></a>Sintaxe


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*y* 
</dt> <dd>

Componente de luminância da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*u* 
</dt> <dd>

Brilho azul da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*l* 
</dt> <dd>

Brilho vermelho da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor de [**D3DCOLOR**](d3dcolor.md) que corresponde aos valores fornecidos (y, u, v).

## <a name="remarks"></a>Comentários

Uma cor RGB pode ser reduzida para 16 bits por pixel por conversão para diferenças de luminosidade e cor com as seguintes equações:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



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

[**D3DCOLOR \_ AYUV**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




