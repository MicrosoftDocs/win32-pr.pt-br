---
description: A função EnumPrinterKey enumera as sub-chaves de uma chave especificada para uma impressora especificada.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Função EnumPrinterKey (Winspool.h)
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
ms.openlocfilehash: c3666cce36884a331085d074df44e05b5bcfd0422433ce24bdbf3dbc385d7f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471780"
---
# <a name="enumprinterkey-function"></a>Função EnumPrinterKey

A **função EnumPrinterKey** enumera as sub-chaves de uma chave especificada para uma impressora especificada.

Os dados da impressora são armazenados no Registro. Ao enumerar dados da impressora, não chame funções do Registro que possam alterar os dados.

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

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora para a qual a função enumera subkeys. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*pKeyName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém as sub-chaves a enumerar. Use o caractere ' ' da faixa invertida como umlimiter para especificar um \\ caminho com uma ou mais sub-chaves. **EnumPrinterKey** enumera todas as sub-chaves da chave, mas não enumera as sub-chaves dessas subkeys.

Se *pKeyName for* uma cadeia de caracteres vazia (""), **EnumPrinterKey** enumera a chave de nível superior para a impressora. Se *pKeyName* for **NULL,** **EnumPrinterKey retornará** ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*pSubkey* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de nomes de sub-chaves terminadas em nulo. A matriz é encerrada por dois caracteres nulos.

</dd> <dt>

*cbSubkey* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pSubkey.* Se você definir *cbSubkey como* zero, o *parâmetro pcbSubkey* retornará o tamanho do buffer necessário.

</dd> <dt>

*pcbSubkey* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes recuperados no buffer *pSubkey.* Se o tamanho do buffer especificado por *cbSubkey* for muito pequeno, a função retornará ERROR MORE DATA e \_ \_ *pcbSubkey* indicará o tamanho do buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro do sistema. Se *pKeyName* não existir, o valor de retorno será ERROR \_ FILE NOT \_ \_ FOUND.

## <a name="remarks"></a>Comentários

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
| Nomes Unicode e ANSI<br/>   | **EnumPrinterKeyW** (Unicode) **e EnumPrinterKeyA** (ANSI)<br/>                                   |



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

 

 




