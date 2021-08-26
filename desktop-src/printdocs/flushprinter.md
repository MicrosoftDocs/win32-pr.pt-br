---
description: A função FlushPrinter envia um buffer para a impressora para desalocá-lo de um estado transitório.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Função FlushPrinter (Winspool.h)
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
ms.openlocfilehash: 78bd5b6ccc86651a717c29db8b938508c857f83dbd3bdf5364fb1596b8a2c956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949296"
---
# <a name="flushprinter-function"></a>Função FlushPrinter

A **função FlushPrinter** envia um buffer para a impressora para desalocá-lo de um estado transitório.

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

*hPrinter* \[ Em\]
</dt> <dd>

Um identificador para o objeto de impressora. Esse deve ser o mesmo handle que foi usado, em uma [**chamada writePrinter**](writeprinter.md) anterior, pelo driver de impressora.

</dd> <dt>

*pBuf* \[ Em\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém os dados a serem gravados na impressora.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

O tamanho, em bytes, da matriz apontada por *pBuf*.

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes de dados que foram gravados na impressora.

</dd> <dt>

*cSleep* \[ Em\]
</dt> <dd>

O tempo, em milissegundos, para o qual a linha de E/S para a porta da impressora deve ser mantida ociosa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**FlushPrinter** deverá ser chamado somente se [**WritePrinter**](writeprinter.md) falhar, deixando a impressora em um estado transitório. Por exemplo, a impressora pode entrar em um estado transitório quando o trabalho é anulado e o driver de impressora enviou parcialmente alguns dados brutos para a impressora.

**FlushPrinter também** pode especificar um período ocioso durante o qual o spooler de impressão não agenda nenhum trabalho para a porta de impressora correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




