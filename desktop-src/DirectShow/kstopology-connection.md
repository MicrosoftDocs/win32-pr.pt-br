---
description: Este tópico se aplica ao Windows XP Service Pack 2 ou posterior. A estrutura KSTOPOLOGY \_ CONNECTION descreve uma conexão de nó dentro de um filtro de streaming de kernel (KS). Um nó pode ser conectado a outro nó dentro do filtro ou a um pino no filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION estrutura (Ks.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: 80a7b6f046edd1cd7f602487a11d6a79c375276814f9374f4142d148699bb8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397240"
---
# <a name="kstopology_connection-structure"></a>Estrutura KSTOPOLOGY \_ CONNECTION

Este tópico se aplica ao Windows XP Service Pack 2 ou posterior.

A **estrutura KSTOPOLOGY \_ CONNECTION** descreve uma conexão de nó dentro de um filtro de streaming de kernel (KS). Um nó pode ser conectado a outro nó dentro do filtro ou a um pino no filtro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a>Membros

<dl> <dt>

**FromNode**
</dt> <dd>

Índice do nó upstream na conexão. Se a conexão upstream for um pin, em vez de um nó, o valor será KSFILTER \_ NODE.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Se o valor do **campo FromNode** for KSFILTER NODE, esse campo especificará o \_ índice do pino upstream. Caso contrário, esse campo será ignorado.

</dd> <dt>

**ToNode**
</dt> <dd>

Índice do nó downstream na conexão. Se a conexão downstream for um pin, em vez de um nó, o valor será KSFILTER \_ NODE.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Se o valor do campo **ToNode** for KSFILTER NODE, esse campo especificará o \_ índice do pino downstream. Caso contrário, esse campo será ignorado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Estruturas](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo::get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




