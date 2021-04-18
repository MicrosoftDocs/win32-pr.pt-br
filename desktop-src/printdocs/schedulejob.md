---
description: A função ScheduleJob solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Função ScheduleJob (winspool. h)
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
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811731"
---
# <a name="schedulejob-function"></a>Função ScheduleJob

A função **ScheduleJob** solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para o trabalho de impressão. Essa deve ser uma impressora local configurada como uma impressora em spool. Se *hPrinter* for um identificador para uma conexão de impressora remota, ou se a impressora estiver configurada para impressão direta, a função **ScheduleJob** falhará. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

*hPrinter* deve ser o mesmo identificador de impressora especificado na chamada para [**AddJob**](addjob.md) que obteve o identificador do trabalho de impressão *dwJobID* .

</dd> <dt>

*dwJobID* \[ no\]
</dt> <dd>

O trabalho de impressão a ser agendado. Você obtém esse identificador de trabalho de impressão chamando a função [**AddJob**](addjob.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Você deve chamar a função [**AddJob**](addjob.md) com êxito antes de chamar a função **ScheduleJob** . **AddJob** Obtém o identificador do trabalho de impressão que você passa para o **ScheduleJob** como *dwJobID*. As duas chamadas devem usar o mesmo valor para *hPrinter*.

A função **ScheduleJob** verifica um arquivo de spool válido. Se houver um arquivo de spool inválido, ou se estiver vazio, **ScheduleJob** excluirá o arquivo de spool e a entrada do trabalho de impressão correspondente no spooler de impressão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




