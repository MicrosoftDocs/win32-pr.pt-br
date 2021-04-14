---
description: Cada origem do evento deve registrar os arquivos de mensagem que contêm cadeias de caracteres de descrição para cada identificador de evento, categoria de evento e parâmetro.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Arquivos de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505758"
---
# <a name="message-files"></a><span data-ttu-id="fc7f9-103">Arquivos de mensagem</span><span class="sxs-lookup"><span data-stu-id="fc7f9-103">Message Files</span></span>

<span data-ttu-id="fc7f9-104">Cada [origem do evento](event-sources.md) deve registrar os arquivos de mensagem que contêm cadeias de caracteres de descrição para cada [identificador de evento](event-identifiers.md), [categoria de evento](event-categories.md)e [parâmetro](event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="fc7f9-104">Each [event source](event-sources.md) should register message files that contain description strings for each [event identifier](event-identifiers.md), [event category](event-categories.md), and [parameter](event-identifiers.md).</span></span> <span data-ttu-id="fc7f9-105">Registre esses arquivos nos valores de registro **EventMessageFile**, **CategoryMessageFile** e **ParameterMessageFile** para a origem do evento.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-105">Register these files in the **EventMessageFile**, **CategoryMessageFile**, and **ParameterMessageFile** registry values for the event source.</span></span>

<span data-ttu-id="fc7f9-106">Você pode criar um arquivo de mensagem que contém descrições para os identificadores de evento, categorias e parâmetros, ou criar três arquivos de mensagem separados.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-106">You can create one message file that contains descriptions for the event identifiers, categories, and parameters, or create three separate message files.</span></span> <span data-ttu-id="fc7f9-107">Os identificadores de mensagem para todas as suas mensagens devem ser exclusivos, independentemente de você especificar as mensagens em um arquivo ou três arquivos.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-107">The message identifiers for all of your messages should be unique whether you specify the messages in one file or three files.</span></span> <span data-ttu-id="fc7f9-108">Vários aplicativos podem compartilhar o mesmo arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-108">Several applications can share the same message file.</span></span> <span data-ttu-id="fc7f9-109">Para obter mais informações sobre arquivos de mensagens, consulte [**compilador de mensagens**](/windows/desktop/WES/message-compiler--mc-exe-).</span><span class="sxs-lookup"><span data-stu-id="fc7f9-109">For more information on message files, see [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-).</span></span> <span data-ttu-id="fc7f9-110">Para obter detalhes sobre a sintaxe de um arquivo de mensagem, consulte [arquivos de texto da mensagem](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="fc7f9-110">For details on the syntax of a message file, see [Message Text Files](message-text-files.md).</span></span>

## <a name="example-message-file"></a><span data-ttu-id="fc7f9-111">Exemplo de arquivo de mensagem</span><span class="sxs-lookup"><span data-stu-id="fc7f9-111">Example Message File</span></span>

<span data-ttu-id="fc7f9-112">Este é um exemplo de arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-112">The following is an example message file.</span></span>

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

<span data-ttu-id="fc7f9-113">O aplicativo de exibição de eventos pode usar o procedimento a seguir para obter acesso às [cadeias de caracteres de mensagem](event-identifiers.md) na DLL de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-113">The event-viewing application can use the following procedure to gain access to the [message strings](event-identifiers.md) in the message DLL.</span></span>

<span data-ttu-id="fc7f9-114">**Para obter cadeias de caracteres de descrição**</span><span class="sxs-lookup"><span data-stu-id="fc7f9-114">**To obtain description strings**</span></span>

1.  <span data-ttu-id="fc7f9-115">Chame a função [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) para abrir a origem do evento.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-115">Call the [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) function to open the event source.</span></span>
2.  <span data-ttu-id="fc7f9-116">Chame a função [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para obter o conteúdo do valor de **EventMessageFile** para a origem do evento, que é o nome da dll da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-116">Call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function to obtain the contents of the **EventMessageFile** value for the event source, which is the name of the message DLL.</span></span>
3.  <span data-ttu-id="fc7f9-117">Chame a função [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para carregar a DLL de mensagem determinada pela etapa 2.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-117">Call the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message DLL determined by step 2.</span></span>
4.  <span data-ttu-id="fc7f9-118">Chame a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) com o identificador da mensagem para obter a descrição da dll.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-118">Call the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function with the message identifier to obtain the description from the DLL.</span></span> <span data-ttu-id="fc7f9-119">(Observe que os identificadores de mensagens são definidos no. Arquivo H gerado pelo compilador de mensagem.) A função **FormatMessage** substituirá as cadeias de caracteres de inserção usando os valores de argumento que você passa, mas não substituirá as cadeias de caracteres de inserção de parâmetro; Você deve substituir as cadeias de caracteres de inserção de parâmetro por conta própria antes de exibir a cadeia.</span><span class="sxs-lookup"><span data-stu-id="fc7f9-119">(Note that the messages identifiers are defined in the .H file generated by the message compiler.) The **FormatMessage** function will replace the insertion strings using the argument values that you pass but it will not replace the parameter insertion strings; you must replace the parameter insertion strings yourself before displaying the string.</span></span>

 

 
