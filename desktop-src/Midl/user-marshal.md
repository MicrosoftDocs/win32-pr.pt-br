---
title: user_marshal atributo
description: O atributo ACF de marshal do usuário associa um tipo local nomeado no idioma de destino (tipo userm) a um tipo de transferência (tipo de transmissão) que é transferido entre o cliente e o \_ servidor.
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal atributo MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f17b4ef9d4376309307403ee12e2c5aae507556beaf091f9d742998d18671a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105566"
---
# <a name="user_marshal-attribute"></a>atributo \_ de marshal de usuário

O atributo ACF de marshal do usuário associa um tipo local nomeado na linguagem de destino (*tipo userm*) a um tipo de transferência *(* tipo de transmissão ) que é transferido entre o cliente e o servidor. **\_**

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

*userm-type* 
</dt> <dd>

Especifica o identificador do tipo de dados do usuário a ser empacotado. O *tipo userm* não precisa ser transmitível e não precisa ser um tipo conhecido para o compilador MIDL.

</dd> <dt>

*tipo de transmissão* 
</dt> <dd>

Especifica o tipo de dados de transferência nomeado que é realmente transferido entre o cliente e o servidor. O tipo de transmissão deve ser um tipo base MIDL, um tipo predefinido ou um identificador de tipo de um tipo que pode ser transmitido pela rede.

</dd> <dt>

*pFlags* 
</dt> <dd>

Especifica um ponteiro para um campo de sinalizador ( [**long sem sinal).**](unsigned.md) [](long.md) A palavra de ordem alta especifica sinalizadores de representação de dados NDR conforme definido pela DCE para representação de caracteres, big ou little endian. A palavra de ordem baixa especifica um sinalizador de contexto de marshaling. O layout exato dos sinalizadores é descrito em [O tipo \_ Função UserSize](/windows/desktop/Rpc/the-type-usersize-function).

</dd> <dt>

*StartingSize* 
</dt> <dd>

Especifica o tamanho atual do buffer (deslocamento) antes de tamanho do objeto.

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

Especifica um ponteiro para um objeto do *tipo userm \_*.

</dd> <dt>

*Buffer* 
</dt> <dd>

Especifica o ponteiro de buffer atual.

</dd> </dl>

## <a name="remarks"></a>Comentários

Cada tipo local nomeado, *userm-type*, tem uma correspondência um-para-um com um tipo de transmissão que define a representação de transmissão do tipo.  Você deve fornecer rotinas para tamanho dos dados para marshaling, marshaling e unmarshal dos dados e para liberar memória. Para obter mais informações sobre essas rotinas, consulte [O atributo de marshal do \_ usuário](/windows/desktop/Rpc/the-user-marshal-attribute). Observe que, se **\_** \[ [**\[ \_ \]**](wire-marshal.md)houver tipos inseridos em seus dados que também são definidos com marshal de usuário ou marshal de transmissão, você também precisará gerenciar a manutenção desses tipos inseridos.

O *tipo de transmissão* não pode ser um ponteiro de interface ou um ponteiro completo. O *tipo de transmissão* deve ter um tamanho de memória bem definido. Consulte [Marshaling Rules for user marshal and wire \_ \_ marshal (Regras](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal) de marshaling de marshaling de usuário e marshaling de transmissão) para obter detalhes sobre como fazer marshaling de um determinado *tipo de transmissão.*

O *tipo userm* não deve ser um ponteiro de interface, pois eles podem ser empacotados diretamente. Se o tipo de usuário for um ponteiro completo, você deverá gerenciar o alias por conta própria.

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

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> <dt>

[O atributo \_ de marshal do usuário](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 