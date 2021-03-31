---
description: A função StartDocPrinter notifica o spooler de impressão de que um documento deve ser colocado no spool para impressão.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Função StartDocPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836892"
---
# <a name="startdocprinter-function"></a>Função StartDocPrinter

A função **StartDocPrinter** notifica o spooler de impressão de que um documento deve ser colocado no spool para impressão.

## <a name="syntax"></a>Sintaxe


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura à qual o *pDocInfo* aponta. Esse valor deve ser 1.

</dd> <dt>

*pDocInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma [**estrutura \_ info \_**](doc-info-1.md) do documento 1 que descreve o documento a ser impresso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno identificará o trabalho de impressão.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A sequência típica para um trabalho de impressão é a seguinte:

1.  Para iniciar um trabalho de impressão, chame **StartDocPrinter**.
2.  Para iniciar cada página, chame [**StartPagePrinter**](startpageprinter.md).
3.  Para gravar dados em uma página, chame [**WritePrinter**](writeprinter.md).
4.  Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).
5.  Repita 2, 3 e 4 para quantas páginas forem necessárias.
6.  Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).

Observe que a chamada de [**StartPagePrinter**](startpageprinter.md) e [**EndPagePrinter**](endpageprinter.md) pode não ser necessária, como se o tipo de dados de impressão incluir as informações da página.

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
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **StartDocPrinterW** (Unicode) e **StartDocPrinterA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**Informações do documento \_ \_ 1**](doc-info-1.md)
</dt> <dt>

[**Informações do documento \_ \_ 2**](doc-info-2.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




