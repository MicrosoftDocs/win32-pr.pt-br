---
description: Inicializa uma cor usando os valores (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: Macro D3DCOLOR_AYUV (D3d9types. h)
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
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752756"
---
# <a name="d3dcolor_ayuv-macro"></a>\_Macro D3DCOLOR AYUV

Inicializa uma cor usando os valores (a, y, u, v).

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

*um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

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

Retorna o valor de [D3DCOLOR](d3dcolor.md) que corresponde aos valores ARGB fornecidos.

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

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




