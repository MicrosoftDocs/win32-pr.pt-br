---
description: A função SetDefaultPrinter define o nome da impressora padrão para o usuário atual no computador local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: Função SetDefaultPrinter (Winspool.h)
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
ms.openlocfilehash: 570e0d57c4a04cd4845883e825acfbbef0282186cc7289751737798ed52b9592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112116"
---
# <a name="setdefaultprinter-function"></a>Função SetDefaultPrinter

A **função SetDefaultPrinter** define o nome da impressora padrão para o usuário atual no computador local.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszPrinter* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora padrão. Para uma conexão de impressora remota, o formato de nome é **\\\\** _server_ *_\\_* _printername_. Para uma impressora local, o formato de nome é *printername*.

Se esse parâmetro for **NULL** ou uma cadeia de caracteres vazia, ou seja, "", **SetDefaultPrinter** selecionará uma impressora padrão de uma das impressoras instaladas. Se uma impressora padrão já existir, chamar **SetDefaultPrinter** com um **NULL** ou uma cadeia de caracteres vazia nesse parâmetro poderá alterar a impressora padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Ao usar esse método, você deve especificar uma impressora, um driver e uma porta válidos. Se elas são inválidas, as APIs não falham, mas o resultado não é definido. Isso poderia fazer com que outros programas definiam a impressora de volta para a impressora válida anterior. Você pode usar [**EnumPrinters**](enumprinters.md) para recuperar o nome da impressora, o nome do driver e o nome da porta de todas as impressoras disponíveis.

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

 

 




