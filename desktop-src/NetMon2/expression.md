---
description: Contém um grupo de matrizes ANDEXP avaliadas como pares.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Estrutura de expressão (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4efa1f79477e3dcc13bedfddb2cdca7fd660f5430b7d7f2b87dbd9d4b4425098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366833"
---
# <a name="expression-structure"></a>Estrutura de expressão

A estrutura de **expressão** contém um grupo de matrizes **ANDEXP** avaliadas como pares em expressões lógicas e, que têm o formato

(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a>Membros

<dl> <dt>

**nAndExps**
</dt> <dd>

Número de padrões de **ANDEXP** .

</dd> <dt>

**AndExp**
</dt> <dd>

Matriz de padrões de **ANDEXP** . O filtro de captura organiza todas as linhas dessa matriz como lógica e instruções. Lembre-se de que cada estrutura de expressão pode conter um máximo de quatro padrões de **ANDEXP** .

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como implementar essa estrutura como parte de um filtro de captura, consulte [filtros de captura](capture-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




