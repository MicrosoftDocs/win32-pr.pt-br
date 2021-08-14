---
description: A função ResetPrinter especifica o tipo de dados e os valores do modo de dispositivo a serem usados para imprimir documentos enviados pela função StartDocPrinter. Esses valores podem ser substituídos usando a função SetJob após o início da impressão do documento.
ms.assetid: 9efc6629-dbb7-4320-90b9-07c66f0add47
title: Função ResetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResetPrinter
- ResetPrinterA
- ResetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: f68601acde884d15572871848eed2d2388c927cf04758ad1183343486d4cc0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470275"
---
# <a name="resetprinter-function"></a>Função ResetPrinter

A função **ResetPrinter** especifica o tipo de dados e os valores do modo de dispositivo a serem usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) . Esses valores podem ser substituídos usando a função [**SetJob**](setjob.md) após o início da impressão do documento.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ResetPrinter(
  _In_ HANDLE             hPrinter,
  _In_ LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Identificador para a impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pDefault* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ padrões de impressora**](printer-defaults.md) .

A função **ResetPrinter** ignora o membro **desiredAccess** da estrutura de [**\_ padrões da impressora**](printer-defaults.md) . Defina esse membro como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Nomes Unicode e ANSI<br/>   | **ResetPrinterW** (Unicode) e **ResetPrinterA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**padrões de impressora \_**](printer-defaults.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




