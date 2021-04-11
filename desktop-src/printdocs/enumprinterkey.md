---
description: A função EnumPrinterKey enumera as subchaves de uma chave especificada para uma impressora especificada.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Função EnumPrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297148"
---
# <a name="enumprinterkey-function"></a>Função EnumPrinterKey

A função **EnumPrinterKey** enumera as subchaves de uma chave especificada para uma impressora especificada.

Os dados da impressora são armazenados no registro. Ao enumerar os dados da impressora, não chame funções de registro que possam alterar os dados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora para a qual a função enumera subchaves. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pKeyName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém as subchaves a serem enumeradas. Use o caractere de barra invertida ' \\ ' como um delimitador para especificar um caminho com uma ou mais subchaves. **EnumPrinterKey** enumera todas as subchaves da chave, mas não enumera as subchaves dessas subchaves.

Se *pKeyName* for uma cadeia de caracteres vazia (""), **EnumPrinterKey** enumerará a chave de nível superior para a impressora. Se *pKeyName* for **nulo**, **EnumPrinterKey** retornará um \_ parâmetro inválido de erro \_ .

</dd> <dt>

*pSubkey* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de nomes de subchaves terminadas em nulo. A matriz é terminada por dois caracteres nulos.

</dd> <dt>

*cbSubkey* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pSubkey*. Se você definir *cbSubkey* como zero, o parâmetro *pcbSubkey* retornará o tamanho de buffer necessário.

</dd> <dt>

*pcbSubkey* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes recuperados no buffer *pSubkey* . Se o tamanho do buffer especificado por *cbSubkey* for muito pequeno, a função retornará um erro com \_ mais \_ dados e *pcbSubkey* indicará o tamanho do buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro do sistema. Se *pKeyName* não existir, o valor de retorno será o \_ arquivo de erro \_ não \_ encontrado.

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
| Nomes Unicode e ANSI<br/>   | **EnumPrinterKeyW** (Unicode) e **EnumPrinterKeyA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




