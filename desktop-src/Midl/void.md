---
title: atributo void
description: O tipo base void indica um procedimento sem argumentos ou um procedimento que não retorna um valor de resultado.
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
ms.openlocfilehash: 7ad758ba334114e13493e7b082f45f37dc6e68efba16dc3a55f14fa57a772d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382432"
---
# <a name="void-attribute"></a>atributo void

O tipo base **void** indica um procedimento sem argumentos ou um procedimento que não retorna um valor de resultado.

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

*Nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*parameter-list* 
</dt> <dd>

Especifica a lista de parâmetros passados para a função junto com os tipos de parâmetro e atributos de parâmetro associados.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o nome do tipo retornado pela função.

</dd> <dt>

*context-handle-type* 
</dt> <dd>

Especifica o nome do tipo que aceita o atributo **\[** [**de \_ identificador de**](context-handle.md) **\]** contexto.

</dd> </dl>

## <a name="remarks"></a>Comentários

O tipo de ponteiro void _, que em C descreve um ponteiro genérico que pode ser lançado para representar qualquer tipo de ponteiro, é limitado em MIDL ao seu uso com a palavra-chave **\* *_* \[ context \_ handle. \]**

## <a name="examples"></a>Exemplos

``` syntax
void VoidFunc1(void); 
HRESULT VoidFunc2([in, out] short s1); 
typedef [context_handle] void * MY_CX_HNDL_TYPE; 
HRESULT InitHandle([out] MY_CX_HNDL_TYPE * ppCxHndl);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**alça de \_ contexto**](context-handle.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> </dl>

 

 




