---
description: A função FlushPrinter envia um buffer para a impressora a fim de limpá-lo de um estado transitório.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Função FlushPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505842"
---
# <a name="flushprinter-function"></a>Função FlushPrinter

A função **FlushPrinter** envia um buffer para a impressora a fim de limpá-lo de um estado transitório.

## <a name="syntax"></a>Sintaxe


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para o objeto de impressora. Deve ser o mesmo identificador que foi usado, em uma chamada [**WritePrinter**](writeprinter.md) anterior, pelo driver de impressora.

</dd> <dt>

*pBuf* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém os dados a serem gravados na impressora.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, da matriz apontada por *pBuf*.

</dd> <dt>

*pcWritten* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes de dados que foram gravados na impressora.

</dd> <dt>

*cSleep* \[ no\]
</dt> <dd>

O tempo, em milissegundos, para o qual a linha de e/s para a porta de impressora deve ser mantida ociosa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**FlushPrinter** deverá ser chamado somente se [**WritePrinter**](writeprinter.md) falhar, deixando a impressora em um estado transitório. Por exemplo, a impressora pode entrar em um estado transitório quando o trabalho é anulado e o driver de impressora enviou parcialmente alguns dados brutos para a impressora.

**FlushPrinter** também pode especificar um período ocioso durante o qual o spooler de impressão não agenda nenhum trabalho para a porta de impressora correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




