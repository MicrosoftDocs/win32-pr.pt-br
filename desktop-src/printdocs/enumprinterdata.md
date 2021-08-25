---
description: A função EnumPrinterData enumera dados de configuração para uma impressora especificada.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Função EnumPrinterData (Winspool.h)
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
ms.openlocfilehash: a542b6a0432ccf7065d94eeb8ebb3acbd8e2ace22044f2cc8984a1f4b2404299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846076"
---
# <a name="enumprinterdata-function"></a>Função EnumPrinterData

A **função EnumPrinterData** enumera dados de configuração para uma impressora especificada.

Para recuperar os dados de configuração em uma única chamada, use a [**função EnumPrinterDataEx.**](enumprinterdataex.md)

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

*hPrinter* \[ Em\]
</dt> <dd>

Um alça para a impressora cujos dados de configuração devem ser obtidos. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

Um valor de índice que especifica o valor de dados de configuração a ser recuperado.

De definir esse parâmetro como zero para a primeira chamada para **EnumPrinterData para** um alça de impressora especificado. Em seguida, incremente o parâmetro em um para chamadas subsequentes que envolvem a mesma impressora, até que a função retorne ERROR \_ NO \_ MORE \_ ITEMS. Consulte a seção Comentários a seguir para obter mais informações.

Se você usar a técnica mencionada nas descrições dos parâmetros *cbValueName* e *cbData* para obter valores de tamanho de buffer adequados, definir esses parâmetros como zero em uma primeira chamada para **EnumPrinterData** para um alça de impressora especificado, o valor *de dwIndex* não importará para essa chamada. De *definir dwIndex* como zero na próxima chamada para **EnumPrinterData** para iniciar o processo de enumeração real.

Os valores de dados de configuração não são ordenados. Novos valores terão um índice arbitrário. Isso significa que a **função EnumPrinterData** pode retornar valores em qualquer ordem.

</dd> <dt>

*pValueName* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o nome do valor de dados de configuração, incluindo um caractere nulo de terminação.

</dd> <dt>

*cbValueName* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pValueName.*

Se você quiser que o sistema operacional fornece um tamanho de buffer adequado, de definir esse parâmetro e o parâmetro *cbData* como zero para a primeira chamada para **EnumPrinterData** para um alça de impressora especificado. Quando a função for retornada, a variável apontada por *pcbValueName* conterá um tamanho de buffer grande o suficiente para enumerar com êxito todos os nomes de valor de dados de configuração da impressora.

</dd> <dt>

*pcbValueName* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes armazenados no buffer apontado por *pValueName.*

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado. Para ver uma lista dos códigos de tipo possíveis, consulte [Tipos de valor do Registro](/windows/desktop/SysInfo/registry-value-types). O *parâmetro pType* poderá ser **NULL se** o código de tipo não for necessário.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Um ponteiro para um buffer que recebe o valor dos dados de configuração.

Esse parâmetro poderá ser **NULL se** o valor dos dados de configuração não for necessário.

</dd> <dt>

*cbData* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pData.*

Se você quiser que o sistema operacional fornecer um tamanho de buffer adequado, de definir esse parâmetro e o parâmetro *cbValueName* como zero para a primeira chamada para **EnumPrinterData** para um alça de impressora especificado. Quando a função retorna, a variável apontada por *pcbData* conterá um tamanho de buffer grande o suficiente para enumerar com êxito todos os nomes de valor de dados de configuração da impressora.

</dd> <dt>

*pcbData* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes armazenados no buffer apontado por *pData*.

Esse parâmetro poderá ser **NULL se** *pData* for **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será ERROR \_ SUCCESS.

Se a função falhar, o valor de retorno será um código de erro do sistema.

A função retorna ERROR NO MORE ITEMS quando não há mais valores de dados de configuração \_ a recuperar para um alça de impressora \_ \_ especificado.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

**EnumPrinterData** recupera dados de configuração de impressora definidos pela [**função SetPrinterData.**](setprinterdata.md) Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados. A **função EnumPrinterData** obtém um desses valores e seu nome e um código de tipo, cada vez que você o chama. Chame a **função EnumPrinterData** várias vezes em sucessão para obter todos os valores de dados de configuração de uma impressora.

Os dados de configuração da impressora são armazenados no Registro. Ao enumerar dados de configuração da impressora, você deve evitar chamar funções do Registro que podem alterar esses dados.

Se você quiser que o sistema operacional fornecer um tamanho de buffer adequado, primeiro chame **EnumPrinterData** com os parâmetros *cbValueName* e *cbData* definidos como zero, conforme foi feito anteriormente na seção Parâmetros. O valor *de dwIndex* não importa para essa chamada. Quando a função for retornada, \* *pcbValueName* e \* *pcbData* conterão tamanhos de buffer grandes o suficiente para enumerar todos os valores e nomes de valor de dados de configuração da impressora. Na próxima chamada, aloque o nome do valor e os buffers de dados, de definir *cbValueName* e *cbData* para os tamanhos em bytes dos buffers alocados e de definir *dwIndex* como zero. Depois disso, continue a chamar a função **EnumPrinterData,** incrementando *dwIndex* em um a cada vez, até que a função retorne ERROR \_ NO MORE \_ \_ ITEMS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrinterDataW** (Unicode) **e EnumPrinterDataA** (ANSI)<br/>                                 |



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

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

