---
description: GetPrintExecutionData recupera o contexto de impressão atual.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Função GetPrintExecutionData (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: 0bbe08e82fb8f753d6e4fd23776618cb5f555b390434fdd0feddd231aaebc635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971345"
---
# <a name="getprintexecutiondata-function"></a>Função GetPrintExecutionData

**GetPrintExecutionData** recupera o contexto de impressão atual.

> [!Note]  
> Essa função destina-se ao uso por drivers de impressora que estão em execução no contexto do spooler de impressão.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o endereço da estrutura [**PRINT \_ EXECUTION \_ DATA.**](print-execution-data.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se a função for bem-sucedida; caso **contrário, FALSE.** Se o valor de retorno for **FALSE,** chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o status do erro.

## <a name="remarks"></a>Comentários

Os drivers de impressora devem chamar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) no módulo winspool.drv para obter o endereço da função **GetPrintExecutionData** porque **GetPrintExecutionData** não tem suporte no Windows Vista ou em versões anteriores do Windows.

**GetPrintExecutionData** só falhará se o valor de *pData* for **NULL.**

O valor do membro **clientAppPID** de [**PRINT EXECUTION \_ \_ DATA**](print-execution-data.md) só será significativo se o valor do contexto for **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64**.  Se o valor do **contexto não** for PRINT EXECUTION **CONTEXT \_ \_ \_ WOW64**, o valor **de clientAppPID** será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Getlasterror**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**CONTEXTO DE \_ EXECUÇÃO \_ DE IMPRESSÃO**](print-execution-context.md)
</dt> <dt>

[**IMPRIMIR \_ DADOS DE \_ EXECUÇÃO**](print-execution-data.md)
</dt> </dl>

 

