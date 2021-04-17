---
description: O arquivo de mensagem de exemplo a seguir mostra como criar e usar um arquivo de texto de mensagem que define as mensagens em vários idiomas.
ms.assetid: 403eaccc-07a3-4368-a39a-18c706c65537
title: Arquivo de texto de mensagem de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e4247b1e39ef94c006262f282d8d830af11851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780547"
---
# <a name="sample-message-text-file"></a><span data-ttu-id="5dfdc-103">Arquivo de texto de mensagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="5dfdc-103">Sample Message Text File</span></span>

<span data-ttu-id="5dfdc-104">O arquivo de mensagem de exemplo a seguir mostra como criar e usar um arquivo de texto de mensagem que define as mensagens em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="5dfdc-104">The following sample message file shows how to create and use a message text file that defines messages in multiple languages.</span></span>

## <a name="sample-message-file"></a><span data-ttu-id="5dfdc-105">Arquivo de mensagem de exemplo</span><span class="sxs-lookup"><span data-stu-id="5dfdc-105">Sample Message File</span></span>

<span data-ttu-id="5dfdc-106">Este arquivo de mensagem de exemplo, Sample.mc, contém um bloco de comentário, seguido por uma seção de cabeçalho, seguido por mensagens em dois idiomas.</span><span class="sxs-lookup"><span data-stu-id="5dfdc-106">This sample message file, Sample.mc, contains a comment block, followed by a header section, followed by messages in two languages.</span></span> <span data-ttu-id="5dfdc-107">Você deve usar um editor compatível com Unicode para dar suporte simultâneo aos caracteres usados em diferentes idiomas escritos.</span><span class="sxs-lookup"><span data-stu-id="5dfdc-107">You must use a Unicode-compatible editor to simultaneously support the characters used in different written languages.</span></span> <span data-ttu-id="5dfdc-108">Para obter mais informações e uma descrição detalhada da sintaxe de arquivos. MC, consulte [arquivos de texto da mensagem](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="5dfdc-108">For more information and a detailed description of the syntax of .mc files, see [Message Text Files](message-text-files.md).</span></span>

``` syntax
; // ***** Sample.mc *****
; // This is the header section.

MessageIdTypedef=DWORD

SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
Warning=0x2:STATUS_SEVERITY_WARNING
Error=0x3:STATUS_SEVERITY_ERROR
)

FacilityNames=(System=0x0:FACILITY_SYSTEM
Runtime=0x2:FACILITY_RUNTIME
Stubs=0x3:FACILITY_STUBS
Io=0x4:FACILITY_IO_ERROR_CODE
)

LanguageNames=(English=0x409:MSG00409)
LanguageNames=(Japanese=0x411:MSG00411)

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x2
Severity=Warning
Facility=Io
SymbolicName=MSG_BAD_PARM1
Language=English
Cannot reconnect to the server.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x3
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2 which is in error.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x5
Severity=Informational
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1!d! attempts with %2!d!%% success%! Disconnect from 
the server and try again later.
.

Language=Japanese
<Japanese message string goes here>
.
```

 

 



