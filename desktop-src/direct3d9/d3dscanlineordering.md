---
description: Sinalizadores que indicam o método que o rasterizador usa para criar uma imagem em uma superfície.
ms.assetid: 55cf790e-ebe9-4791-a2be-a90fc76bae57
title: Enumeração D3DSCANLINEORDERING (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSCANLINEORDERING
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e5265387973c3c1605ac0022d88df3afa676dda614d7cc238e29a1ddd4a73f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987226"
---
# <a name="d3dscanlineordering-enumeration"></a>Enumeração D3DSCANLINEORDERING

Sinalizadores que indicam o método que o rasterizador usa para criar uma imagem em uma superfície.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSCANLINEORDERING { 
  D3DSCANLINEORDERING_PROGRESSIVE  = 1,
  D3DSCANLINEORDERING_INTERLACED   = 2
} D3DSCANLINEORDERING, *LPD3DSCANLINEORDERING;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSCANLINEORDERING_PROGRESSIVE"></span><span id="d3dscanlineordering_progressive"></span>**D3DSCANLINEORDERING \_ progressivo**
</dt> <dd>

A imagem é criada da primeira varredura para a última sem ignorar nenhuma.

</dd> <dt>

<span id="D3DSCANLINEORDERING_INTERLACED"></span><span id="d3dscanlineordering_interlaced"></span>**D3DSCANLINEORDERING \_ entrelaçado**
</dt> <dd>

A imagem é criada usando o método entrelaçado no qual as linhas ímpares são desenhadas em passagens de números ímpares e até mesmo as linhas são desenhadas em passagens de número par.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração é usada como um membro em [**D3DDISPLAYMODEFILTER**](d3ddisplaymodefilter.md) e [**D3DDISPLAYMODEEX**](d3ddisplaymodeex.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




