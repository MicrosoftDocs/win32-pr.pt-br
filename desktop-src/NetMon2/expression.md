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
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753429"
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

 

 




