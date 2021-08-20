---
description: Cada origem do evento deve registrar os arquivos de mensagem que contêm cadeias de caracteres de descrição para cada identificador de evento, categoria de evento e parâmetro.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Arquivos de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44de0c91a098ab1b916a73d99a02d0d31a8b5b7690936322166e65baef4bd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951405"
---
# <a name="message-files"></a>Arquivos de mensagem

Cada [origem do evento](event-sources.md) deve registrar os arquivos de mensagem que contêm cadeias de caracteres de descrição para cada [identificador de evento](event-identifiers.md), [categoria de evento](event-categories.md)e [parâmetro](event-identifiers.md). Registre esses arquivos nos valores de registro **EventMessageFile**, **CategoryMessageFile** e **ParameterMessageFile** para a origem do evento.

Você pode criar um arquivo de mensagem que contém descrições para os identificadores de evento, categorias e parâmetros, ou criar três arquivos de mensagem separados. Os identificadores de mensagem para todas as suas mensagens devem ser exclusivos, independentemente de você especificar as mensagens em um arquivo ou três arquivos. Vários aplicativos podem compartilhar o mesmo arquivo de mensagem. Para obter mais informações sobre arquivos de mensagens, consulte [**compilador de mensagens**](/windows/desktop/WES/message-compiler--mc-exe-). Para obter detalhes sobre a sintaxe de um arquivo de mensagem, consulte [arquivos de texto da mensagem](message-text-files.md).

## <a name="example-message-file"></a>Exemplo de arquivo de mensagem

Este é um exemplo de arquivo de mensagem.

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

O aplicativo de exibição de eventos pode usar o procedimento a seguir para obter acesso às [cadeias de caracteres de mensagem](event-identifiers.md) na DLL de mensagem.

**Para obter cadeias de caracteres de descrição**

1.  Chame a função [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) para abrir a origem do evento.
2.  Chame a função [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para obter o conteúdo do valor de **EventMessageFile** para a origem do evento, que é o nome da dll da mensagem.
3.  Chame a função [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para carregar a DLL de mensagem determinada pela etapa 2.
4.  Chame a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) com o identificador da mensagem para obter a descrição da dll. (Observe que os identificadores de mensagens são definidos no. Arquivo H gerado pelo compilador de mensagem.) A função **FormatMessage** substituirá as cadeias de caracteres de inserção usando os valores de argumento que você passa, mas não substituirá as cadeias de caracteres de inserção de parâmetro; Você deve substituir as cadeias de caracteres de inserção de parâmetro por conta própria antes de exibir a cadeia.

 

 
