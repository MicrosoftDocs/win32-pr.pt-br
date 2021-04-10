---
description: A \_ estrutura informações do trabalho \_ 2 descreve um conjunto completo de valores associados a um trabalho.
ms.assetid: 0cc61e35-4ac9-47bd-bb0d-ff43854bdee5
title: Estrutura de JOB_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_2
- _JOB_INFO_2A
- _JOB_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d6b582267afceb01fd7ced7d6d46144664bb9d2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171707"
---
# <a name="job_info_2-structure"></a>Estrutura de informações do trabalho \_ \_ 2

A **estrutura \_ informações \_ do trabalho 2** descreve um conjunto completo de valores associados a um trabalho.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _JOB_INFO_2 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
} JOB_INFO_2, *PJOB_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**JobId**
</dt> <dd>

Um valor de identificador de trabalho.

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

**pNotifyName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que deve ser notificado quando o trabalho foi impresso ou quando ocorre um erro durante a impressão do trabalho.

</dd> <dt>

**pDatatype**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão que deve ser usado para imprimir o trabalho.

</dd> <dt>

**pParameters**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros do processador de impressão.

</dd> <dt>

**pDriverName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora que deve ser usado para processar o trabalho de impressão.

</dd> <dt>

**pDevMode**
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém dados de inicialização de dispositivo e de ambiente para o driver de impressora.

</dd> <dt>

**pStatus**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão. Esse membro deve ser verificado antes do **status** e, se **pStatus** for **nulo**, o status será definido pelo conteúdo do membro de status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

O valor deste membro é **nulo**. Não há suporte para recuperação e configuração de descritores de segurança de documento nesta versão.

</dd> <dt>

**Status**
</dt> <dd>

O status do trabalho. Esse membro pode ser um ou mais dos valores a seguir.

| Valor                           | Significado                                                      |
|---------------------------------|--------------------------------------------------------------|
| STATUS do trabalho \_ \_ bloqueado \_ DEVQ      | O driver não pode imprimir o trabalho.                             |
| STATUS do trabalho \_ \_ excluído            | O trabalho foi excluído.                                        |
| \_exclusão do status do trabalho \_           | O trabalho está sendo excluído.                                        |
| \_erro de status do trabalho \_              | Um erro está associado ao trabalho.                         |
| STATUS do trabalho \_ \_ offline            | A impressora está offline.                                          |
| \_papel de status do trabalho \_           | A impressora está sem papel.                                     |
| STATUS do trabalho em \_ \_ pausa             | O trabalho está em pausa.                                               |
| STATUS do trabalho \_ \_ impresso            | O trabalho foi impresso.                                             |
| \_impressão do status do trabalho \_           | O trabalho está sendo impresso.                                             |
| reinicialização do status do trabalho \_ \_            | O trabalho foi reiniciado.                                      |
| \_spool de status do trabalho \_           | O trabalho está em spool.                                             |
| \_ \_ \_ intervenção do usuário do status do trabalho | A impressora tem um erro que exige que o usuário faça algo. |



 

No Windows XP e versões posteriores do Windows, os seguintes valores também podem ser usados:

| Valor                 | Significado                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| STATUS do trabalho \_ \_ concluído | O trabalho é enviado para a impressora, mas pode não ser impresso ainda. Consulte comentários para obter mais informações. |
| STATUS do trabalho \_ \_ retido | O trabalho foi retido na fila de impressão após a impressão.                              |



 

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

**StartTime**
</dt> <dd>

A hora mais antiga em que o trabalho pode ser impresso.

</dd> <dt>

**UntilTime**
</dt> <dd>

A hora mais recente em que o trabalho pode ser impresso.

</dd> <dt>

**TotalPages**
</dt> <dd>

O número de páginas necessárias para o trabalho. Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho, em bytes, do trabalho.

</dd> <dt>

**Enviado**
</dt> <dd>

Uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que o trabalho foi enviado.

Esse valor de tempo está no formato UTC (Universal Time Coordinate). Você deve convertê-lo em um valor de hora local antes de exibi-lo. Você pode usar a função [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para executar a conversão.

</dd> <dt>

**Hora**
</dt> <dd>

O tempo total, em milissegundos, decorrido desde que o trabalho começou a ser impresso.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

O número de páginas que foram impressas. Esse valor pode ser zero se o trabalho de impressão não contiver informações de delimitação de página.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os monitores de porta que não dão suporte a TrueEndOfJob definirão o trabalho como status de trabalho \_ \_ impresso logo depois que o trabalho for enviado para a impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do trabalho \_ \_ 2W** (Unicode) e **\_ info do trabalho \_ \_ 2a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

