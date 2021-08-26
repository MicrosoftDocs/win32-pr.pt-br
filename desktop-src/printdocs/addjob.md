---
description: A função AddJob adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão. A função recupera o nome do arquivo que você pode usar para armazenar o trabalho.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: Função AddJob (Winspool.h)
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
ms.openlocfilehash: de99b0866e8cd7ec8486d2a3f15f95194b4350008a43fe4db8ae82d970684c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950746"
---
# <a name="addjob-function"></a>Função AddJob

A **função AddJob** adiciona um trabalho de impressão à lista de trabalhos de impressão que podem ser agendados pelo spooler de impressão. A função recupera o nome do arquivo que você pode usar para armazenar o trabalho.

> [!NOTE]
> No Windows 8 e sistemas operacionais posteriores, não recomendamos o uso de **AddJob** diretamente porque há casos (como impressão em uma fila usando Arquivo: ou PORTPROMPT:) em **que AddJob** falhará. Em vez disso, você é aconselhado a usar a API de Impressão [GDI,](gdi-printing.md)a API de Impressão [XPS,](xps-printing.md) [**o StartDocPrinter**](startdocprinter.md)ou o método apropriado do [**Windows. Namespace Graphics.Printing,**](/uwp/api/Windows.Graphics.Printing) dependendo do cenário de impressão.
>
> Se você tentar imprimir em uma fila usando **Arquivo:** ou **PORTPROMPT:**, **AddJob** retornará o erro NOT \_ SUPPORTED.

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

*hPrinter* \[ Em\]
</dt> <dd>

Um alça que especifica a impressora para o trabalho de impressão. Essa deve ser uma impressora local configurada como uma impressora em spool. Se *hPrinter for* um lidar com uma conexão de impressora remota ou se a impressora estiver configurada para impressão direta, a **função AddJob** falhará. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

A versão da estrutura de dados de informações de trabalho de impressão que a função armazena no buffer apontado por *pData*. De definir esse parâmetro como um.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma estrutura de dados [**ADDJOB \_ INFO \_ 1**](addjob-info-1.md) e uma cadeia de caracteres de caminho.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pData.* O buffer precisa ser grande o suficiente para conter uma estrutura [**ADDJOB \_ INFO \_ 1**](addjob-info-1.md) e uma cadeia de caracteres de caminho.

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho total, em bytes, da estrutura de dados [**ADDJOB \_ INFO \_ 1**](addjob-info-1.md) mais a cadeia de caracteres de caminho. Se esse valor for menor ou igual a *cbBuf* e a função for bem-sucedida, esse será o número real de bytes gravados no buffer apontado por *pData*. Se esse número for maior que *cbBuf*, o buffer será muito pequeno e você deverá chamar a função novamente com um tamanho de buffer pelo menos tão grande quanto \* *pcbNeeded*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Você pode chamar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o arquivo de spool especificado pelo membro **Path** da estrutura [**ADDJOB \_ INFO \_ 1**](addjob-info-1.md) e, em seguida, chamar a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para gravar dados de trabalho de impressão nele. Depois de fazer isso, chame a função [**ScheduleJob**](schedulejob.md) para notificar o spooler de impressão de que o trabalho de impressão agora pode ser agendado pelo spooler para impressão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddJobW** (Unicode) e **AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DE ADDJOB \_ \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[API de Impressão GDI](gdi-printing.md)
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

[**Windows. Graphics.Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[API de Impressão XPS](xps-printing.md)
</dt> </dl>

 

