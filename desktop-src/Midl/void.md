---
title: atributo void
description: O tipo de base void indica um procedimento sem argumentos ou um procedimento que não retorna um valor de resultado.
ms.assetid: a3eebfe7-bf43-4bab-b87b-9188a54ab9bf
keywords:
- atributo void MIDL
topic_type:
- apiref
api_name:
- void
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b14a5ae4a2325f840d8a840cb0a1bc5283bb4a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105750831"
---
# <a name="void-attribute"></a>atributo void

O tipo de base **void** indica um procedimento sem argumentos ou um procedimento que não retorna um valor de resultado.

``` syntax
void function-name(parameter-list);

return-type function-name(void);

typedef [context_handle] void * context-handle-type;

return-type function-name(
    [context_handle] void * * context-handle-type
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Especifica a lista de parâmetros passados para a função junto com os tipos de parâmetro associados e atributos de parâmetro.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o nome do tipo retornado pela função.

</dd> <dt>

*tipo de identificador de contexto* 
</dt> <dd>

Especifica o nome do tipo que usa o atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> </dl>

## <a name="remarks"></a>Comentários

O tipo de **ponteiro \* void**, que em C descreve um ponteiro genérico que pode ser convertido para representar qualquer tipo de ponteiro, é limitado em MIDL para seu uso com a palavra-chave de **\[ \_ manipulador \] de contexto** .

## <a name="examples"></a>Exemplos

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




