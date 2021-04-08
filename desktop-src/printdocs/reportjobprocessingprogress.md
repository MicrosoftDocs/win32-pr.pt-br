---
description: Relata para o serviço spooler de impressão se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização e qual parte do processamento está em andamento no momento.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: Função ReportJobProcessingProgress (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 327d2f7cffe2f90a5719de38cef4cd3fde17e086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922170"
---
# <a name="reportjobprocessingprogress-function"></a>Função ReportJobProcessingProgress

Relata para o serviço spooler de impressão se um trabalho de impressão XPS está na fase de processamento de spool ou de renderização e qual parte do processamento está em andamento no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*printerHandle* \[ no\]
</dt> <dd>

Um identificador de impressora para o qual a função deve recuperar informações. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*jobId* \[in\]
</dt> <dd>

Identifica o trabalho de impressão para o qual recuperar dados. Use a função [**AddJob**](addjob.md) ou a função [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obter um identificador de trabalho de impressão.

</dd> <dt>

*jobOperation* 
</dt> <dd>

Especifica se o trabalho está na fase de spool ou na fase de renderização.

</dd> <dt>

*jobProgress* 
</dt> <dd>

Especifica qual parte do processamento está atualmente em andamento. Esse valor se refere a eventos na fase de processamento em spool ou de renderização, dependendo do valor de *jobOperation*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

> [!Note]  
> O **ReportJobProcessingProgress** só relatará o progresso do trabalho de impressão XPS se o trabalho de impressão estiver na fase de processamento em spool ou de renderização. O **ReportJobProcessingProgress** falhará se for chamado quando o trabalho de impressão XPS não estiver na fase de processamento em spool ou de renderização.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EPrintXPSJobOperation**](eprintxpsjoboperation.md)
</dt> <dt>

[**EPrintXPSJobProgress**](eprintxpsjobprogress.md)
</dt> </dl>

 

