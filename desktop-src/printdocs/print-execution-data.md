---
description: Contém o contexto de execução do driver de impressora que chama GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Estrutura de PRINT_EXECUTION_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170879"
---
# <a name="print_execution_data-structure"></a>Estrutura de dados de \_ execução de impressão \_

Contém o contexto de execução do driver de impressora que chama [**GetPrintExecutionData**](getprintexecutiondata.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**contexto**
</dt> <dd>

O valor do [**\_ \_ contexto de execução de impressão**](print-execution-context.md) que representa o contexto de execução atual do driver de impressora.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Se o valor do **contexto** for **o \_ contexto de execução de impressão \_ \_ WOW64**, **clientAppPID** identificará o aplicativo cliente em cujo nome o processo de splwow64.exe carregou o driver de impressora. Se o valor do **contexto** não for **o \_ contexto de execução de impressão \_ \_ WOW64**, **clientAppPID** será zero.

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

[**\_contexto de execução de impressão \_**](print-execution-context.md)
</dt> </dl>

 

 




