---
title: user_marshal atributo
description: O atributo de ACF do Marshal do usuário \_ associa um tipo de local nomeado no idioma de destino (tipo de usuário) a um tipo de transferência (tipo de fio) que é transferido entre o cliente e o servidor.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal do atributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293947"
---
# <a name="user_marshal-attribute"></a>\_atributo de marshaling do usuário

O atributo de ACF do **\_ Marshal do usuário** associa um tipo de local nomeado no idioma de destino (*tipo de usuário*) a um tipo de transferência (*tipo de fio*) que é transferido entre o cliente e o servidor.

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de usuário* 
</dt> <dd>

Especifica o identificador do tipo de dados do usuário a ser empacotado. O *tipo User-Type* não precisa ser transmititable e não precisa ser um tipo conhecido pelo compilador MIDL.

</dd> <dt>

*tipo de fio* 
</dt> <dd>

Especifica o tipo de dados de transferência nomeado que é realmente transferido entre o cliente e o servidor. O tipo de conexão deve ser um tipo base de MIDL, um tipo predefinido ou um identificador de tipo de um tipo que pode ser transmitido pela rede.

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

Especifica um ponteiro para um objeto de *\_ tipo de usuário*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica o ponteiro do buffer atual.

</dd> </dl>

## <a name="remarks"></a>Comentários

Cada tipo de local nomeado, *User-Type*, tem uma correspondência um-para-um com um *tipo de conexão* que define a representação de transmissão do tipo. Você deve fornecer rotinas para dimensionar os dados para marshaling, para realizar marshaling e desempacotamento dos dados e para liberar memória. Para obter mais informações sobre essas rotinas, consulte [o \_ atributo Marshal do usuário](/windows/desktop/Rpc/the-user-marshal-attribute). Observe que, se houver tipos inseridos em seus dados que também são definidos com marshaling do **usuário \_** ou \[ [**\[ \_ \] marshaling de conexão**](wire-marshal.md), você precisará gerenciar a manutenção desses tipos inseridos também.

O *tipo de conexão* não pode ser um ponteiro de interface nem um ponteiro completo. O *tipo de conexão* deve ter um tamanho de memória bem definido. Consulte marshaling [Rules for User Marshal \_ and wire \_ Marshal](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) para obter detalhes sobre como realizar marshaling de um determinado *tipo de cabo*.

O *tipo de usuário* não deve ser um ponteiro de interface, pois eles podem ser empacotados diretamente. Se o tipo de usuário for um ponteiro completo, você mesmo precisará gerenciar o alias.

## <a name="examples"></a>Exemplos

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> <dt>

[O \_ atributo de marshaling do usuário](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**\_marshaling de transmissão**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 