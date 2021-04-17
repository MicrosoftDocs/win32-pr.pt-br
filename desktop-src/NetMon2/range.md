---
description: A estrutura do intervalo define um intervalo de valores de propriedade válidos.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Estrutura do intervalo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757017"
---
# <a name="range-structure"></a>Estrutura do intervalo

A estrutura do **intervalo** define um intervalo de valores de propriedade válidos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Membros

<dl> <dt>

**MinValue**
</dt> <dd>

Menor valor possível em um intervalo.

</dd> <dt>

**MaxValue**
</dt> <dd>

Maior valor possível em um intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura do **intervalo** é usada para especificar um intervalo válido de números para uma propriedade de protocolo. Se o membro **Dataqualificador** da estrutura **PropertyInfo** estiver definido como **prop \_ igual \_ Range**, o membro **lpRange** da estrutura [PropertyInfo](propertyinfo.md) deverá fornecer um ponteiro para uma estrutura de **intervalo** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




