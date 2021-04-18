---
description: O GetPrintExecutionData recupera o contexto de impressão atual.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Função GetPrintExecutionData (winspool. h)
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
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764051"
---
# <a name="getprintexecutiondata-function"></a>Função GetPrintExecutionData

O **GetPrintExecutionData** recupera o contexto de impressão atual.

> [!Note]  
> Essa função destina-se a uso por drivers de impressora que estão em execução no contexto do spooler de impressão.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o endereço da estrutura [**de \_ \_ dados de execução de impressão**](print-execution-data.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a função tiver sucesso; caso contrário, **false**. Se o valor de retorno for **false**, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o status de erro.

## <a name="remarks"></a>Comentários

Os drivers de impressora devem chamar o [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) no módulo winspool. drv para obter o endereço da função **GetPrintExecutionData** porque o **GetPrintExecutionData** não tem suporte no Windows Vista ou em versões anteriores do Windows.

**GetPrintExecutionData** só falhará se o valor de *pData* for **nulo**.

O valor do membro **clientAppPID** dos [**dados de \_ execução \_ de impressão**](print-execution-data.md) só será significativo se o valor do **contexto** for o contexto de **execução de impressão \_ \_ \_ WOW64**. Se o valor do **contexto** não for **o \_ contexto de execução de impressão \_ \_ WOW64**, o valor de **clientAppPID** será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**\_contexto de execução de impressão \_**](print-execution-context.md)
</dt> <dt>

[**IMPRIMIR \_ dados de execução \_**](print-execution-data.md)
</dt> </dl>

 

