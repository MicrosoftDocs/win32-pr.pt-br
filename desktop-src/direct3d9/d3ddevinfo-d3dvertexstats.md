---
description: Relata o número de triângulos que foram processados e recortados pelo processamento de vértice de software do tempo de execução.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: Estrutura de D3DDEVINFO_D3DVERTEXSTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3baa6738e5d90d2353beb6c7d7bf0ab85770af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105753314"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>\_Estrutura D3DDEVINFO D3DVERTEXSTATS

Relata o número de triângulos que foram processados e recortados pelo processamento de vértice de software do tempo de execução.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número total de triângulos que não são cortados neste quadro.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de novos triângulos gerados pelo recorte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o tempo de execução de depuração e o processamento de vértice de software para obter o número de primitivos cortados e não recortados para uma determinada cena. Os primitivos normalmente serão recortados com base em uma faixa de proteção (se houver um). A faixa de proteção de recorte é definida com parâmetros como GuardBandLeft em [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
