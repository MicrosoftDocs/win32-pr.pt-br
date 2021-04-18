---
description: Define as operações de combinação com suporte. Consulte comentários para ver as definições de termos.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Enumeração D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815564"
---
# <a name="d3dblendop-enumeration"></a>Enumeração D3DBLENDOP

Define as operações de combinação com suporte. Consulte comentários para ver as definições de termos.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Adicionar**
</dt> <dd>

O resultado é o destino adicionado à origem. Resultado = origem + destino

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**\_Subtrair D3DBLENDOP**
</dt> <dd>

O resultado é o destino subtraído da origem. Resultado = destino de origem

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**
</dt> <dd>

O resultado é a origem subtraída do destino. Resultado = origem-de-destino

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ mín.**
</dt> <dd>

O resultado é o mínimo da origem e do destino. Resultado = mín (origem, destino)

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**
</dt> <dd>

O resultado é o máximo da origem e do destino. Resultado = máximo (origem, destino)

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Origem, destino e resultado são definidos como:



| Termo        | Tipo   | Descrição                                                            |
|-------------|--------|------------------------------------------------------------------------|
| Fonte      | Entrada  | Cor do pixel de origem antes da operação.                        |
| Destino | Entrada  | A cor do pixel no buffer de destino antes da operação.     |
| Resultado      | Saída | Valor retornado que é a cor mesclada resultante da operação. |



 

Esse tipo enumerado define os valores usados pelos seguintes Estados de renderização:

-   D3DRS \_ BLENDOP
-   D3DRS \_ BLENDOPALPHA

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

 

 
