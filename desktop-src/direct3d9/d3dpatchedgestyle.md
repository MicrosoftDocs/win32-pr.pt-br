---
description: Define se o modo de mosaico atual é discreto ou contínuo.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumeração D3DPATCHEDGESTYLE (D3D9Types. h)
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
ms.openlocfilehash: e625b7c4ff12f9859efdcc2b10b551a2223adab6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837945"
---
# <a name="d3dpatchedgestyle-enumeration"></a>Enumeração D3DPATCHEDGESTYLE

Define se o modo de mosaico atual é discreto ou contínuo.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ discreto**
</dt> <dd>

Estilo de borda discreto. No modo discreto, você pode especificar o mosaico flutuante, mas ele será truncado para inteiros.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ contínuo**
</dt> <dd>

Estilo de borda contínua. No modo contínuo, o mosaico é especificado como valores float que podem ser tranqüilamente variados para reduzir os artefatos "pop-los".

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que o mosaico contínuo produz um padrão de mosaico completamente diferente do discreto para os mesmos valores de mosaico (isso é mais aparente no modo de wireframe). Portanto, 4,0 contínuo não é o mesmo que 4 discretos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




