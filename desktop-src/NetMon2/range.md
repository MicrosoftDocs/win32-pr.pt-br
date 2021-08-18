---
description: A estrutura RANGE define um intervalo de valores de propriedade válidos.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Estrutura RANGE (Netmon.h)
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
ms.openlocfilehash: 0e0135a6210aebbca38bfdede00231315dd2680461f366930b24925eda830604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063716"
---
# <a name="range-structure"></a>Estrutura RANGE

A **estrutura RANGE** define um intervalo de valores de propriedade válidos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a>Membros

<dl> <dt>

**Minvalue**
</dt> <dd>

O menor valor possível em um intervalo.

</dd> <dt>

**Maxvalue**
</dt> <dd>

O valor mais alto possível em um intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **estrutura RANGE** é usada para especificar um intervalo válido de números para uma propriedade de protocolo. Se o **membro DataQualifier** da estrutura **PROPERTYINFO** estiver definido como **PROP QUAL \_ \_ RANGE,** o membro **lpRange** da estrutura [PROPERTYINFO](propertyinfo.md) deverá fornecer um ponteiro para uma **estrutura RANGE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propertyinfo](propertyinfo.md)
</dt> </dl>

 

 




