---
description: A função EnumPrinterDataEx enumera todos os nomes de valor e dados de uma impressora e chave especificadas.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Função EnumPrinterDataEx (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e78c17cccf416d186c4669e3576c5a0c9bf2365cb048a73b42d583b187156f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034264"
---
# <a name="enumprinterdataex-function"></a>Função EnumPrinterDataEx

A **função EnumPrinterDataEx** enumera todos os nomes de valor e dados de uma impressora e chave especificadas.

Os dados da impressora são armazenados no Registro. Ao enumerar dados da impressora, não chame funções do Registro que possam alterar os dados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para a qual a função recupera dados de configuração. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*pKeyName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém os valores a enumerar. Use o caractere de backslash ( ) como umlimiter para especificar um \\ caminho com uma ou mais sub-chaves. **EnumPrinterDataEx** enumera todos os valores da chave, mas não enumera valores de subkeys da chave especificada. Use a [**função EnumPrinterKey**](enumprinterkey.md) para enumerar subkeys.

Se *pKeyName for* **NULL ou uma** cadeia de caracteres vazia, **EnumPrinterDataEx** retornará ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pEnumValues* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas [**PRINTER \_ ENUM \_ VALUES.**](printer-enum-values.md) Cada estrutura contém o nome do valor, o tipo, os dados e os tamanhos de um valor sob a chave.

</dd> <dt>

*cbEnumValues* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pcbEnumValues*. Se você definir *cbEnumValues* como zero, o *parâmetro pcbEnumValues* retornará o tamanho do buffer necessário.

</dd> <dt>

*pcbEnumValues* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de configuração recuperados. Se o tamanho do buffer especificado por *cbEnumValues* for muito pequeno, a função retornará ERROR MORE DATA e \_ \_ *pcbEnumValues* indicará o tamanho do buffer necessário.

</dd> <dt>

*pnEnumValues* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas [**PRINTER \_ ENUM \_ VALUES**](printer-enum-values.md) retornadas em *pEnumValues*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro do sistema.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**EnumPrinterDataEx** recupera dados de configuração de impressora definidos pelas funções [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData.**](setprinterdata.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrinterDataExW** (Unicode) **e EnumPrinterDataExA** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**VALORES \_ DE ENUM \_ DA IMPRESSORA**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




