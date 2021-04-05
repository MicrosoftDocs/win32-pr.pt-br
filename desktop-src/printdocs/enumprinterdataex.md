---
description: A função EnumPrinterDataEx enumera todos os nomes de valor e dados para uma impressora e chave especificadas.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Função EnumPrinterDataEx (winspool. h)
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
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662606"
---
# <a name="enumprinterdataex-function"></a>Função EnumPrinterDataEx

A função **EnumPrinterDataEx** enumera todos os nomes de valor e dados para uma impressora e chave especificadas.

Os dados da impressora são armazenados no registro. Ao enumerar os dados da impressora, não chame funções de registro que possam alterar os dados.

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

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual a função recupera dados de configuração. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pKeyName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém os valores a serem enumerados. Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho com uma ou mais subchaves. **EnumPrinterDataEx** enumera todos os valores da chave, mas não enumera os valores de subchaves da chave especificada. Use a função [**EnumPrinterKey**](enumprinterkey.md) para enumerar subchaves.

Se *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **EnumPrinterDataEx** retornará um \_ parâmetro inválido de erro \_ .

</dd> <dt>

*pEnumValues* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas de [**\_ \_ valores de enumeração de impressora**](printer-enum-values.md) . Cada estrutura contém o nome do valor, o tipo, os dados e os tamanhos de um valor sob a chave.

</dd> <dt>

*cbEnumValues* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pcbEnumValues*. Se você definir *cbEnumValues* como zero, o parâmetro *pcbEnumValues* retornará o tamanho de buffer necessário.

</dd> <dt>

*pcbEnumValues* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de configuração recuperados. Se o tamanho do buffer especificado por *cbEnumValues* for muito pequeno, a função retornará um erro com \_ mais \_ dados e *pcbEnumValues* indicará o tamanho do buffer necessário.

</dd> <dt>

*pnEnumValues* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas de [**\_ \_ valores de enumeração de impressora**](printer-enum-values.md) retornado em *pEnumValues*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro do sistema.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**EnumPrinterDataEx** recupera os dados de configuração de impressora definidos pelas funções [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrinterDataExW** (Unicode) e **EnumPrinterDataExA** (ANSI)<br/>                             |



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

[**\_valores de enumeração da impressora \_**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




