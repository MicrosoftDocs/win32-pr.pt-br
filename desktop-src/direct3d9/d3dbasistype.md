---
description: Define o tipo base de uma superfície de patch de ordem superior.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumeração D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091949"
---
# <a name="d3dbasistype-enumeration"></a>Enumeração D3DBASISTYPE

Define o tipo base de uma superfície de patch de ordem superior.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**\_BEZIER D3DBASIS**
</dt> <dd>

Os vértices de entrada são tratados como uma série de patches de Bézier. O número de vértices especificado deve ser divisível por 4. Partes da malha além desse critério não serão renderizadas. A continuidade completa é presumida entre os subpatches no interior da superfície renderizada por cada chamada. Somente os vértices nos cantos de cada subpatch têm a garantia de estar na superfície resultante.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**
</dt> <dd>

Os vértices de entrada são tratados como pontos de controle de uma superfície B-spline. O número de aberturas renderizadas é de dois a menos do que o número de aberturas nessa direção. Em geral, a superfície gerada não contém os vértices de controle especificados.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**
</dt> <dd>

Uma base de interpolação define a superfície de forma que a superfície percorra todos os vértices de entrada especificados. No DirectX 8, essa era D3DBASIS \_ interpolação.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros de **D3DBASISTYPE** especificam a formulação a ser usada na avaliação do primitivo de superfície de patch de ordem superior durante o mosaico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**Informações de D3DRECTPATCH \_**](d3drectpatch-info.md)
</dt> <dt>

[**Informações de D3DTRIPATCH \_**](d3dtripatch-info.md)
</dt> </dl>

 

 




