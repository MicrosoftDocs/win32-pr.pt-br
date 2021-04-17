---
description: A estrutura de entrega do PF \_ define os protocolos que são entregues ao analisador ou os protocolos que o analisador transfere para o.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Estrutura de PF_HANDOFFSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749237"
---
# <a name="pf_handoffset-structure"></a>Estrutura de entrega do PF \_

A estrutura de **\_ entrega do PF** define os protocolos que são entregues ao analisador ou os protocolos que o analisador transfere para o.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>Membros

<dl> <dt>

**nEntries**
</dt> <dd>

Número de protocolos.

</dd> <dt>

**Entrada**
</dt> <dd>

Uma matriz de [estruturas \_ HANDOFFENTRY de PF](pf-handoffentry.md) que definem cada protocolo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de [ \_ PARSERINFO de PF](pf-parserinfo.md) usa a estrutura de **\_ entrega do PF** para listar o seguinte:

-   Quais protocolos estão disponíveis para o analisador.
-   Para quais protocolos o analisador passa.

A estrutura de **\_ entrega do PF** deve ser alocada usando **HeapAlloc**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[PARSERINFO de PF \_](pf-parserinfo.md)
</dt> <dt>

[HANDOFFENTRY de PF \_](pf-handoffentry.md)
</dt> </dl>

 

 




