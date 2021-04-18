---
description: A função AddFormat adiciona um formulário à lista de formulários disponíveis que podem ser selecionados para a impressora especificada.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Função AddFormat (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810639"
---
# <a name="addform-function"></a>Função AddFormat

A função **AddFormat** adiciona um formulário à lista de formulários disponíveis que podem ser selecionados para a impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora que dá suporte à impressão com o formulário especificado. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O nível da estrutura à qual *pForm* aponta. Esse valor deve ser 1 ou 2.

</dd> <dt>

*pForm* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**informações de formulário \_ \_ 1**](form-info-1.md) ou de [**formulário \_ \_ 2**](form-info-2.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Um aplicativo pode determinar quais formulários estão disponíveis para uma impressora chamando a função [**EnumForms**](enumforms.md) .

Se *pForm* apontar para uma [**informação de formulário \_ \_ 2**](form-info-2.md), o **AddForm** falhará se um formulário com o nome especificado já existir ou se o valor de *pKeyword* da estrutura já existir.

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

[**EnumForms**](enumforms.md)
</dt> <dt>

[**Informações do formulário \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**Informações do formulário \_ \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




