---
description: A \_ estrutura informações do monitor \_ 2 identifica um monitor.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Estrutura de MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663207"
---
# <a name="monitor_info_2-structure"></a>Estrutura de informações de MONITOR \_ \_ 2

A **estrutura \_ informações \_ do monitor 2** identifica um monitor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**pName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do monitor.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o monitor foi gravado (por exemplo, Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que é o nome da DLL do monitor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Monitor de \_ informações \_ 2W** (Unicode) e **\_ informações de monitor \_ \_ 2a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addmonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**Informações do MONITOR \_ \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




