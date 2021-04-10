---
description: A função setform define as informações do formulário para a impressora especificada.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Função SetFormat (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296705"
---
# <a name="setform-function"></a>Função SetFormat

A função **setform** define as informações do formulário para a impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual as informações do formulário estão definidas. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pFormName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário para o qual as informações do formulário são definidas.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

A versão da estrutura à qual o *pForm* aponta. Esse valor deve ser 1 ou 2.

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

 

**SetFormat** pode ser chamado várias vezes para uma [**informação de formulário \_ \_ 2**](form-info-2.md)existente, cada chamada adiciona pares adicionais de valores **pDisplayName** e **wLangId** . Todas as versões de idiomas do formulário obterão os valores de **tamanho** e **ImageableArea** do **formulário \_ informações \_ 2** na chamada mais recente para **setform**.

Se o chamador for remoto e o *nível* for 2, o valor de **StringType** do [**formulário \_ info \_ 2**](form-info-2.md) não poderá ser String \_ MUIDLL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **SetFormW** (Unicode) e **setformaa** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Informações do formulário \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**Informações do formulário \_ \_ 2**](form-info-2.md)
</dt> </dl>

 

 




