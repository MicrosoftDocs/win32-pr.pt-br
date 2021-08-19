---
description: A estrutura ANDEXP contém uma matriz de corresponde ao padrão usada para avaliar dados de quadro.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Estrutura ANDEXP (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ANDEXP
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7ee2ac65e10e0dc9be46ab103fe21abcc78dc403302b298f3eb2fc83000802cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982948"
---
# <a name="andexp-structure"></a>Estrutura ANDEXP

A **estrutura ANDEXP** contém uma matriz de corresponde ao padrão usada para avaliar dados de quadro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ANDEXP {
  DWORD        nPatternMatches;
  PATTERNMATCH PatternMatch[MAX_PATTERNS];
} ANDEXP, *LPANDEXP;
```



## <a name="members"></a>Membros

<dl> <dt>

**nPatternMatches**
</dt> <dd>

Número de corresponde ao padrão.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Matriz de elementos de combinação de padrões. Observe que cada **estrutura ANDEXP** pode conter até quatro elementos de combinação de padrões. Para obter mais informações sobre esse membro, consulte [Capturar filtros](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os padrões na matriz **PatternMatch** \[ MAX PATTERNS são unidos como pares em instruções OR \_ \] lógicas no formato

(Padrão 1 \| \| Padrão 2 \| \| Padrão 3).

Para obter mais informações sobre como implementar essa estrutura, consulte [Capturar filtros](capture-filters.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




