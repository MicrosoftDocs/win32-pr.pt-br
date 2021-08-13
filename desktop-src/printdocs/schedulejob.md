---
description: A função ScheduleJob solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Função ScheduleJob (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a09d3e67b4be422f10db7761f28a2aa873e9bd0d84ec2c09de23ae20c7cea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470221"
---
# <a name="schedulejob-function"></a>Função ScheduleJob

A **função ScheduleJob** solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para o trabalho de impressão. Essa deve ser uma impressora local configurada como uma impressora em spool. Se *hPrinter for* um lidar com uma conexão de impressora remota ou se a impressora estiver configurada para impressão direta, a **função ScheduleJob** falhará. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

*hPrinter* deve ser o mesmo identificador de impressora especificado na chamada para [**AddJob**](addjob.md) que obteve o identificador de trabalho de impressão *dwJobID.*

</dd> <dt>

*dwJobID* \[ Em\]
</dt> <dd>

O trabalho de impressão a ser agendado. Você obtém esse identificador de trabalho de impressão chamando a [**função AddJob.**](addjob.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Você deve chamar com êxito a [**função AddJob**](addjob.md) antes de chamar a **função ScheduleJob.** **AddJob** obtém o identificador de trabalho de impressão que você passa para **ScheduleJob** como *dwJobID.* Ambas as chamadas devem usar o mesmo valor para *hPrinter*.

A **função ScheduleJob** verifica se há um arquivo de spool válido. Se houver um arquivo de spool inválido ou se ele estiver vazio, **ScheduleJob** excluirá o arquivo spool e a entrada de trabalho de impressão correspondente no spooler de impressão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addjob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




