---
description: A função SetDefaultPrinter define o nome da impressora padrão para o usuário atual no computador local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Função SetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764267"
---
# <a name="setdefaultprinter-function"></a>Função SetDefaultPrinter

A função **SetDefaultPrinter** define o nome da impressora padrão para o usuário atual no computador local.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszPrinter* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora padrão. Para uma conexão de impressora remota, o formato de nome é **\\\\** _Server_ *_\\_* _PrinterName_. Para uma impressora local, o formato de nome é *PrinterName*.

Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, ou seja, "", o **SetDefaultPrinter** selecionará uma impressora padrão de uma das impressoras instaladas. Se uma impressora padrão já existir, chamar **SetDefaultPrinter** com uma cadeia de caracteres **nula** ou vazia nesse parâmetro poderá alterar a impressora padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Ao usar esse método, você deve especificar uma impressora, Driver e porta válidos. Se forem inválidas, as APIs não falharão, mas o resultado não será definido. Isso pode fazer com que outros programas configurassem a impressora de volta para a impressora válida anterior. Você pode usar [**EnumPrinters**](enumprinters.md) para recuperar o nome da impressora, o nome do driver e o nome da porta de todas as impressoras disponíveis.

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
| Nomes Unicode e ANSI<br/>   | **SetDefaultPrinterW** (Unicode) e **SetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 




