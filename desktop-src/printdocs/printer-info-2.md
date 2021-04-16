---
description: A \_ estrutura informações da impressora \_ 2 especifica informações detalhadas sobre a impressora.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Estrutura de PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506095"
---
# <a name="printer_info_2-structure"></a>Estrutura de informações da impressora \_ \_ 2

A **estrutura \_ informações \_ da impressora 2** especifica informações detalhadas sobre a impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a>Membros

<dl> <dt>

**pServerName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica o servidor que controla a impressora. Se essa cadeia de caracteres for **nula**, a impressora será controlada localmente.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora.

</dd> <dt>

**pShareName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica o ponto de compartilhamento da impressora. (Essa cadeia de caracteres será usada somente se a impressora \_ \_A constante compartilhada do atributo foi definida para o membro **Attributes** .)

</dd> <dt>

**pPortName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora. Se uma impressora estiver conectada a mais de uma porta, os nomes de cada porta deverão ser separados por vírgulas (por exemplo, "LPT1:, LPT2:, LPT3:").

</dd> <dt>

**pDriverName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora.

</dd> <dt>

**pComment**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que fornece uma breve descrição da impressora.

</dd> <dt>

**pLocation**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o local físico da impressora (por exemplo, "Bldg. 38, sala 1164 ").

</dd> <dt>

**pDevMode**
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define dados de impressora padrão, como a orientação do papel e a resolução.

</dd> <dt>

**pSepFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo usado para criar a página separadora. Esta página é usada para separar trabalhos de impressão enviados para a impressora.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão usado pela impressora. Você pode usar a função [**EnumPrintProcessors**](enumprintprocessors.md) para obter uma lista de processadores de impressão instalados em um servidor.

</dd> <dt>

**pDatatype**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão. Você pode usar a função [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para obter uma lista de tipos de dados com suporte por um processador de impressão específico.

</dd> <dt>

**pParameters**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros de processador de impressão padrão.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para a impressora. Este membro pode ser **nulo**.

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



 

No Windows Server 2003, o valor a seguir também pode ser usado.

| Valor                  | Significado                                                                 |
|------------------------|-------------------------------------------------------------------------|
| atributo de impressora \_ \_ TS | Indica que a impressora está atualmente conectada por meio de um servidor de terminal. |



 

</dd> <dt>

**Prioridade**
</dt> <dd>

Um valor de prioridade que o spooler usa para rotear trabalhos de impressão.

</dd> <dt>

**Defaultanteriority**
</dt> <dd>

O valor de prioridade padrão atribuído a cada trabalho de impressão.

</dd> <dt>

**StartTime**
</dt> <dd>

A hora mais antiga em que a impressora imprimirá um trabalho. Esse valor é expresso como minutos decorridos desde 12:00 AM GMT (Greenwich Mean Time).

</dd> <dt>

**UntilTime**
</dt> <dd>

A última hora em que a impressora imprimirá um trabalho. Esse valor é expresso como minutos decorridos desde 12:00 AM GMT (Greenwich Mean Time).

</dd> <dt>

**Status**
</dt> <dd>

O status da impressora. Esse membro pode ser qualquer combinação razoável dos valores a seguir.



| Valor                               | Significado                                                          |
|-------------------------------------|------------------------------------------------------------------|
| STATUS da impressora \_ \_ ocupado               | A impressora está ocupada.                                             |
| porta de status da impressora \_ \_ \_ aberta         | A porta da impressora está aberta.                                        |
| \_erro de status da impressora \_              | A impressora está em um estado de erro.                                |
| \_inicialização do status da impressora \_       | A impressora está sendo inicializada.                                     |
| STATUS da impressora \_ \_ e/s \_ ativa         | A impressora está em um estado de entrada/saída ativo                   |
| \_ \_ feed manual de status da impressora \_       | A impressora está em um estado de feed manual.                           |
| STATUS da impressora \_ \_ sem \_ toner          | A impressora está sem toner.                                     |
| STATUS da impressora \_ \_ não \_ disponível     | A impressora não está disponível para impressão.                       |
| STATUS da impressora \_ \_ offline            | A impressora está offline.                                          |
| \_status \_ da impressora fora \_ da \_ memória    | A impressora ficou sem memória.                               |
| bandeja de saída de status da impressora \_ \_ \_ \_ cheia  | O compartimento de saída da impressora está cheio.                                |
| \_ \_ apontador de página de status da impressora \_         | A impressora não pode imprimir a página atual.                       |
| \_ \_ emperramento de papel do status da impressora \_         | O papel está emperrado na impressora                                   |
| \_saída do status da impressora \_ \_         | A impressora está sem papel.                                     |
| \_problema de \_ papel do status da impressora \_     | A impressora tem um problema de papel.                                 |
| STATUS da impressora em \_ \_ pausa             | A impressora está em pausa.                                           |
| \_exclusão de status \_ da impressora pendente \_  | A impressora está sendo excluída.                                    |
| \_economia de \_ energia de status da impressora \_        | A impressora está no modo de economia de energia.                               |
| \_impressão de status da impressora \_           | A impressora está imprimindo.                                         |
| \_processamento de status da impressora \_         | A impressora está processando um trabalho de impressão.                           |
| servidor de status de impressora \_ \_ \_ desconhecido    | O status da impressora é desconhecido.                                   |
| \_toner de status da impressora \_ \_ baixo         | A impressora está com pouco toner.                                     |
| \_status da \_ impressora \_ intervenção do usuário | A impressora tem um erro que exige que o usuário faça algo. |
| STATUS da impressora \_ \_ aguardando            | A impressora está aguardando.                                          |
| STATUS da impressora \_ \_ aquecendo \_        | A impressora está em preparação.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

O número de trabalhos de impressão que foram enfileirados para a impressora.

</dd> <dt>

**AveragePPM**
</dt> <dd>

O número médio de páginas por minuto que foram impressas na impressora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | Informações de **\_ impressora \_ \_ 2W** (Unicode) e **\_ informações de impressora \_ \_ 2a** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**Informações da impressora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Informações da impressora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Informações da impressora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**\_descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

