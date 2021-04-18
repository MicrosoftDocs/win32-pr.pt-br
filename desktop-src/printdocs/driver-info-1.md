---
description: A \_ estrutura informações sobre o driver \_ 1 identifica um driver de impressora.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Estrutura de DRIVER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791603"
---
# <a name="driver_info_1-structure"></a>\_Estrutura informações do driver \_ 1

A **estrutura \_ informações \_ sobre o driver 1** identifica um driver de impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**pName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um driver de impressora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do driver \_ \_ 1W** (Unicode) e **\_ info do driver \_ \_ 1a** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

 




