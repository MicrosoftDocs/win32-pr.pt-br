---
description: Descreve um conjunto completo de valores associados a um trabalho e dá suporte a arquivos de spool grandes com tamanhos expressos com 64 bits.
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: JOB_INFO_4 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dd338b4e6e486c59bfdac705b68c72c56eafb96c9f4e1899e9b4cb3b294791de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091916"
---
# <a name="job_info_4-structure"></a>Estrutura JOB \_ INFO \_ 4

Descreve um conjunto completo de valores associados a um trabalho e dá suporte a arquivos de spool grandes com tamanhos expressos com 64 bits.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _JOB_INFO_4 {
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
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a>Membros

<dl> <dt>

**Jobid**
</dt> <dd>

Um valor do identificador de trabalho.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora para a qual o trabalho está em spool.

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

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que deve ser notificado quando o trabalho foi impresso ou quando ocorre um erro ao imprimir o trabalho.

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

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica parâmetros de processador de impressão.

</dd> <dt>

**pDriverName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora que deve ser usado para processar o trabalho de impressão.

</dd> <dt>

**pDevMode**
</dt> <dd>

Um ponteiro para uma [**estrutura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém dados de ambiente e inicialização do dispositivo para o driver de impressora.

</dd> <dt>

**pStatus**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão. Esse membro deve ser verificado antes do **Status** e, se **pStatus** for **NULL,** o status será definido pelo conteúdo do membro Status.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

O valor desse membro é **NULL.** Não há suporte para recuperação e configuração de descritores de segurança de documento nesta versão.

</dd> <dt>

**Status**
</dt> <dd>

O status do trabalho. Esse membro pode ser um ou mais dos seguintes valores:

| Valor                           | Significado                                                      |
|---------------------------------|--------------------------------------------------------------|
| STATUS \_ DO TRABALHO BLOQUEADO \_ \_ DEVQ      | O driver não pode imprimir o trabalho.                             |
| \_STATUS DO TRABALHO \_ EXCLUÍDO            | O trabalho foi excluído.                                        |
| EXCLUSÃO \_ DO STATUS \_ DO TRABALHO           | O trabalho está sendo excluído.                                        |
| ERRO \_ DE STATUS DO \_ TRABALHO              | Um erro está associado ao trabalho.                         |
| \_STATUS DO TRABALHO \_ OFFLINE            | A impressora está offline.                                          |
| PAPEL DE \_ STATUS \_ DO TRABALHO           | A impressora está sem papel.                                     |
| \_STATUS DO TRABALHO \_ PAUSADO             | O trabalho está em pausa.                                               |
| STATUS \_ DO \_ TRABALHO IMPRESSO            | O trabalho foi impresso.                                             |
| IMPRESSÃO DE \_ STATUS \_ DO TRABALHO           | O trabalho está imprimindo.                                             |
| REINICIALIZAÇÃO \_ DO STATUS \_ DO TRABALHO            | O trabalho foi reiniciado.                                      |
| \_SPOOLING DE STATUS DO \_ TRABALHO           | O trabalho é o spooling.                                             |
| INTERVENÇÃO DO \_ USUÁRIO NO STATUS DO \_ \_ TRABALHO | A impressora tem um erro que exige que o usuário faça algo. |



 

No Windows XP e versões posteriores do Windows, os seguintes valores também podem ser usados:

| Valor                 | Significado                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| STATUS \_ DO \_ TRABALHO CONCLUÍDO | O trabalho é enviado para a impressora, mas pode não ser impresso ainda. Consulte Comentários para obter mais informações. |
| STATUS DO \_ \_ TRABALHO RETIDO | O trabalho foi mantido na fila de impressão após a impressão.                              |



 

</dd> <dt>

**Prioridade**
</dt> <dd>

A prioridade do trabalho. Esse membro pode ser um dos valores a seguir ou no intervalo entre 1 e 99 (MIN \_ PRIORITY até MAX \_ PRIORITY).



| Valor         | Significado           |
|---------------|-------------------|
| MIN \_ PRIORITY | Prioridade mínima. |
| PRIORIDADE \_ MÁXIMA | Prioridade máxima. |
| DEF \_ PRIORITY | Prioridade padrão. |



 

</dd> <dt>

**Posição**
</dt> <dd>

A posição do trabalho na fila de impressão.

</dd> <dt>

**StartTime**
</dt> <dd>

A primeira vez que o trabalho pode ser impresso.

</dd> <dt>

**UntilTime**
</dt> <dd>

A hora mais recente em que o trabalho pode ser impresso.

</dd> <dt>

**TotalPages**
</dt> <dd>

O número de páginas necessárias para o trabalho. Esse valor pode ser zero se o trabalho de impressão não contém informações de delimitação de página.

</dd> <dt>

**Tamanho**
</dt> <dd>

Os quatro bytes inferiores do tamanho, em bytes, do trabalho. Consulte também o **membro SizeHigh** abaixo.

</dd> <dt>

**Enviado**
</dt> <dd>

Uma [**estrutura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que o trabalho foi enviado.

Esse valor de hora está no formato UTC (Universal Time Coordinate). Você deve convertê-lo em um valor de hora local antes de exibi-lo. Você pode usar a [**função FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) para executar a conversão.

</dd> <dt>

**Hora**
</dt> <dd>

O tempo total, em milissegundos, decorrido desde o início da impressão do trabalho.

</dd> <dt>

**PagesPrinted**
</dt> <dd>

O número de páginas que foram impressas. Esse valor pode ser zero se o trabalho de impressão não contém informações de delimitação de página.

</dd> <dt>

**SizeHigh**
</dt> <dd>

Os quatro bytes mais altos do tamanho, em bytes, do trabalho. Consulte também o **membro Tamanho** acima.

</dd> </dl>

## <a name="remarks"></a>Comentários

Monitores de porta que não são suportados por TrueEndOfJob definirão o trabalho como STATUS DO TRABALHO IMPRESSO imediatamente após o trabalho \_ ser enviado para a \_ impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DE TRABALHO \_ 4W** (Unicode) e **\_ INFORMAÇÕES DE TRABALHO \_ \_ 4A** (ANSI)<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**Getjob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

