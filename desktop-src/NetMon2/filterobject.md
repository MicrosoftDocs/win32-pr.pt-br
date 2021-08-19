---
description: Define um único objeto de um filtro de exibição.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Estrutura FILTERobject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6a8da526eb60d8d581ca10e24f87a78b91492c4c043e6322eebe6a2ca0ebfd10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795779"
---
# <a name="filterobject-structure"></a>Estrutura de FILTERobject

A estrutura **filterobject** define um único objeto de um filtro de exibição. A função [**FilterAddObject**](filteraddobject.md) usa **filterobject** para criar um filtro de exibição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Ação**
</dt> <dd>

Sinalizador que especifica a ação de **filterobject** . Um sinalizador pode especificar uma propriedade, um valor ou um operador.

A tabela a seguir lista os sinalizadores de propriedade de membro de ação.



| Valor                                                                                                                                                                                                | Significado                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**Propriedade FILTERaction \_**</dt> </dl>                | Contém esta propriedade.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**FILTERaction \_ PROPERTYEXIST**</dt> </dl> | Indica que uma propriedade de ação de filtro já está definida.<br/> |



 

A tabela a seguir lista os sinalizadores de valor de membro da ação.



| Valor                                                                                                                                                                                        | Significado                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**valor de FILTERaction \_**</dt> </dl>                 | Contém esse valor.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**Cadeia de \_ caracteres filteraction**</dt> </dl>              | Contém esta cadeia de caracteres.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**matriz FILTERaction \_**</dt> </dl>                 | Contém esta matriz.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**FILTERaction \_ CONTAINSNC**</dt> </dl>  | Indica que uma propriedade contém uma subcadeia de caracteres que não diferencia maiúsculas de minúsculas.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**FILTERaction \_ contém**</dt> </dl>        | Indica que uma propriedade contém uma subcadeia de caracteres que diferencia maiúsculas de minúsculas.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**Endereço FILTERaction \_**</dt> </dl>           | Contém o endereço MAC.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**FILTERaction \_ ADDRESSANY**</dt> </dl>  | Corresponde a qualquer endereço MAC.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**FILTERaction \_ de**</dt> </dl>                    | Indica o endereço **Mac de** .<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**FILTERaction \_ para**</dt> </dl>                          | Indica o endereço **Mac a** .<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**FILTERaction \_ deto**</dt> </dl>              | Indica um emparelhamento de **/para** de endereços MAC.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**FILTERaction \_ LARGEINT**</dt> </dl>        | Contém um inteiro grande.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**tempo de FILTROaction \_**</dt> </dl>                    | Contém uma estrutura **SYSTEMTIME** .<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**FILTERaction \_ addr \_ ether**</dt> </dl> | Contém um endereço MAC Ethernet.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**TOKEN de endereço de FILTERaction \_ \_**</dt> </dl> | Contém um endereço MAC de token ring.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**o \_ endaction addr \_ FDDI**</dt> </dl>    | Contém um endereço MAC FDDI.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**FILTRAR \_ endereço \_ IPX**</dt> </dl>       | Contém um endereço MAC IPX.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**IP de endereço de FILTERaction \_ \_**</dt> </dl>          | Contém um endereço MAC IP.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**OID FILTERaction \_**</dt> </dl>                       | Contém um OID (identificador de objeto).<br/>                             |



 

A tabela a seguir lista os sinalizadores de operador de membro de ação.



