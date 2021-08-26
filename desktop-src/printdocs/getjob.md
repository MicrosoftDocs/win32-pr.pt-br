---
description: A função GetJob recupera informações sobre um trabalho de impressão especificado.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: Função GetJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 26665d6141ea36adbe8aeeca0555bc6a5e918cb5213a4fb7a6dbd315eac92a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949076"
---
# <a name="getjob-function"></a>Função GetJob

A **função GetJob** recupera informações sobre um trabalho de impressão especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para a qual os dados de trabalho de impressão são recuperados. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*JobId* \[ Em\]
</dt> <dd>

Identifica o trabalho de impressão para o qual recuperar dados. Use a [**função AddJob**](addjob.md) ou [**a função StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) para obter um identificador de trabalho de impressão.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

O tipo de informações retornadas no buffer *pJob.* Se *Level* for 1, *pJob* receberá uma estrutura [**JOB INFO \_ \_ 1.**](job-info-1.md) Se *Level* for 2, *pJob* receberá uma estrutura [**JOB INFO \_ \_ 2.**](job-info-2.md)

</dd> <dt>

*pJob* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura [**JOB \_ INFO \_ 1**](job-info-1.md) ou [**JOB INFO \_ \_ 2**](job-info-2.md) que contém informações sobre o trabalho. O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.

Para determinar o tamanho do buffer necessário, chame **GetJob** com *cbBuf* definido como zero. **GetJob** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna ERROR INSUFFICIENT BUFFER e o parâmetro \_ \_ *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, da matriz.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Um ponteiro para um valor que especifica o número de bytes copiados se a função for bem-sucedida ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetJobW** (Unicode) e **GetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO TRABALHO \_ 1**](job-info-1.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO TRABALHO \_ 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

