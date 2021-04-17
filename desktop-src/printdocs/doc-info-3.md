---
description: A \_ estrutura informações do documento \_ 3 descreve um documento que será impresso.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Estrutura de DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798488"
---
# <a name="doc_info_3-structure"></a>Estrutura de informações do documento \_ \_ 3

A **estrutura \_ informações \_ do documento 3** descreve um documento que será impresso.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a>Membros

<dl> <dt>

**pDocName**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de um arquivo de saída.

</dd> <dt>

**pDatatype**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o tipo de dados usado para gravar o documento.

</dd> <dt>

**dwFlags**
</dt> <dd>

Flags. No momento, ele pode ser **nulo** ou o seguinte.



| Sinalizador                 | Significado                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_gravação de MEMORYMAP de di \_ | Faz com que o [**StartDocPrinter**](startdocprinter.md) não use [**AddJob**](addjob.md) e [**ScheduleJob**](schedulejob.md) para impressão local. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A \_ configuração de gravação de MEMORYMAP de di \_ no **documento \_ informações \_ 3** é uma otimização. Isso permite que o GDI mapeie arquivos de spool no aplicativo e acelere a gravação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do documento \_ \_ 3W** (Unicode) e **\_ info do documento \_ \_ 3a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




