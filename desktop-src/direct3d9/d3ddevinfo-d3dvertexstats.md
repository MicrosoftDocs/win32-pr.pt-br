---
description: Relata o número de triângulos que foram processados e recortados pelo processamento de vértice de software do runtime.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: D3DDEVINFO_D3DVERTEXSTATS estrutura (D3D9Types.h)
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
ms.openlocfilehash: 80edbdcdeea5df6ff020c0c4cc2179db5152c15cc4965efe6580db7fd7bdcc48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894526"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>Estrutura D3DDEVINFO \_ D3DVERTEXSTATS

Relata o número de triângulos que foram processados e recortados pelo processamento de vértice de software do runtime.

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

Número total de triângulos que não são recortados nesse quadro.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de novos triângulos gerados pelo recorte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o runtime de depuração e o processamento de vértice de software para obter o número de primitivos não recortados e recortados para uma cena específica. Os primitivos normalmente serão recortados com base em uma faixa de proteção (se uma estiver presente). A faixa de proteção de recorte é definida com parâmetros como GuardBandLeft em [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
