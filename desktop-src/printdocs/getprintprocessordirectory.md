---
description: A função GetPrintProcessorDirectory recupera o caminho para o diretório do processador de impressão no servidor especificado.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Função GetPrintProcessorDirectory (Winspool.h)
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
ms.openlocfilehash: 27e79305295d078912169a2a12a99aa516372486f9b5dcd1997161a030103dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719245"
---
# <a name="getprintprocessordirectory-function"></a>Função GetPrintProcessorDirectory

A **função GetPrintProcessorDirectory** recupera o caminho para o diretório do processador de impressão no servidor especificado.

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

*pName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor. Se esse parâmetro for **NULL,** um caminho local será retornado.

</dd> <dt>

*pEnvironment* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL,** o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

O nível da estrutura. Esse valor deve ser 1.

</dd> <dt>

*pPrintProcessorInfo* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o caminho. Observe que, para sistemas operacionais anteriores ao Windows Server 2003 SP 1, o caminho está no formato local para o servidor, não no formato remoto verdadeiro. Por exemplo, o caminho é dado como "%Windir% \\ System32 \\ Spool \\ Prtprocs %Environment%" em vez de \\ " \\ \\ ServerName \\ Print$ \\ Prtprocs \\ %Environment%", mesmo quando chamado para um servidor remoto. Para os sistemas operacionais Windows Server 2003 SP 1 e posterior, o caminho remoto verdadeiro é retornado.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho do buffer apontado por *pPrintProcessorInfo.*

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
| Nomes Unicode e ANSI<br/>   | **GetPrintProcessorDirectoryW** (Unicode) e **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 




