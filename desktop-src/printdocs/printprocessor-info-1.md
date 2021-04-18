---
description: A \_ estrutura info do multiprocessador informações \_ 1 especifica o nome de um processador de impressão instalado.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Estrutura de PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781414"
---
# <a name="printprocessor_info_1-structure"></a>Estrutura informações do multiprocessador \_ \_ 1

A estrutura **info do multiprocessador \_ informações \_ 1** especifica o nome de um processador de impressão instalado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**pName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um processador de impressão instalado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ \_ \_ 1W** (Unicode) e informações de **\_ multiprocessadores \_ \_ 1a** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




