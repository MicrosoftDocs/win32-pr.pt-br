---
description: A \_ estrutura ADDJOB info \_ 1 identifica um trabalho de impressão, bem como o diretório e o arquivo em que um aplicativo pode armazenar esse trabalho.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Estrutura de ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171716"
---
# <a name="addjob_info_1-structure"></a>Estrutura de informações de ADDJOB \_ \_ 1

A estrutura **ADDJOB \_ info \_ 1** identifica um trabalho de impressão, bem como o diretório e o arquivo em que um aplicativo pode armazenar esse trabalho.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**Caminho**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o caminho e o nome do arquivo que o aplicativo pode usar para armazenar o trabalho de impressão.

</dd> <dt>

**JobId**
</dt> <dd>

Um identificador para o trabalho de impressão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ ADDJOB \_ info \_ 1W** (Unicode) e **\_ ADDJOB \_ info \_ 1a** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