| Valor                                                                                                                                                                                                        | Significado                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**FILTERaction \_ inválido**</dt> </dl>                           | Indica uma ação de filtro inválida.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERaction \_ e**</dt> </dl>                                       | Indica uma instrução **and** lógica.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERaction \_ ou**</dt> </dl>                                          | Indica uma instrução **or** lógica.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**XOR FILTERaction \_**</dt> </dl>                                       | Indica uma instrução or exclusiva lógica **or** (XOR).<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**FILTERaction \_ não**</dt> </dl>                                       | Indica uma instrução **not** lógica.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**FILTERaction \_ EQUALNC**</dt> </dl>                           | A ação do filtro é igual e não diferencia maiúsculas de minúsculas.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**FILTERaction \_ igual**</dt> </dl>                                 | A ação de filtro é igual e diferencia maiúsculas de minúsculas.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**FILTERaction \_ NOTEQUALNC**</dt> </dl>                  | A instrução not lógica é igual e **não** diferencia maiúsculas de minúsculas.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**FILTERaction não \_ igual**</dt> </dl>                        | A instrução **not** lógica é igual e diferencia maiúsculas de minúsculas.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**FILTERaction \_ GREATERNC**</dt> </dl>                     | A ação do filtro é maior que (>) e não diferencia maiúsculas de minúsculas.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**FILTERaction \_ maior**</dt> </dl>                           | A ação do filtro é maior que (>) e diferencia maiúsculas de minúsculas.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**FILTERaction \_ LESSNC**</dt> </dl>                              | A ação de filtro é menor que (<) e não diferencia maiúsculas de minúsculas.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**FILTERaction \_ menos**</dt> </dl>                                    | A ação de filtro é menor que (<) e diferencia maiúsculas de minúsculas.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**FILTERaction \_ GREATEREQUALNC**</dt> </dl>      | A ação do filtro é maior ou igual a (>=) e não diferencia maiúsculas de minúsculas.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**FILTERaction \_ GREATEREQUAL**</dt> </dl>            | A ação do filtro é maior ou igual a (>=) e diferencia maiúsculas de minúsculas.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**FILTERaction \_ LESSEQUALNC**</dt> </dl>               | A ação de filtro é menor ou igual a (<=) e não diferencia maiúsculas de minúsculas.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**FILTERaction \_ LESSEQUAL**</dt> </dl>                     | A ação de filtro é menor ou igual a (<=) e diferencia maiúsculas de minúsculas.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**FILTERaction \_ mais**</dt> </dl>                                    | Adicionar operador (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**FILTERaction \_ menos**</dt> </dl>                                 | Operador de subtração (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**FILTERaction \_ AREBITSON**</dt> </dl>                     | Indica uma operação bit-a-bit.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**FILTERaction \_ AREBITSOFF**</dt> </dl>                  | Indica uma operação não bit a bit.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLSEXIST**</dt> </dl>      | Indica que os protocolos selecionados existem.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**FILTERACTION \_ PROTOCOLEXIST**</dt> </dl>         | Indica que o protocolo selecionado existe.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**FILTERACTION \_ ARRAYEQUAL**</dt> </dl>                  | Indica que o conteúdo da matriz é igual. O sinalizador deve ser usado com uma **estrutura FILTERACTION \_ ARRAY.**<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**FILTERACTION \_ DEREFPROPERTY**</dt> </dl>         | Descreve uma combinação de padrões em um deslocamento (em bytes) do protocolo.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**FILTERACTION \_ OID \_ CONTAINS**</dt> </dl>           | Avalia uma substring dentro de um identificador de objeto. A ação deve ser usada com a **estrutura \_ OID FILTERACTION.**<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**FILTERACTION \_ OID \_ COMEÇA \_ COM**</dt> </dl> | Avalia uma substring que inicia um identificador de objeto. O sinalizador deve ser usado com **FILTERACTION \_ OID**.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**FILTERACTION \_ OID \_ TERMINA \_ COM**</dt> </dl>       | Avalia uma substring que encerra um identificador de objeto. O sinalizador deve ser usado com **FILTERACTION \_ OID**.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**VINES DO \_ ADDR FILTERACTION \_**</dt> </dl>                 | Contém um endereço MAC Vines.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**EXPRESSÃO \_ FILTERACTION**</dt> </dl>                  | Contém uma expressão de ação.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**FILTERACTION \_ BOOL**</dt> </dl>                                    | Contém um **tipo de dados BOOL.**<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**DIREÇÃO \_ DO FILTRO \_ PRÓXIMO**</dt> </dl>                       | Controla a direção sequencial (próximo quadro) dentro de um arquivo de captura.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**FILTER \_ DIRECTION \_ PREV**</dt> </dl>                       | Controla a direção sequencial (quadro anterior) em um arquivo de captura.<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

Lidar com uma chave de propriedade.

</dd> <dt>

**Valor**
</dt> <dd>

Valor de um objeto .

</dd> <dt>

**hProtocol**
</dt> <dd>

Manipular para exibir o protocolo de filtro.

</dd> <dt>

**Lparray**
</dt> <dd>

Ponteiro para uma matriz.

</dd> <dt>

**lpProtocolTable**
</dt> <dd>

Ponteiro para uma lista de protocolos projetada para testar a existência do protocolo em um quadro.

</dd> <dt>

**Lpaddress**
</dt> <dd>

Ponteiro para o endereço do tipo kernel. Por exemplo, MAC ou IP.

</dd> <dt>

**lpLargeInt**
</dt> <dd>

DWORD **duplo** usado em um Windows NT ou Windows 2000.

</dd> <dt>

**lpTime**
</dt> <dd>

Um ponteiro para uma **estrutura SYSTEMTIME.**

</dd> <dt>

**lpOID**
</dt> <dd>

Um ponteiro para a estrutura OID **(OBJECT \_ IDENTIFIER).**

</dd> <dt>

**ByteCount**
</dt> <dd>

O número, em bytes, no quadro.

</dd> <dt>

**ByteOffset**
</dt> <dd>

O valor de byte de deslocamento da estrutura FILTEROBJECT usada para comparar matrizes.

</dd> <dt>

**pNext**
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




