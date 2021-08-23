---
description: Define o local no qual um componente de cor ou cor deve ser acessado para cálculos de iluminação.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Enumeração D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3c8069fdde062fdc6dea311b40b8614d2165356ff397f0d056c43569f391e02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988886"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>Enumeração D3DMATERIALCOLORSOURCE

Define o local no qual um componente de cor ou cor deve ser acessado para cálculos de iluminação.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**MATERIAL de D3DMCS \_**
</dt> <dd>

Use a cor do material atual.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**
</dt> <dd>

Use a cor do vértice difuso.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

Use a cor do vértice especular.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses sinalizadores são usados para definir o valor dos seguintes Estados de renderização no tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .

-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ DiffuseMaterialSource
-   D3DRS \_ EMISSIVEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
