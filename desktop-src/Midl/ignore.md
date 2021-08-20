---
title: ignorar atributo
description: O atributo \ ignore \ designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não são transmitidos. O atributo \ ignore \ é restrito a membros de ponteiros de estruturas ou uniões.
ms.assetid: 9c2fc71a-4fac-4a59-95f5-2121067b326f
keywords:
- ignorar atributo MIDL
topic_type:
- apiref
api_name:
- ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6b7a1e70804bc3c9c277f3d46ac6a8ad20fc0f98b370f93fe9fd09b0b1bb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013854"
---
# <a name="ignore-attribute"></a>ignorar atributo

O atributo **\[ ignore \]** designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não são transmitidos. O atributo **\[ ignore \]** é restrito a membros de ponteiros de estruturas ou uniões.

``` syntax
[ignore] pointer-member-type pointer-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ponteiro-tipo de membro* 
</dt> <dd>

Especifica o tipo do membro de ponteiro da estrutura ou União.

</dd> <dt>

*nome do ponteiro* 
</dt> <dd>

Especifica o nome do membro do ponteiro que deve ser ignorado durante o marshaling.

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor de um membro de estrutura com o atributo **\[ ignore \]** é indefinido no destino. Um **\[** parâmetro [**in**](in.md) **\]** não está definido no computador remoto. Um **\[** parâmetro de [**saída**](out-idl.md) **\]** não está definido no computador local.

O atributo **\[ ignorar \]** permite que você impeça a transmissão de dados. Isso é útil em situações como uma lista de links duplos. O exemplo a seguir inclui uma lista vinculada dupla que apresenta o alias de dados:

``` syntax
/* IDL file */ 
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE; 
 
HRESULT remote_op([in] DBL_LINK_NODE_TYPE * list_head); 
 
/* application */ 
DBL_LINK_NODE_TYPE * p, * q 
 
p = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
q = (DBL_LINK_NODE_TYPE *) midl_user_allocate(
        sizeof(DBL_LINK_NODE_TYPE)); 
 
p->next = q;  
q->previous = p; 
p->previous = q->next = NULL; 
.. 
remote_op(p);
```

O alias ocorre no exemplo anterior porque a mesma área de memória está disponível de dois ponteiros diferentes na função **p** e **p->avançar >anterior**.

Observe que **\[ ignorar \]** não pode ser usado como um atributo de tipo.

## <a name="examples"></a>Exemplos

``` syntax
typedef struct _DBL_LINK_NODE_TYPE 
{ 
    long value; 
    struct _DBL_LINK_NODE_TYPE * next; 
    [ignore] struct _DBL_LINK_NODE_TYPE * previous; 
} DBL_LINK_NODE_TYPE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos de matriz e de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**matrizes**](arrays-1.md)
</dt> <dt>

[Matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 