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
ms.openlocfilehash: 1f7a2b871cc0181fbceab56e4ac14170bf46fa1b31081f4b4365ad7296ec2e85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600606"
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



 

no Windows XP e versões posteriores do Windows, o valor a seguir também pode ser usado.

| Valor                   | Significado                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fax de atributo de impressora \_ | Se definido, a impressora é uma impressora de fax. Isso só pode ser definido pelo [**AddPrinter**](addprinter.md), mas pode ser recuperado por [**EnumPrinters**](enumprinters.md) e [**getprinter**](getprinter.md). |



 

no Windows Vista e versões posteriores do Windows, os valores a seguir também podem ser usados.

| Valor                               | Significado                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ nome amigável do atributo de impressora \_  | Um computador se conectou a essa impressora e deu a ela um nome amigável.           |
| \_computador de atributo de impressora \_         | A impressora é uma conexão por computador.                                             |
| atributo de impressora \_ \_ enviado por push \_    | A impressora foi instalada usando a política de usuário conexões de push Printer.     |
| computador com o atributo de impressora \_ \_ enviado por push \_ | A impressora foi instalada usando a política de computador conexões de impressora de envio por push. |



 

no Windows Server 2003, o valor a seguir também pode ser usado.

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

A hora mais recente em que a impressora imprimirá um trabalho. Esse valor é expresso como minutos decorridos desde 00:00 GMT (Hora média de Greenwich).

</dd> <dt>

**Status**
</dt> <dd>

O status da impressora. Esse membro pode ser qualquer combinação razoável dos valores a seguir.



| Valor                               | Significado                                                          |
|-------------------------------------|------------------------------------------------------------------|
| STATUS DA \_ IMPRESSORA \_ OCUPADO               | A impressora está ocupada.                                             |
| PORTA \_ DE STATUS DA IMPRESSORA \_ \_ ABERTA         | A porta da impressora está aberta.                                        |
| ERRO DE \_ STATUS \_ DA IMPRESSORA              | A impressora está em um estado de erro.                                |
| INICIALIZAÇÃO \_ DO STATUS \_ DA IMPRESSORA       | A impressora está sendo inicializada.                                     |
| \_STATUS DA IMPRESSORA \_ E/S \_ ATIVO         | A impressora está em um estado de entrada/saída ativo                   |
| \_FEED MANUAL DE STATUS DA \_ \_ IMPRESSORA       | A impressora está em um estado de feed manual.                           |
| \_STATUS DA IMPRESSORA NÃO \_ \_ TONER          | A impressora está sem toner.                                     |
| \_STATUS DA IMPRESSORA NÃO \_ \_ DISPONÍVEL     | A impressora não está disponível para impressão.                       |
| \_STATUS DA IMPRESSORA \_ OFFLINE            | A impressora está offline.                                          |
| \_STATUS DA IMPRESSORA SEM \_ \_ \_ MEMÓRIA    | A impressora ficou sem memória.                               |
| COMPARTIMENTO DE \_ SAÍDA DE STATUS DA IMPRESSORA \_ \_ \_ CHEIO  | O compartimento de saída da impressora está cheio.                                |
| PUNT DA \_ PÁGINA STATUS \_ DA \_ IMPRESSORA         | A impressora não pode imprimir a página atual.                       |
| PAPEL \_ DE STATUS DA IMPRESSORA \_ \_ JAM         | O papel é ressalvado na impressora                                   |
| PAPEL \_ DE STATUS DA \_ \_ IMPRESSORA         | A impressora está sem papel.                                     |
| PROBLEMA DE \_ PAPEL DE STATUS DA \_ \_ IMPRESSORA     | A impressora tem um problema de papel.                                 |
| \_STATUS DA IMPRESSORA \_ PAUSADO             | A impressora está em pausa.                                           |
| \_EXCLUSÃO PENDENTE DO STATUS \_ \_ DA IMPRESSORA  | A impressora está sendo excluída.                                    |
| ECONOMIA DE \_ ENERGIA DO STATUS DA \_ \_ IMPRESSORA        | A impressora está no modo de economia de energia.                               |
| IMPRESSÃO DE \_ STATUS \_ DA IMPRESSORA           | A impressora está imprimindo.                                         |
| PROCESSAMENTO \_ DE STATUS DA \_ IMPRESSORA         | A impressora está processando um trabalho de impressão.                           |
| SERVIDOR \_ DE STATUS DA IMPRESSORA \_ \_ DESCONHECIDO    | O status da impressora é desconhecido.                                   |
| STATUS \_ DA IMPRESSORA \_ TONER \_ BAIXO         | A impressora está com pouco toner.                                     |
| INTERVENÇÃO DO \_ USUÁRIO NO STATUS DA \_ \_ IMPRESSORA | A impressora tem um erro que exige que o usuário faça algo. |
| STATUS DA \_ \_ IMPRESSORA AGUARDANDO            | A impressora está aguardando.                                          |
| AQUECIMENTO \_ DO STATUS DA \_ \_ IMPRESSORA        | A impressora está em preparação.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

O número de trabalhos de impressão que foram ensuados para a impressora.

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
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ INFORMAÇÕES \_ DA IMPRESSORA \_ 2W** (Unicode) e **\_ INFORMAÇÕES DA IMPRESSORA \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Imprimir estruturas de API do Spooler](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA \_ IMPRESSORA 1**](printer-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMAÇÕES \_ DA IMPRESSORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**DESCRITOR \_ DE SEGURANÇA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

