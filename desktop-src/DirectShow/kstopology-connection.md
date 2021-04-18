---
description: Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior. A estrutura de conexão do KSTOPOLOGY \_ descreve uma conexão de nó em um filtro de streaming de kernel (KS). Um nó pode ser conectado a outro nó dentro do filtro ou a um PIN no filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: Estrutura de KSTOPOLOGY_CONNECTION (KS. h)
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
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767672"
---
# <a name="kstopology_connection-structure"></a>Estrutura de conexão do KSTOPOLOGY \_

Este tópico aplica-se ao Windows XP Service Pack 2 ou posterior.

A estrutura de **\_ conexão do KSTOPOLOGY** descreve uma conexão de nó em um filtro de streaming de kernel (KS). Um nó pode ser conectado a outro nó dentro do filtro ou a um PIN no filtro.

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

Índice do nó upstream na conexão. Se a conexão upstream for um PIN, em vez de um nó, o valor será KSFILTER \_ nó.

</dd> <dt>

**FromNodePin**
</dt> <dd>

Se o valor do campo **FromNode** for KSFILTER \_ nó, esse campo especificará o índice do pino upstream. Caso contrário, esse campo será ignorado.

</dd> <dt>

**ToNode**
</dt> <dd>

Índice do nó downstream na conexão. Se a conexão downstream for um PIN, em vez de um nó, o valor será KSFILTER \_ nó.

</dd> <dt>

**ToNodePin**
</dt> <dd>

Se o valor do campo **tonode** for KSFILTER \_ node, esse campo especificará o índice do PIN do downstream. Caso contrário, esse campo será ignorado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsTopologyInfo:: get \_ ConnectionInfo**](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




