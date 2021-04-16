---
description: A \_ estrutura informações da impressora \_ 5 especifica informações detalhadas sobre a impressora.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Estrutura de PRINTER_INFO_5 (winspool. h)
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
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768397"
---
# <a name="printer_info_5-structure"></a>Estrutura de informações da impressora \_ \_ 5

A **estrutura \_ informações \_ da impressora 5** especifica informações detalhadas sobre a impressora.

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

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora. Se uma impressora estiver conectada a mais de uma porta, os nomes de cada porta deverão ser separados por vírgulas (por exemplo, "LPT1:, LPT2:, LPT3:").

</dd> <dt>

**Atributos**
</dt> <dd>

Os atributos da impressora. Esse membro pode ser qualquer combinação razoável dos valores a seguir.

| Valor                                   | Significado                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| atributo de impressora \_ \_ direto              | O trabalho é enviado diretamente para a impressora (não é colocado no spool).                                                                                                                                |
| o \_ atributo de impressora \_ é \_ concluído \_ primeiro | Se a configuração e a impressora estiverem definidas para impressão durante o spool, todos os trabalhos que concluíram o spool serão agendados para impressão antes dos trabalhos que não concluíram o spool.                          |
| atributo de impressora \_ \_ habilitar \_ DEVQ        | Se definido, **DevQueryPrint** será chamado. **DevQueryPrint** poderá falhar se as configurações do documento e da impressora não corresponderem. Definir esse sinalizador faz com que documentos incompatíveis sejam mantidos na fila. |
| atributo de impressora \_ \_ oculto              | Reservado.                                                                                                                                                                               |
| atributo de impressora \_ \_ KEEPPRINTEDJOBS     | Se definido, os trabalhos são mantidos depois de serem impressos. Se forem desdefinidas, os trabalhos serão excluídos.                                                                                                               |
| atributo de impressora \_ \_ local               | A impressora é uma impressora local.                                                                                                                                                             |
| \_rede de atributos da impressora \_             | A impressora é uma conexão de impressora de rede.                                                                                                                                                |
| atributo de impressora \_ \_ publicado           | Indica se a impressora está publicada no serviço de diretório.                                                                                                                    |
| atributo de impressora \_ \_ na fila              | Se definido, a impressora coloca em spool e começa a impressão depois que a última página é colocada em spool. Se não for definido e \_ \_ o atributo de impressora Direct não estiver definido, a impressora spoole e imprime durante o spool.      |
| \_atributo de \_ impressora \_ somente bruto           | Indica que apenas trabalhos de impressão de tipo de dados brutos podem ser colocados em spool.                                                                                                                            |
| atributo de impressora \_ \_ compartilhado              | A impressora está compartilhada.                                                                                                                                                                      |



 

No Windows XP e versões posteriores do Windows, o valor a seguir também pode ser usado.

| Valor                   | Significado                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fax de atributo de impressora \_ | Se definido, a impressora é uma impressora de fax. Isso só pode ser definido pelo [**AddPrinter**](addprinter.md), mas pode ser recuperado por [**EnumPrinters**](enumprinters.md) e [**getprinter**](getprinter.md). |



 

No Windows Vista e versões posteriores do Windows, os valores a seguir também podem ser usados.

| Valor                               | Significado                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ nome amigável do atributo de impressora \_  | Um computador se conectou a essa impressora e deu a ela um nome amigável.           |
| \_computador de atributo de impressora \_         | A impressora é uma conexão por computador.                                             |
| atributo de impressora \_ \_ enviado por push \_    | A impressora foi instalada usando a política de usuário conexões de push Printer.     |
| computador com o atributo de impressora \_ \_ enviado por push \_ | A impressora foi instalada usando a política de computador conexões de impressora de envio por push. |



 

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
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações de impressora \_ \_ 5W** (Unicode) e **\_ informações de impressora \_ \_ 5a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




