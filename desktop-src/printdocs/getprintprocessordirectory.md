---
description: A função GetPrintProcessorDirectory recupera o caminho para o diretório do processador de impressão no servidor especificado.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Função GetPrintProcessorDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837148"
---
# <a name="getprintprocessordirectory-function"></a>Função GetPrintProcessorDirectory

A função **GetPrintProcessorDirectory** recupera o caminho para o diretório do processador de impressão no servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor. Se esse parâmetro for **NULL**, um caminho local será retornado.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O nível da estrutura. Esse valor deve ser 1.

</dd> <dt>

*pPrintProcessorInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o caminho. Observe que, para sistemas operacionais anteriores ao Windows Server 2003 SP 1, o caminho está no formato local para o servidor, não no verdadeiro formato remoto. Por exemplo, o caminho é fornecido como "% windir% \\ System32 \\ spool \\ prtprocs \\ % Environment" em vez de " \\ \\ ServerName \\ Print $ \\ prtprocs \\ % Environment%", mesmo quando chamado para um servidor remoto. Para os sistemas operacionais Windows Server 2003 SP 1 e posterior, o caminho remoto verdadeiro é retornado.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho do buffer apontado por *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que especifica o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **GetPrintProcessorDirectoryW** (Unicode) e **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 




