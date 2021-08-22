---
description: Representa o contexto de execução quando GetPrintExecutionData é chamado.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: PRINT_EXECUTION_CONTEXT enumeração (Winspool.h)
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
ms.openlocfilehash: 78e4afb29b75c0a73799302ddb76e270b18ca2c38cb6325b59ebae5041d5f99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033954"
---
# <a name="print_execution_context-enumeration"></a>Enumeração PRINT \_ EXECUTION \_ CONTEXT

Representa o contexto de execução [**quando GetPrintExecutionData**](getprintexecutiondata.md) é chamado.

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

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**IMPRIMIR \_ APLICATIVO DE CONTEXTO DE \_ \_ EXECUÇÃO**
</dt> <dd>

O chamador está em execução em um aplicativo.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**SERVIÇO \_ \_ SPOOLER DE CONTEXTO \_ DE EXECUÇÃO \_ DE IMPRESSÃO**
</dt> <dd>

O chamador está em execução no serviço de spooler (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**PRINT \_ EXECUTION \_ CONTEXT \_ SPOOLER \_ ISOLATION \_ HOST**
</dt> <dd>

O chamador está em execução no host de isolamento de impressão (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**PIPELINE DE \_ FILTRO DE CONTEXTO DE EXECUÇÃO DE \_ \_ \_ IMPRESSÃO**
</dt> <dd>

O chamador está em execução no pipeline de filtro de impressão (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**PRINT \_ EXECUTION \_ CONTEXT \_ WOW64**
</dt> <dd>

O chamador está em execução splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**IMPRIMIR \_ DADOS DE \_ EXECUÇÃO**](print-execution-data.md)
</dt> </dl>

 

 




