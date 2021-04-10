---
description: A função EnumPrinterData enumera dados de configuração para uma impressora especificada.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Função EnumPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169343"
---
# <a name="enumprinterdata-function"></a>Função EnumPrinterData

A função **EnumPrinterData** enumera dados de configuração para uma impressora especificada.

Para recuperar os dados de configuração em uma única chamada, use a função [**EnumPrinterDataEx**](enumprinterdataex.md) .

## <a name="syntax"></a>Sintaxe


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para a impressora cujos dados de configuração serão obtidos. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*dwIndex* \[ no\]
</dt> <dd>

Um valor de índice que especifica o valor dos dados de configuração a recuperar.

Defina esse parâmetro como zero para a primeira chamada para **EnumPrinterData** para um identificador de impressora especificado. Em seguida, aumente o parâmetro por um para chamadas subsequentes que envolvam a mesma impressora, até que a função retorne um erro \_ sem \_ mais \_ itens. Consulte a seção de comentários a seguir para obter mais informações.

Se você usar a técnica mencionada nas descrições dos parâmetros *cbValueName* e *cbData* para obter valores de tamanho de buffer adequados, definindo esses parâmetros como zero em uma primeira chamada para **EnumPrinterData** para um identificador de impressora especificado, o valor de *dwIndex* não é importante para essa chamada. Defina *dwIndex* como zero na próxima chamada para **EnumPrinterData** para iniciar o processo de enumeração real.

Os valores dos dados de configuração não são ordenados. Os novos valores terão um índice arbitrário. Isso significa que a função **EnumPrinterData** pode retornar valores em qualquer ordem.

</dd> <dt>

*valores principais* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o nome do valor dos dados de configuração, incluindo um caractere nulo de terminação.

</dd> <dt>

*cbValueName* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *valores* de datas.

Se você quiser que o sistema operacional forneça um tamanho de buffer adequado, defina esse parâmetro e o parâmetro *cbData* como zero para a primeira chamada para **EnumPrinterData** para um identificador de impressora especificado. Quando a função retornar, a variável apontada por *pcbValueName* conterá um tamanho de buffer grande o suficiente para enumerar com êxito todos os nomes de valor dos dados de configuração da impressora.

</dd> <dt>

*pcbValueName* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes armazenados no buffer apontado por *valores* de número.

</dd> <dt>

*pType* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado. Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types). O parâmetro *pType* poderá ser **nulo** se o código de tipo não for necessário.

</dd> <dt>

*pData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe o valor dos dados de configuração.

Esse parâmetro poderá ser **nulo** se o valor dos dados de configuração não for necessário.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pData*.

Se você quiser que o sistema operacional forneça um tamanho de buffer adequado, defina esse parâmetro e o parâmetro *cbValueName* como zero para a primeira chamada para **EnumPrinterData** para um identificador de impressora especificado. Quando a função retornar, a variável apontada por *pcbData* conterá um tamanho de buffer grande o suficiente para enumerar com êxito todos os nomes de valor dos dados de configuração da impressora.

</dd> <dt>

*pcbData* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes armazenados no buffer apontado por *pData*.

Esse parâmetro poderá ser **nulo** se *pData* for **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno será um código de erro do sistema.

A função retorna \_ um erro sem \_ mais itens quando não há \_ mais valores de dados de configuração a serem recuperados para um identificador de impressora especificado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**EnumPrinterData** recupera os dados de configuração da impressora definidos pela função [**SetPrinterData**](setprinterdata.md) . Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados. A função **EnumPrinterData** Obtém um desses valores, e seu nome e um código de tipo, cada vez que você o chama. Chame a função **EnumPrinterData** várias vezes em sucessão para obter todos os valores de dados de configuração de uma impressora.

Os dados de configuração da impressora são armazenados no registro. Ao enumerar os dados de configuração da impressora, você deve evitar chamar funções de registro que podem alterar esses dados.

Se você quiser que o sistema operacional forneça um tamanho de buffer adequado, primeiro chame **EnumPrinterData** com os parâmetros *cbValueName* e *cbData* definidos como zero, conforme observado anteriormente na seção parâmetros. O valor de *dwIndex* não importa para essa chamada. Quando a função retornar, \* *pcbValueName* e \* *pcbData* conterá tamanhos de buffer grandes o suficiente para enumerar todos os nomes e valores de valores de dados de configuração da impressora. Na próxima chamada, aloque o nome do valor e os buffers de dados, defina *cbValueName* e *cbData* para os tamanhos em bytes dos buffers alocados e defina *dwIndex* como zero. Depois disso, continue a chamar a função **EnumPrinterData** , incrementando *dwIndex* por um a cada vez, até que a função retorne \_ um erro sem \_ mais \_ itens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrinterDataW** (Unicode) e **EnumPrinterDataA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Setprinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

