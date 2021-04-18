---
description: A função de exportação RecognizeFrame indica se um dado é reconhecido como o protocolo que o analisador detecta. A função de exportação RecognizeFrame deve ser implementada para cada analisador compatível com a DLL do analisador.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Função de retorno de chamada RecognizeFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766247"
---
# <a name="recognizeframe-callback-function"></a>Função de retorno de chamada RecognizeFrame

A função de exportação **RecognizeFrame** indica se um dado é reconhecido como o protocolo que o analisador detecta. A função de exportação **RecognizeFrame** deve ser implementada para cada analisador compatível com a DLL do analisador.

## <a name="syntax"></a>Sintaxe


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFrame* \[ no\]
</dt> <dd>

Identificador para o quadro que contém os dados.

</dd> <dt>

*lpFrame* \[ no\]
</dt> <dd>

Ponteiro para o primeiro byte de um quadro. O ponteiro fornece uma maneira de exibir os dados que outros analisadores reconhecem.

</dd> <dt>

*lpProtocol* \[ no\]
</dt> <dd>

Ponteiro para o início dos dados não reivindicados. Normalmente, os dados não reivindicados estão localizados no meio de um quadro porque um analisador anterior declarou dados antes desse analisador. O analisador deve testar os dados não reivindicados primeiro.

</dd> <dt>

*MacType* \[ no\]
</dt> <dd>

Valor MAC do primeiro protocolo em um quadro. Normalmente, o valor de *MacType* é usado quando o analisador deve identificar o primeiro protocolo em um quadro. O valor de *MacType* pode ser um dos seguintes:



| Valor                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**tipo de MAC \_ \_ Ethernet**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**tipo de MAC \_ \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**tipo de MAC \_ \_ FDDI**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ no\]
</dt> <dd>

O número restante de bytes de um local em um quadro até o fim do quadro.

</dd> <dt>

*hPreviousProtocol* \[ no\]
</dt> <dd>

Identificador do protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ no\]
</dt> <dd>

Deslocamento do protocolo anterior início do quadro.

</dd> <dt>

*ProtocolStatusCode* \[ fora\]
</dt> <dd>

Indicador de status de protocolo. A DLL do analisador deve definir um dos códigos de status a seguir.



| Valor                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**STATUS do protocolo \_ \_ reconhecido**</dt> </dl>              | O analisador reconhece os dados, mas não sabe qual protocolo segue. Depois de definir o código, retorne um ponteiro para os dados não reivindicados restantes que seguem o protocolo reconhecido. Monitor de Rede usa o [*conjunto de acompanhamento*](f.md) do protocolo para continuar a análise. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**STATUS do protocolo \_ \_ não \_ reconhecido**</dt> </dl> | O analisador não reconhece os dados. Depois de definir esse código, retorne o ponteiro para o início dos dados usando o ponteiro que o parâmetro *lpProtocol* passa para a DLL do analisador. Monitor de Rede usa o *conjunto de acompanhamento* do protocolo anterior para continuar a análise. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**STATUS do protocolo \_ \_ declarado**</dt> </dl>                       | O analisador reconhece os dados e declara os dados restantes. Depois de definir o código, retorne **nulo** para monitor de rede para encerrar a análise de um quadro. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**\_ \_ protocolo próximo do status do protocolo \_**</dt> </dl>    | O analisador reconhece os dados e sabe qual protocolo segue. Depois de definir o código, defina o parâmetro *phNextProtocol* e retorne um ponteiro para os dados não reivindicados restantes que seguem o protocolo reconhecido. Monitor de Rede continua analisando o quadro. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ fora\]
</dt> <dd>

Aponta para o identificador do próximo protocolo. Esse parâmetro é definido quando um protocolo identifica o protocolo que segue um protocolo. Para obter o identificador do próximo protocolo, chame a função [GetProtocolFromTable](getprotocolfromtable.md) .

</dd> <dt>

*lpInstData* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para os dados da instância do protocolo anterior.

Na saída, um ponteiro para os dados da instância para o protocolo atual. Os dados da instância não podem ter mais de um \_ PTR de comprimento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte após os dados do analisador reconhecido. Se o analisador alegar todos os dados restantes, o valor de retorno será **nulo**.

Se a função não for bem-sucedida, o valor de retorno será um ponteiro inicial que o parâmetro *lpProtocol* passa.

## <a name="remarks"></a>Comentários

A função **RecognizeFrame** determina se o analisador reconhece os dados brutos começando no ponteiro *lpProtocol* .

-   Se o protocolo reconhecer os dados, a função **RecognizeFrame** retornará um ponteiro para os dados restantes ou retornará **NULL** se o protocolo atual for o último protocolo em um quadro.
-   Se o protocolo não reconhecer os dados, a função **RecognizeFrame** retornará o ponteiro passado para a DLL do analisador no parâmetro *lpProtocol* .

> [!Note]  
> *RecognizeFrame* pode ser chamado antes que a função [*Register*](register-parser.md) seja chamada para registrar as propriedades de protocolo. Por esse motivo, a implementação da função *RecognizeFrame* não depende de propriedades ou estruturas criadas ou inicializadas durante a implementação da função de **registro** de protocolo.

 

**Conjunto de entrega e conjunto de acompanhamento**

Um analisador pode usar um conjunto de entrega ou seguir definido para identificar para Monitor de Rede o protocolo que segue os dados reconhecidos.

-   Se as informações estiverem disponíveis nos dados reconhecidos, o analisador usará sua entrega definida para obter um identificador para o próximo protocolo e, em seguida, passará esse identificador para Monitor de Rede.
-   Se as informações não estiverem disponíveis, o analisador não passará por um identificador e Monitor de Rede usará o conjunto de acompanhamento do analisador para determinar o protocolo a seguir.

**Passando informações entre protocolos**

Use o parâmetro *lpInstData* para passar informações entre protocolos. Na entrada, você pode recuperar as informações do protocolo anterior. Na saída, você pode passar informações para o próximo protocolo.

Os dados da instância podem ser quaisquer dados que sejam menores ou iguais a um \_ PTR de comprimento, ou um ponteiro para dados, como dados de quadro brutos, que não precisam ser alocados pelo analisador ou liberados pelo parser.



| Para obter informações sobre                                        | Consulte                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Quais analisadores são e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                                                                                    |
| Quais pontos de entrada são incluídos na DLL do analisador.        | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                                                                    |
| Como implementar **RecognizeFrame**  inclui um exemplo. | [Implementando RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Como especificar um conjunto de entrega e seguir o conjunto.              | [Especificando um conjunto de entrega](specifying-a-handoff-set.md)[especificando um conjunto de acompanhamento](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 




