---
description: A função AddJob adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão. A função recupera o nome do arquivo que você pode usar para armazenar o trabalho.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Função AddJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab21b98036975934c00e28d0be1d5670d4c0742c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662125"
---
# <a name="addjob-function"></a>Função AddJob

A função **AddJob** adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão. A função recupera o nome do arquivo que você pode usar para armazenar o trabalho.

> [!NOTE]
> No Windows 8 e sistemas operacionais posteriores, não recomendamos o uso do **AddJob** diretamente porque há casos (como imprimir em uma fila usando o arquivo: ou PORTPROMPT:) em que **AddJob** falhará. Em vez disso, é aconselhável usar a [API de impressão GDI](gdi-printing.md), a [API de impressão XPS](xps-printing.md), o [**StartDocPrinter**](startdocprinter.md)ou o método apropriado do namespace [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , dependendo do cenário de impressão.
>
> Se você tentar imprimir em uma fila usando o **arquivo:** ou **PORTPROMPT:**, **AddJob** retornará o erro sem \_ suporte.

## <a name="syntax"></a>Sintaxe

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador que especifica a impressora para o trabalho de impressão. Essa deve ser uma impressora local configurada como uma impressora em spool. Se *hPrinter* for um identificador para uma conexão de impressora remota, ou se a impressora estiver configurada para impressão direta, a função **AddJob** falhará. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura de dados de informações do trabalho de impressão que a função armazena no buffer apontado por *pData*. Defina esse parâmetro como um.

</dd> <dt>

*pData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura de dados [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e uma cadeia de caracteres de caminho.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pData*. O buffer precisa ser grande o suficiente para conter uma estrutura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e uma cadeia de caracteres de caminho.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho total, em bytes, da estrutura de dados [**ADDJOB \_ info \_ 1**](addjob-info-1.md) mais a cadeia de caracteres de caminho. Se esse valor for menor ou igual a *cbBuf* e a função tiver sucesso, esse será o número real de bytes gravados no buffer apontado por *pData*. Se esse número for maior que *cbBuf*, o buffer será muito pequeno e você deverá chamar a função novamente com um tamanho de buffer pelo menos tão grande quanto \* *pcbNeeded*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Você pode chamar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o arquivo de spool especificado pelo membro **Path** da estrutura [**ADDJOB \_ info \_ 1**](addjob-info-1.md) e, em seguida, chamar a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para gravar dados de trabalho de impressão nele. Depois disso, chame a função [**ScheduleJob**](schedulejob.md) para notificar o spooler de impressão de que o trabalho de impressão agora pode ser agendado pelo spooler para impressão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddJobW** (Unicode) e **AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Informações de ADDJOB \_ \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[API de impressão GDI](gdi-printing.md)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[API de impressão XPS](xps-printing.md)
</dt> </dl>

 

