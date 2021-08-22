---
title: implicit_handle atributo
description: O atributo \ implicit handle\ ACF especifica o handle usado para funções que não incluem um handle \_ explícito como um parâmetro de procedimento.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle atributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c53ded4c7459be8f0c8eb98f3770d88ff88a9b7da20cb3482c1032a4f74e96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013804"
---
# <a name="implicit_handle-attribute"></a>atributo de \_ alça implícita

O **\[ atributo \_ \]** ACF do handle implícito especifica o handle usado para funções que não incluem um handle explícito como um parâmetro de procedimento.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de identificador* 
</dt> <dd>

Especifica o tipo de dados handle, como o identificador de tipo base [**\_ t**](handle-t.md) ou um tipo de identificador definido pelo usuário.

</dd> <dt>

*handle-name* 
</dt> <dd>

Especifica o nome do alça.

</dd> </dl>

## <a name="remarks"></a>Comentários

O handle especificado pelo atributo **\[ de \_ alça \] implícita** é usado de maneiras diferentes, dependendo da natureza do procedimento. Se o procedimento for remoto, o handle será usado como o alça de associação para a chamada remota. O alça implícito também pode ser usado para estabelecer uma associação inicial para uma função que usa um alça de contexto. Se o procedimento for um procedimento de serialização, o handle será usado como um alça de serialização que controla a operação. No caso da serialização de tipo, o identificador é usado como o identificador de serialização para todos os tipos serializados.

O **\[ atributo de \_ handle \]** implícito especifica uma variável global que contém um handle usado por qualquer função que precise de alças implícitas.

O tipo de identificador de associação implícita deve ser identificador [**\_ t**](handle-t.md) (ou um tipo baseado no identificador **\_ t**) ou um tipo de identificador definido pelo usuário especificado com o [**atributo handle.**](handle.md) O identificador de serialização implícito deve ser um tipo baseado no **identificador \_ t**.

Se o tipo de identificador implícito não estiver definido no arquivo IDL ou em arquivos incluídos e importados pelo arquivo IDL para o computador MIDL, você deverá fornecer o arquivo que contém a definição de tipo de identificador ao compilar os stubs. Use a instrução ACF [**include**](include.md) para incluir o arquivo que contém a definição de tipo de identificador.

O **\[ atributo de \_ alça \]** implícita pode ocorrer uma vez, no máximo. O **\[ atributo de \_ \] handle** implícito poderá ocorrer [**\[ \_ \]**](auto-handle.md) somente se os atributos de alça automática e [**\[ de \_ alça \]**](explicit-handle.md) explícita não ocorrerem.

## <a name="examples"></a>Exemplos

``` syntax
/* ACF file */ 
[
    implicit_handle(handle_t hMyHandle)
] 
interface iface
{ 
    // Attribute configuration statements
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**auto \_ handle**](auto-handle.md)
</dt> <dt>

[**alça \_ explícita**](explicit-handle.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Incluem**](include.md)
</dt> </dl>

 

 




