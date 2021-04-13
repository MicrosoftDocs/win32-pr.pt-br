---
title: Atributo wire_marshal
description: O atributo \ Wire \_ Marshal \ tem um tipo de dados que será usado para transmissão (o tipo de cabo) em vez de um tipo de dados específico do aplicativo (o tipo de usuário).
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal do atributo MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366840"
---
# <a name="wire_marshal-attribute"></a>\_atributo de marshaling de fio

O atributo de **\[ \_ marshaling \] de fio** especifica um tipo de dados que será usado para transmissão (o tipo de *cabo*) em vez de um tipo de dados específico do aplicativo (o *tipo de usuário*).

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de fio* 
</dt> <dd>

Especifica o tipo de dados de transferência nomeado que é realmente transferido entre o cliente e o servidor. O *tipo de conexão* deve ser um tipo base de MIDL, um tipo predefinido ou um identificador de tipo de um tipo que pode ser transmitido pela rede.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

O tipo para o qual o *tipo de usuário* se tornará um alias.

</dd> <dt>

*tipo de usuário* 
</dt> <dd>

Especifica o identificador do tipo de dados do usuário a ser empacotado. Ele pode ser qualquer tipo, conforme fornecido pelo *especificador de tipo*, desde que tenha um tamanho bem definido. O *tipo User-Type* não precisa ser transmititable, mas deve ser um tipo conhecido pelo compilador MIDL.

</dd> <dt>

*pFlags* 
</dt> <dd>

Especifica um ponteiro para um campo de sinalizador ( [**longo**](long.md) [**sem sinal**](unsigned.md) ). A palavra de ordem superior especifica sinalizadores de representação de dados de NDR, conforme definido pela DCE para ponto flutuante, Big ou little-endian e representação de caracteres. A palavra de ordem inferior Especifica um sinalizador de contexto de marshaling. O layout exato dos sinalizadores é descrito na [ \_ função tipo usersize](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Especifica o tamanho atual do buffer (deslocamento) antes de dimensionar o objeto.

</dd> <dt>

*tipo de pUser \_* 
</dt> <dd>

Especifica um ponteiro para um objeto de *tipo de usuário \_ .*

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica o ponteiro do buffer atual.

</dd> </dl>

## <a name="remarks"></a>Comentários

Cada tipo de dados específico do aplicativo, *tipo de usuário,* tem uma correspondência um-para-um com um *tipo de conexão* que define a representação de transmissão do tipo. Você deve fornecer rotinas para dimensionar os dados para marshaling, para realizar marshaling e desempacotamento dos dados e para liberar memória. Observe que, se houver tipos inseridos em seus dados que também são definidos com marshaling de **\[ conexão \_ \]** ou **\[** [**\_ marshaling do usuário**](user-marshal.md) **\]** , você precisará gerenciar a manutenção desses tipos inseridos também. Para obter mais informações sobre essas rotinas, consulte [o \_ atributo de marshaling de fio](/windows/desktop/Rpc/the-wire-marshal-attribute).

Sua implementação deve seguir as regras de Marshalling de acordo com a especificação uso-DCE. Detalhes sobre a sintaxe de transferência de NDR podem ser encontrados em [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) . Não é recomendável usar o **\[ \_ marshaling \] de conexão** se você não estiver familiarizado com o protocolo de conexão.

O *tipo de conexão* não pode ser um ponteiro de interface nem um ponteiro completo. O *tipo de conexão* deve ter um tamanho de memória bem definido. Consulte marshaling [Rules for User Marshal \_ and wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para obter detalhes sobre como realizar marshaling de um determinado *tipo de cabo*.

O *tipo de usuário* não deve ser um ponteiro de interface porque pode ser empacotado diretamente. Se o tipo de usuário for um ponteiro completo, você mesmo precisará gerenciar o alias.

Você não pode usar o atributo de **\[ \_ marshaling \] de fio** com o **\[** [](allocate.md) **\]** atributo Allocate, direta ou indiretamente, porque o mecanismo de NDR não controla a alocação de memória para o tipo transmitido.

## <a name="examples"></a>Exemplos

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[Representação de dados](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[O \_ atributo de marshaling de fio](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[**Marshal do usuário \_**](user-marshal.md)
</dt> </dl>

 

 