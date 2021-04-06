---
title: atributo de codificação
description: O atributo \ Encode \ ACF especifica que um procedimento ou um tipo de dados precisa de suporte de serialização.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- atributo de codificação MIDL
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917184"
---
# <a name="encode-attribute"></a>atributo de codificação

O atributo **\[ Encode \]** ACF especifica que um procedimento ou um tipo de dados precisa de suporte de serialização.

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica outros atributos que se aplicam à interface como um todo.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*interface-definição* 
</dt> <dd>

Especifica as instruções IDL que formam a definição da interface.

</dd> <dt>

*lista de atributos de op* 
</dt> <dd>

Especifica outros atributos operacionais que se aplicam ao procedimento como **\[** [**decodificar**](decode.md) **\]** .

</dd> <dt>

*proc-nome* 
</dt> <dd>

Especifica o nome do procedimento.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica outros atributos que se aplicam ao tipo, como **\[** [**decodificar**](decode.md) **\]** e **\[** [**alocar**](allocate.md) **\]** .

</dd> <dt>

*nome do tipo* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo de **\[ codificação \]** faz com que o compilador MIDL gere código que um aplicativo pode usar para serializar dados em um buffer. O **\[** atributo [**decodificar**](decode.md) **\]** gera o código para desempacotamento de dados de um buffer.

Use os atributos de **\[ codificação \]** e **\[** [**decodificação**](decode.md) **\]** em um ACF para gerar código de SERIALIZAÇÃO para procedimentos ou tipos definidos no arquivo IDL de uma interface. Quando usado como um atributo de interface, a **\[ codificação \]** se aplica a todos os tipos e procedimentos definidos no arquivo IDL. Quando usado como um atributo operacional, a **\[ codificação \]** se aplica somente ao procedimento especificado. Quando usado como um atributo de tipo, a **\[ codificação \]** se aplica somente ao tipo especificado.

Quando o atributo de **\[ \] codificação** ou **\[** [**decodificação**](decode.md) **\]** é aplicado a um procedimento, o compilador MIDL gera um stub de serialização de maneira semelhante à medida que os stubs remotos são gerados para rotinas remotas. Um procedimento pode ser um procedimento remoto ou de serialização, mas não pode ser ambos. O protótipo da rotina gerada é enviado para o STUB. O arquivo H, enquanto o próprio stub entra no \_ arquivo de stub c. c.

O compilador MIDL gera duas funções para cada tipo ao qual o atributo de **\[ codificação \]** se aplica e uma função adicional para cada tipo ao qual o atributo de **\[** [**decodificação**](decode.md) **\]** se aplica. Por exemplo, para um tipo definido pelo usuário chamado com MyType, o compilador gera código para as \_ funções com MyType Encode, com MyType \_ decodificar e com MyType \_ AlignSize. Para essas funções, o compilador grava protótipos no STUB. H e código-fonte para \_ C.C. de stub

Para obter informações adicionais sobre identificadores de serialização e codificação ou decodificação de dados, consulte [serviços de serialização](/windows/desktop/Rpc/serialization-services).

## <a name="examples"></a>Exemplos

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**aloca**](allocate.md)
</dt> <dt>

[**RET**](decode.md)
</dt> </dl>

 

 