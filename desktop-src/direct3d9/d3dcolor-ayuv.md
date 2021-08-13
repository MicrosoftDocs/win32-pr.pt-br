---
description: Inicializa uma cor usando os valores (a,y, u,v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 5e1900bf0d400971786eb37dd5138154913562982e1a1e3221c8002ac51fbf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300310"
---
# <a name="d3dcolor_ayuv-macro"></a>Macro AYUV D3DCOLOR \_

Inicializa uma cor usando os valores (a,y, u,v).

## <a name="syntax"></a>Sintaxe


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*y* 
</dt> <dd>

Componente Luminance da cor. Esse valor deve estar no intervalo de 0 a 255.

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

Retorna o [valor D3DCOLOR](d3dcolor.md) que corresponde aos valores ARGB fornecidos.

## <a name="remarks"></a>Comentários

Uma cor RGB pode ser reduzida para 16 bits por pixel por conversão em luminância e diferenças de cor com as seguintes equações:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




