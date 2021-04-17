---
description: A função GetDefaultPrinter recupera o nome da impressora padrão para o usuário atual no computador local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Função GetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811473"
---
# <a name="getdefaultprinter-function"></a>Função GetDefaultPrinter

A função **GetDefaultPrinter** recupera o nome da impressora padrão para o usuário atual no computador local.

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszBuffer* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma cadeia de caracteres terminada em nulo que contém o nome da impressora padrão. Se esse parâmetro for **NULL**, a função falhará e a variável apontada por *pcchBuffer* retornará o tamanho de buffer necessário, em caracteres.

</dd> <dt>

*pcchBuffer* \[ entrada, saída\]
</dt> <dd>

Na entrada, especifica o tamanho, em caracteres, do buffer *pszBuffer* . Na saída, recebe o tamanho, em caracteres, da cadeia de caracteres do nome da impressora, incluindo o caractere nulo de terminação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero e a variável apontada por *pcchBuffer* conterá o número de caracteres copiados para o buffer *pszBuffer* , incluindo o caractere nulo de terminação.

Se a função falhar, o valor retornado será zero.



| Valor                       | Significado                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| ERRO \_ de \_ buffer insuficiente | O buffer *pszBuffer* é muito pequeno. A variável apontada por *pcchBuffer* contém o tamanho de buffer necessário, em caracteres. |
| arquivo de erro \_ \_ não \_ encontrado     | Não há nenhuma impressora padrão.                                                                                                   |



 

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
| Nomes Unicode e ANSI<br/>   | **GetDefaultPrinterW** (Unicode) e **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 




