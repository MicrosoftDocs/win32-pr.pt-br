---
description: A função DeletePrinter exclui o objeto de impressora especificado.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Função DeletePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813526"
---
# <a name="deleteprinter-function"></a>Função DeletePrinter

A função **DeletePrinter** exclui o objeto de impressora especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ entrada, saída\]
</dt> <dd>

Identificador para um objeto de impressora que será excluído. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Se houver trabalhos de impressão restantes para serem processados para a impressora especificada, o **DeletePrinter** marcará a impressora para exclusão pendente e a excluirá quando todos os trabalhos de impressão tiverem sido impressos. Nenhum trabalho de impressão pode ser adicionado a uma impressora marcada para exclusão pendente.

Uma impressora marcada para exclusão pendente não pode ser mantida, mas seus trabalhos de impressão podem ser retidos, retomados e reiniciados. Se a impressora for mantida e houver trabalhos para a impressora, **DeletePrinter** falhará com o erro \_ acesso \_ negado.

Observe que o **DeletePrinter** não fecha o identificador que é passado para ele. Portanto, o aplicativo ainda deve chamar [**ClosePrinter**](closeprinter.md).

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

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




