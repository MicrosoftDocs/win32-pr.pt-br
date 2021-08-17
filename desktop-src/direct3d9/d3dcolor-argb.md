---
description: Inicializa uma cor com os valores alfa, vermelho, verde e azul fornecidos.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB macro (D3d9types.h)
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
ms.openlocfilehash: 8b65ae82673e98d666754ae42348cb62b3c336a1e642a5f78607924dc58313dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805426"
---
# <a name="d3dcolor_argb-macro"></a>Macro ARGB D3DCOLOR \_

Inicializa uma cor com os valores alfa, vermelho, verde e azul fornecidos.

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

*Um* 
</dt> <dd>

Componente alfa da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*r* 
</dt> <dd>

Componente vermelho da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*G* 
</dt> <dd>

Componente verde da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul da cor. Esse valor deve estar no intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o [valor D3DCOLOR](d3dcolor.md) que corresponde aos valores ARGB fornecidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




