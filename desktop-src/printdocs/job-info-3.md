---
description: A \_ estrutura informações do trabalho \_ 3 é usada para vincular um conjunto de trabalhos de impressão.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Estrutura de JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 111b292c5f355aceefa95fb01bafc2cb9220757618d39d4b3ca29bbf77ca4570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948676"
---
# <a name="job_info_3-structure"></a>Estrutura das informações do trabalho \_ \_ 3

A **estrutura \_ informações \_ do trabalho 3** é usada para vincular um conjunto de trabalhos de impressão.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>Membros

<dl> <dt>

**JobId**
</dt> <dd>

O identificador do trabalho de impressão.

</dd> <dt>

**NextJobId**
</dt> <dd>

O identificador do trabalho de impressão para o próximo trabalho de impressão no conjunto vinculado de trabalhos de impressão.

</dd> <dt>

**Reserved**
</dt> <dd>

Este valor está reservado para uso futuro. Você deve defini-lo como zero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




