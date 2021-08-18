---
title: Atributo switch_type
description: O atributo \ switch \_ Type \ identifica o tipo da variável usada como discriminante de União. O tipo de opção pode ser um número inteiro, caractere, booliano ou tipo de enumeração.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- switch_type do atributo MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8695a17c60f9785d7782d77db839499306a9577755e8a6838540f5a0fc2cea48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146229"
---
# <a name="switch_type-attribute"></a>alterar \_ atributo de tipo

O atributo **\[ \_ tipo \] de comutador** identifica o tipo da variável usada como discriminante de União. O tipo de opção pode ser um número inteiro, caractere, booliano ou tipo de enumeração.

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*especificador de tipo de switch* 
</dt> <dd>

Especifica um tipo [**int**](int.md), [**Char**](char-idl.md), [**Boolean**](boolean.md)ou [**enum**](enum.md) ou um identificador desse tipo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Enquanto o atributo de **\[ \_ tipo \] de opção** identifica o tipo de variável, o **\[** atributo [**switch \_ é**](switch-is.md) **\]** especifica o nome do parâmetro que é o discriminante de União. O atributo de **\[ \_ tipo \] de comutador** se aplica a parâmetros ou membros de estruturas ou uniões.

A União e seu discriminante devem ser especificados no mesmo nível lógico. Quando Union é um parâmetro, o discriminante de União deve ser outro parâmetro. Quando Union é um campo de uma estrutura, discriminante deve ser outro campo da estrutura no mesmo nível que o campo Union.

## <a name="examples"></a>Exemplos

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Boolean**](boolean.md)
</dt> <dt>

[**char**](char-idl.md)
</dt> <dt>

[Uniões encapsuladas](encapsulated-unions.md)
</dt> <dt>

[**enumera**](enum.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[Uniões não encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**switch \_ é**](switch-is.md)
</dt> <dt>

[**unida**](union.md)
</dt> </dl>

 

 




