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
ms.openlocfilehash: caa6bc1eb9586c1526a7af674040fd703ff0a75a5055ce42e13378206e82c879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300320"
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

*v* 
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

 

 




