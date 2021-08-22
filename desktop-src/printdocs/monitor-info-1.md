---
description: A estrutura \_ MONITOR INFO \_ 1 identifica um monitor instalado.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: MONITOR_INFO_1 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dff4fa4913be25d8a7cb5cd3324bd6e13d68761147fa76c451b587fb9569257d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099080"
---
# <a name="monitor_info_1-structure"></a>Estrutura MONITOR \_ INFO \_ 1

A **estrutura MONITOR INFO \_ \_ 1** identifica um monitor instalado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**Pname**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica um monitor instalado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ MONITOR \_ INFO \_ 1W** (Unicode) e **\_ MONITOR INFO \_ \_ 1A** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**MONITORAR \_ INFORMAÇÕES \_ 2**](monitor-info-2.md)
</dt> </dl>

 

 




