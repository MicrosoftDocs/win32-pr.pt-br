---
description: Define os modos de remoção com suporte.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Enumeração D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 062135f1eff43bd568f1b08674985b4744e0835ebf3fa9e78c2756a798f85ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989056"
---
# <a name="d3dcull-enumeration"></a>Enumeração D3DCULL

Define os modos de remoção com suporte.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ nenhum**
</dt> <dd>

Não faça a remoção de faces.

</dd> <dt>

<span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**PV de D3DCULL \_**
</dt> <dd>

Faça a remoção de faces com vértices no sentido horário.

</dd> <dt>

<span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**\_CCW D3DCULL**
</dt> <dd>

Faça a remoção de faces com vértices no sentido anti-horário.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores nesse tipo enumerado são usados pelo estado de renderização D3DRS de \_ seleção. Os modos de remoção definem como as faces traseiras são refeitas ao renderizar uma geometria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
