---
description: Representa o contexto de execução quando GetPrintExecutionData é chamado.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Enumeração de PRINT_EXECUTION_CONTEXT (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169456"
---
# <a name="print_execution_context-enumeration"></a>Enumeração de contexto de \_ execução de impressão \_

Representa o contexto de execução quando [**GetPrintExecutionData**](getprintexecutiondata.md) é chamado.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**\_aplicativo de \_ contexto de execução de impressão \_**
</dt> <dd>

O chamador está sendo executado em um aplicativo.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ serviço spooler do contexto de execução de \_ impressão \_**
</dt> <dd>

O chamador está em execução no serviço de spooler (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_host de \_ isolamento do spooler do contexto de execução de \_ \_ impressão \_**
</dt> <dd>

O chamador está em execução no host de isolamento de impressão (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**\_pipeline de \_ filtro do contexto de execução de impressão \_ \_**
</dt> <dd>

O chamador está em execução no pipeline de filtro de impressão (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Contexto de execução de impressão \_ \_ \_ WOW64**
</dt> <dd>

O chamador está em execução no splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**IMPRIMIR \_ dados de execução \_**](print-execution-data.md)
</dt> </dl>

 

 




