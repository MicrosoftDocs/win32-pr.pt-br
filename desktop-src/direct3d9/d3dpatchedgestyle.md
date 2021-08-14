---
description: Define se o modo de mosaico atual é discreto ou contínuo.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumeração D3DPATCHEDGESTYLE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 717139a33e260aa29bc8d0e244fa49b3cb324c5249614f513faf0624ccf21841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987236"
---
# <a name="d3dpatchedgestyle-enumeration"></a>Enumeração D3DPATCHEDGESTYLE

Define se o modo de mosaico atual é discreto ou contínuo.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ DISCRETE**
</dt> <dd>

Estilo de borda discreto. No modo discreto, você pode especificar o mosaico float, mas ele será truncado para inteiros.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ CONTINUOUS**
</dt> <dd>

Estilo de borda contínua. No modo contínuo, o mosaico é especificado como valores float que podem ser suavemente variados para reduzir os artefatos de "estouro".

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que o mosaico contínuo produz um padrão de mosaico completamente diferente do discreto para os mesmos valores de mosaico (isso é mais aparente no modo wireframe). Portanto, 4.0 contínuo não é o mesmo que 4 discreto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




