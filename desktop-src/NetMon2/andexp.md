---
description: A estrutura ANDEXP contém uma matriz de correspondências de padrão usada para avaliar dados de quadro.
ms.assetid: e5f4c030-eb2b-4cc9-9032-9ad4701b6503
title: Estrutura ANDEXP (Netmon. h)
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
ms.openlocfilehash: 1d27d5bdd51a45b31f518271053f44b45917cdeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297016"
---
# <a name="andexp-structure"></a>Estrutura ANDEXP

A estrutura **ANDEXP** contém uma matriz de correspondências de padrão usada para avaliar dados de quadro.

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

Número de correspondências de padrão.

</dd> <dt>

**PatternMatch**
</dt> <dd>

Matriz de elementos de correspondência de padrões. Observe que cada estrutura **ANDEXP** pode conter até quatro elementos de correspondência de padrões. Para obter mais informações sobre esse membro, consulte [filtros de captura](capture-filters.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Os padrões na matriz de padrões **PatternMatch** \[ Max \_ \] são Unidos como pares em instruções or lógicas no formato

(Padrão 1 \| \| Padrão 2 \| \| padrão 3).

Para obter mais informações sobre como implementar essa estrutura, consulte [filtros de captura](capture-filters.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




