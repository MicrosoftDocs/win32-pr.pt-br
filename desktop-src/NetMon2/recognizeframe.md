---
description: A função de exportação RecognizeFrame indica se uma parte dos dados é reconhecida como o protocolo detectado pelo analisador. A função de exportação RecognizeFrame deve ser implementada para cada analisador compatível com a DLL do analisador.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Função de retorno de chamada RecognizeFrame (Netmon.h)
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
ms.openlocfilehash: b9f8fcbfccdb306038b7b654e947ff1a11654267012c7527799d8633ed8a9410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889696"
---
# <a name="recognizeframe-callback-function"></a>Função de retorno de chamada RecognizeFrame

A função de exportação **RecognizeFrame** indica se uma parte dos dados é reconhecida como o protocolo detectado pelo analisador. A função de exportação **RecognizeFrame** deve ser implementada para cada analisador compatível com a DLL do analisador.

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

*hFrame* \[ Em\]
</dt> <dd>

Lidar com o quadro que contém os dados.

</dd> <dt>

*lpFrame* \[ Em\]
</dt> <dd>

Ponteiro para o primeiro byte de um quadro. O ponteiro fornece uma maneira de exibir dados que outros analisadores reconhecem.

</dd> <dt>

*lpProtocol* \[ Em\]
</dt> <dd>

Ponteiro para o início dos dados não confirmados. Normalmente, os dados não reivindicados estão localizados no meio de um quadro porque um analisador anterior reivindicou dados antes desse analisador. O analisador deve testar os dados não confirmados primeiro.

</dd> <dt>

*MacType* \[ Em\]
</dt> <dd>

Valor MAC do primeiro protocolo em um quadro. Normalmente, o *valor macType* é usado quando o analisador deve identificar o primeiro protocolo em um quadro. O *valor macType* pode ser um dos seguintes:



| Valor                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**ETHERNET \_ DE TIPO \_ MAC**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**TOKENRING \_ DE \_ TIPO MAC**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_FDDI DE \_ TIPO MAC**</dt> </dl>                | ANSI X3T9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ Em\]
</dt> <dd>

O número restante de bytes de um local em um quadro até o final do quadro.

</dd> <dt>

*hPreviousProtocol* \[ Em\]
</dt> <dd>

Lidar com o protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ Em\]
</dt> <dd>

Deslocamento do início do protocolo anterior do quadro.

</dd> <dt>

*ProtocolStatusCode* \[ out\]
</dt> <dd>

Indicador de status do protocolo. A DLL do analisador deve definir um dos seguintes códigos de status.



| Valor                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**STATUS \_ DO PROTOCOLO \_ RECONHECIDO**</dt> </dl>              | O analisador reconhece os dados, mas não sabe qual protocolo segue. Depois de definir o código, retorne um ponteiro para os dados não confirmados restantes que seguem o protocolo reconhecido. Monitor de Rede usa o [*conjunto a seguir*](f.md) do protocolo para continuar a análise. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**STATUS \_ DO PROTOCOLO NÃO \_ \_ RECONHECIDO**</dt> </dl> | O analisador não reconhece os dados. Depois de definir esse código, retorne o ponteiro para o início dos dados usando o ponteiro que o *parâmetro lpProtocol* passa para a DLL do analisador. Monitor de Rede usa o *conjunto a seguir* do protocolo anterior para continuar a análise. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**STATUS \_ DO \_ PROTOCOLO REIVINDICADO**</dt> </dl>                       | O analisador reconhece os dados e declara os dados restantes. Depois de definir o código, retorne **NULL** Monitor de Rede para encerrar a análise de um quadro. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**PROTOCOLO \_ STATUS \_ NEXT \_ PROTOCOL**</dt> </dl>    | O analisador reconhece os dados e sabe qual protocolo segue. Depois de definir o código, de definir o parâmetro *phNextProtocol* e retornar um ponteiro para os dados não confirmados restantes que seguem o protocolo reconhecido. Monitor de Rede continua a análise do quadro. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ out\]
</dt> <dd>

Ponteiro para o alça do próximo protocolo. Esse parâmetro é definido quando um protocolo identifica o protocolo que segue um protocolo. Para obter o handle do próximo protocolo, chame a [função GetProtocolFromTable.](getprotocolfromtable.md)

</dd> <dt>

*lpInstData* \[ in, out\]
</dt> <dd>

Na entrada, um ponteiro para os dados da instância do protocolo anterior.

Na saída, um ponteiro para os dados da instância para o protocolo atual. Os dados da instância não podem ter mais tempo do que um \_ PTR DWORD de comprimento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um ponteiro para o primeiro byte após os dados do analisador reconhecidos. Se o analisador reivindicar todos os dados restantes, o valor de retorno será **NULL.**

Se a função não for bem-sucedida, o valor de retorno será um ponteiro inicial que o *parâmetro lpProtocol* passa.

## <a name="remarks"></a>Comentários

A **função RecognizeFrame** determina se o analisador reconhece os dados brutos começando no *ponteiro lpProtocol.*

-   Se o protocolo reconhecer os dados, a **função RecognizeFrame** retornará um ponteiro para os dados restantes ou retornará **NULL** se o protocolo atual for o último protocolo em um quadro.
-   Se o protocolo não reconhecer os dados, a **função RecognizeFrame** retornará o ponteiro passado para a DLL do analisador no *parâmetro lpProtocol.*

> [!Note]  
> *RecognizeFrame* pode ser chamado antes que [*a função Register*](register-parser.md) seja chamada para registrar as propriedades do protocolo. Por esse motivo, a implementação da função *RecognizeFrame* não depende de nenhuma propriedade ou estrutura criada ou inicializada durante a implementação da função **De registro de** protocolo.

 

**Conjunto de entrega e acompanhamento de conjunto**

Um analisador pode usar um conjunto de entrega ou seguir o conjunto para identificar Monitor de Rede o protocolo que segue os dados reconhecidos.

-   Se as informações estão disponíveis em dados reconhecidos, o analisador usa seu conjunto de entrega para obter um handle para o próximo protocolo e, em seguida, passa esse alça para Monitor de Rede.
-   Se as informações não estão disponíveis, o analisador não passa um handle e Monitor de Rede usa o conjunto de acompanhamento do analisador para determinar qual protocolo segue.

**Passando informações entre protocolos**

Use o *parâmetro lpInstData* para passar informações entre protocolos. Na entrada, você pode recuperar as informações do protocolo anterior. Na saída, você pode passar informações para o próximo protocolo.

Os dados da instância podem ser dados menores ou iguais a um PTR DWORD de comprimento ou um ponteiro para dados, como dados brutos do quadro, que não precisam ser alocados nem liberados pelo \_ analisador.



| Para obter informações sobre                                        | Consulte                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| O que são analisadores e como eles funcionam com Monitor de Rede. | [Analisadores](parsers.md)                                                                                                    |
| Quais pontos de entrada estão incluídos na DLL do analisador.        | [Arquitetura de DLL do analisador](parser-dll-architecture.md)                                                                    |
| Como implementar **o RecognizeFrame**  inclui um exemplo. | [Implementando RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Como especificar um conjunto de entrega e seguir o conjunto.              | [Especificando um conjunto de entrega especificando](specifying-a-handoff-set.md)[um conjunto a seguir](specifying-a-follow-set.md)<br/> |



 

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

 

 




