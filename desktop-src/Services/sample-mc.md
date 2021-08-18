---
description: Este é um exemplo de arquivo de mensagem que pode ser usado para criar uma DLL somente de recursos a ser usada com o exemplo de serviço ao gravar eventos no log de eventos.
ms.assetid: d0d46041-5608-4abf-b833-7aae1744ef60
title: Sample.mc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9244ce043f8c3696efd46866dd7f29246d13553a5bc9a4ec05281fd56dbc60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889194"
---
# <a name="samplemc"></a>Sample.mc

Este é um exemplo de arquivo de mensagem que pode ser usado para criar uma DLL somente de recursos a ser usada com o exemplo de serviço ao gravar eventos no log de eventos.

Use as seguintes etapas para compilar a DLL:

1.  **MC-U sample.mc**
2.  **RC-r Sample. rc**
3.  **link-dll-NOENTRY -out:sample.dll amostra. res**

``` syntax
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

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=SVC_ERROR
Language=English
An error has occurred (%2).
.

; // A message file must end with a period on its own line
; // followed by a blank line.
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O exemplo de serviço completo](the-complete-service-sample.md)
</dt> </dl>

 

 



