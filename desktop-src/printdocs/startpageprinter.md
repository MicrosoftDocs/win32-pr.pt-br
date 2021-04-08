---
description: A função StartPagePrinter notifica o spooler de que uma página está prestes a ser impressa na impressora especificada.
ms.assetid: 8ac7c47b-b3a7-4642-bfb7-54e014139fbf
title: Função StartPagePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f8d1c5cc296fae1b166b891fc881a6abcdb6b2af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921604"
---
# <a name="startpageprinter-function"></a>Função StartPagePrinter

A função **StartPagePrinter** notifica o spooler de que uma página está prestes a ser impressa na impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL StartPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Identificador para uma impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A sequência para um trabalho de impressão é a seguinte:

1.  Para iniciar um trabalho de impressão, chame [**StartDocPrinter**](startdocprinter.md).
2.  Para iniciar cada página, chame **StartPagePrinter**.
3.  Para gravar dados em uma página, chame [**WritePrinter**](writeprinter.md).
4.  Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).
5.  Repita 2, 3 e 4 para quantas páginas forem necessárias.
6.  Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).

Quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro. Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes. O limite de tamanho de página depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo.

## <a name="examples"></a>Exemplos

Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).

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

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




