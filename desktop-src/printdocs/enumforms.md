---
description: A função EnumForms enumera os formulários com suporte pela impressora especificada.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Função EnumForms (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e5ce18e81e4d775fdc801517867491740a7dd5035fc730226cb084e5af7d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732694"
---
# <a name="enumforms-function"></a>Função EnumForms

A **função EnumForms** enumera os formulários com suporte pela impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Lidar com a impressora para a qual os formulários devem ser enumerados. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*Nível* \[ Em\]
</dt> <dd>

Especifica a versão da estrutura para a qual *pForm aponta.* Esse valor deve ser 1 ou 2.

</dd> <dt>

*pForm* \[ out\]
</dt> <dd>

Ponteiro para uma ou mais [**estruturas FORM \_ INFO \_ 1**](form-info-1.md) ou para uma ou mais [**estruturas FORM \_ INFO \_ 2.**](form-info-2.md) Todas as estruturas terão o mesmo nível.

</dd> <dt>

*cbBuf* \[ Em\]
</dt> <dd>

Especifica o tamanho, em bytes, do buffer para o qual *pForm aponta.*

</dd> <dt>

*pcbNeeded* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o número de bytes copiados para a matriz para a qual *pForm* aponta (se a operação for bem-sucedida) ou o número de bytes necessários (se falhar porque *cbBuf* é muito pequeno).

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Ponteiro para uma variável que recebe o número de estruturas copiadas na matriz para a qual *pForm aponta.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Se o chamador for remoto e *o Nível* for 2, o valor **StringType** das estruturas [**FORM INFO \_ \_ 2**](form-info-2.md) retornadas sempre será **STRING \_ LANGPAIR**.

No Windows Vista, os dados de formulário retornados por **EnumForms** são recuperados de um cache local quando *hPrinter* se refere a um servidor de impressão remoto ou a uma impressora hospedada por um servidor de impressão e há pelo menos uma conexão aberta com uma impressora no servidor de impressão remota. Em todas as outras configurações, os dados do formulário são consultados do servidor de impressão remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumFormsW** (Unicode) **e EnumFormsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**INFORMAÇÕES \_ DO FORMULÁRIO \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




