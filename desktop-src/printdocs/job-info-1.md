---
description: A \_ estrutura informações do trabalho \_ 1 especifica as informações do trabalho de impressão, como o valor do identificador de trabalho, o nome da impressora para a qual o trabalho está em spool, o nome do computador que criou o trabalho de impressão, o nome do usuário que possui o trabalho de impressão e assim por diante.
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: Estrutura de JOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d56d4d6bce15a661ce141d8e22d27a15837a9f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297465"
---
# <a name="job_info_1-structure"></a>Estrutura de informações do trabalho \_ \_ 1

A **estrutura \_ informações \_ do trabalho 1** especifica as informações do trabalho de impressão, como o valor do identificador de trabalho, o nome da impressora para a qual o trabalho está em spool, o nome do computador que criou o trabalho de impressão, o nome do usuário que possui o trabalho de impressão e assim por diante.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a>Membros

<dl> <dt>

**JobId**
</dt> <dd>

Um identificador de trabalho.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora para a qual o trabalho está no spool.

</dd> <dt>

**pMachineName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do computador que criou o trabalho de impressão.

</dd> <dt>

**pUserName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que possui o trabalho de impressão.

</dd> <dt>

**pDocument**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do trabalho de impressão (por exemplo, "MS-WORD: Review.doc").

</dd> <dt>

**pDatatype**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.

</dd> <dt>

**pStatus**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão. Esse membro deve ser verificado antes do *status* e, se *pStatus* for **nulo**, o status será definido pelo conteúdo do membro de status.

</dd> <dt>

**Status**
</dt> <dd>

O status do trabalho. O valor desse membro pode ser zero ou uma combinação de um ou mais dos valores a seguir. Um valor de zero indica que a fila de impressão foi pausada após o término do spool do documento.



| Valor                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| STATUS do trabalho \_ \_ bloqueado \_ DEVQ      | O driver não pode imprimir o trabalho.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| STATUS do trabalho \_ \_ concluído           | **Windows XP e posterior:** O trabalho é enviado para a impressora, mas o trabalho pode não ser impresso ainda.<br/> Consulte comentários para obter mais informações.<br/>                                                                                                                                                                                                                                                                                                                           |
| STATUS do trabalho \_ \_ excluído            | O trabalho foi excluído.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_exclusão do status do trabalho \_           | O trabalho está sendo excluído.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_erro de status do trabalho \_              | Um erro está associado ao trabalho.                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| STATUS do trabalho \_ \_ offline            | A impressora está offline.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_papel de status do trabalho \_           | A impressora está sem papel.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| STATUS do trabalho em \_ \_ pausa             | O trabalho está em pausa.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| STATUS do trabalho \_ \_ impresso            | O trabalho foi impresso.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_impressão do status do trabalho \_           | O trabalho está sendo impresso.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| reinicialização do status do trabalho \_ \_            | O trabalho foi reiniciado.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| STATUS do trabalho \_ \_ retido           | **Windows Vista e posterior:** O trabalho foi retido na fila de impressão e não pode ser excluído. Isso pode ser provocado pelo seguinte:<br/> 1) o trabalho foi retido manualmente por uma chamada para SetJob e o spooler está aguardando o trabalho ser liberado.<br/> 2) o trabalho não concluiu a impressão e deve concluir a impressão antes de poder ser excluído automaticamente.<br/> Consulte [**SetJob**](setjob.md) para obter mais informações sobre os comandos de trabalho de impressão.<br/> |
| \_spool de status do trabalho \_           | O trabalho está em spool.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_ \_ \_ intervenção do usuário do status do trabalho | A impressora tem um erro que exige que o usuário faça algo.                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**Prioridade**
</dt> <dd>

A prioridade do trabalho. Esse membro pode ser um dos valores a seguir ou no intervalo entre 1 e 99 (prioridade mínima \_ até a \_ prioridade máxima).



| Valor         | Significado           |
|---------------|-------------------|
| \_prioridade mínima | Prioridade mínima. |
| \_prioridade máxima | Prioridade máxima. |
| prioridade de DEF. \_ | Prioridade padrão. |



 

</dd> <dt>

**Posição**
</dt> <dd>

A posição do trabalho na fila de impressão.

</dd> <dt>

**TotalPages**
</dt> <dd>

O número total de páginas que o documento contém. Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

O número de páginas que foram impressas. Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.

</dd> <dt>

**Enviado**
</dt> <dd>

Uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que este documento foi colocado em spool.

Esse valor de tempo está no formato UTC (Universal Time Coordinate). Você deve convertê-lo em um valor de hora local antes de exibi-lo. Você pode usar a função [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para executar a conversão.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os monitores de porta que não dão suporte a TrueEndOfJob definirão o trabalho como status de trabalho \_ \_ impresso logo depois que o trabalho for enviado para a impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do trabalho \_ \_ 1W** (Unicode) e **\_ info do trabalho \_ \_ 1a** (ANSI)<br/>                                   |



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

 

