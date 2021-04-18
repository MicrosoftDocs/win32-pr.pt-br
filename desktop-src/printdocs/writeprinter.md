---
description: A função WritePrinter notifica o spooler de impressão que os dados devem ser gravados na impressora especificada.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Função WritePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771298"
---
# <a name="writeprinter-function"></a>Função WritePrinter

A função **WritePrinter** notifica o spooler de impressão que os dados devem ser gravados na impressora especificada.

> [!Note]  
> O **WritePrinter** dá suporte apenas à impressão GDI e não deve ser usado para impressão em XPS. Se seu trabalho de impressão usar o caminho de impressão XPS ou OpenXPS, use a [API de impressão XPS](/windows/desktop/printdocs/xps-printing). Não há suporte para o envio de trabalhos de impressão XPS ou OpenXPS para o spooler usando **WritePrinter** e isso pode resultar em resultados indeterminados.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pBuf* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de bytes que contém os dados que devem ser gravados na impressora.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, da matriz.

</dd> <dt>

*pcWritten* \[ fora\]
</dt> <dd>

Um ponteiro para um valor que recebe o número de bytes de dados que foram gravados na impressora.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A sequência para um trabalho de impressão é a seguinte:

1.  Para iniciar um trabalho de impressão, chame [**StartDocPrinter**](startdocprinter.md).
2.  Para iniciar cada página, chame [**StartPagePrinter**](startpageprinter.md).
3.  Para gravar dados em uma página, chame **WritePrinter**.
4.  Para encerrar cada página, chame [**EndPagePrinter**](endpageprinter.md).
5.  Repita 2, 3 e 4 para quantas páginas forem necessárias.
6.  Para encerrar o trabalho de impressão, chame [**EndDocPrinter**](enddocprinter.md).

Quando um documento de alto nível (como um arquivo Adobe PDF ou Microsoft Word) ou outros dados de impressora (como PCL, PS ou HPGL) são enviados diretamente para uma impressora, as configurações de impressão definidas no documento têm precedentes sobre as configurações de impressão do Windows. Documentos de saída quando o valor do membro *pDatatype* da estrutura [**info do documento \_ \_ 1**](doc-info-1.md) que foi passado no parâmetro *pDocInfo* da chamada [**StartDocPrinter**](startdocprinter.md) é "RAW" deve descrever totalmente as configurações do trabalho de impressão estilo de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)no idioma compreendido pelo hardware.

Em versões do Windows anteriores ao Windows XP, quando uma página em um arquivo em spool excede aproximadamente 350 MB, ela pode falhar ao imprimir e não enviar uma mensagem de erro. Por exemplo, isso pode ocorrer ao imprimir arquivos EMF grandes. O limite de tamanho de página nas versões do Windows anteriores ao Windows XP depende de muitos fatores, incluindo a quantidade de memória virtual disponível, a quantidade de memória alocada por processos de chamada e a quantidade de fragmentação no heap de processo. No Windows XP e versões posteriores do Windows, os arquivos EMF devem ter 2 GB ou menos de tamanho. Se **WritePrinter** for usado para gravar dados não EMF, como a PDL pronta para impressão, o tamanho do arquivo será limitado apenas pelo espaço em disco disponível.

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

 

