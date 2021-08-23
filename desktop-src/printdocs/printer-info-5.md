---
description: A estrutura PRINTER \_ INFO \_ 5 especifica informações detalhadas da impressora.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: PRINTER_INFO_5 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ef50f3bfd83a0c2dd49eb0a15cdae31f25588106926e606887292c705602dd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731417"
---
# <a name="printer_info_5-structure"></a>Estrutura DE \_ INFORMAÇÕES \_ DA IMPRESSORA 5

A **estrutura PRINTER INFO \_ \_ 5** especifica informações detalhadas da impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a>Membros

<dl> <dt>

**pPrinterName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora.

</dd> <dt>

**pPortName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora. Se uma impressora estiver conectada a mais de uma porta, os nomes de cada porta deverão ser separados por vírgulas (por exemplo, "LPT1:,LPT2:,LPT3:").

</dd> <dt>

**Atributos**
</dt> <dd>

Os atributos de impressora. Esse membro pode ser qualquer combinação razoável dos valores a seguir.

| Valor                                   | Significado                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ATRIBUTO PRINTER \_ \_ DIRECT              | O trabalho é enviado diretamente para a impressora (não é em spool).                                                                                                                                |
| ATRIBUTO PRINTER \_ \_ CONCLUIR \_ \_ PRIMEIRO | Se definido e a impressora estiver definida para print-while-spooling, todos os trabalhos que concluíram o spooling serão agendados para imprimir antes de trabalhos que não concluíram o spooling.                          |
| ATRIBUTO PRINTER \_ \_ ENABLE \_ DEVQ        | Se definido, **DevQueryPrint** será chamado. **O DevQueryPrint** poderá falhar se as configurações do documento e da impressora não corresponderem. Definir esse sinalizador faz com que documentos não relacionados sejam mantidos na fila. |
| ATRIBUTO PRINTER \_ \_ HIDDEN              | Reservado.                                                                                                                                                                               |
| ATRIBUTO PRINTER \_ \_ KEEPPRINTEDJOBS     | Se definido, os trabalhos serão mantidos depois que eles são impressos. Se não for o caso, os trabalhos serão excluídos.                                                                                                               |
| LOCAL \_ DO ATRIBUTO PRINTER \_               | A impressora é uma impressora local.                                                                                                                                                             |
| REDE DE \_ ATRIBUTOS DE \_ IMPRESSORA             | Impressora é uma conexão de impressora de rede.                                                                                                                                                |
| ATRIBUTO PRINTER \_ \_ PUBLICADO           | Indica se a impressora é publicada no serviço de diretório.                                                                                                                    |
| ATRIBUTO \_ PRINTER \_ NA FILA              | Se definido, a impressora será spools e começará a imprimir depois que a última página for em spool. Se não estiver definido e PRINTER \_ ATTRIBUTE DIRECT não estiver definido, a impressora será carregada e \_ imprimirá durante o spool.      |
| ATRIBUTO PRINTER \_ \_ RAW \_ ONLY           | Indica que somente trabalhos de impressão de tipo de dados brutos podem ser em spool.                                                                                                                            |
| ATRIBUTO PRINTER \_ \_ SHARED              | A impressora é compartilhada.                                                                                                                                                                      |



 

No Windows XP e versões posteriores do Windows, o valor a seguir também pode ser usado.

| Valor                   | Significado                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_FAX DO ATRIBUTO PRINTER \_ | Se definido, a impressora será uma impressora de fax. Isso só pode ser definido por [**AddPrinter,**](addprinter.md)mas pode ser recuperado por [**EnumPrinters**](enumprinters.md) e [**GetPrinter.**](getprinter.md) |



 

No Windows Vista e versões posteriores do Windows, os valores a seguir também podem ser usados.

| Valor                               | Significado                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| NOME AMIGÁVEL DO ATRIBUTO PRINTER \_ \_ \_  | Um computador se conectou a essa impressora e deu a ela um nome amigável.           |
| COMPUTADOR DE \_ ATRIBUTO DE \_ IMPRESSORA         | A impressora é uma conexão por computador.                                             |
| ATRIBUTO PRINTER \_ PUSHED \_ \_ USER    | A impressora foi instalada usando a política de usuário Conexões de Impressora por Push.     |
| COMPUTADOR COM \_ O ATRIBUTO PRINTER \_ \_ | A impressora foi instalada usando a política de computador Push Printer Connections. |



 

</dd> <dt>

**DeviceNotSelectedTimeout**
</dt> <dd>

Este valor não é usado.

</dd> <dt>

**TransmissionRetryTimeout**
</dt> <dd>

Este valor não é usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DA IMPRESSORA \_ 5W** (Unicode) e **\_ INFORMAÇÕES DA IMPRESSORA \_ \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA \_ IMPRESSORA 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




