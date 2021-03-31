---
title: implicit_handle atributo
description: O atributo \ \_ identificador \ implícito \ ACF especifica o identificador usado para funções que não incluem um identificador explícito como um parâmetro de procedimento.
ms.assetid: 09c17473-87b5-4fd6-beb9-3d9b7bc82d8c
keywords:
- implicit_handle do atributo MIDL
topic_type:
- apiref
api_name:
- implicit_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f410fa048a27e1f7626690e6308de4c1a31c2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823174"
---
# <a name="implicit_handle-attribute"></a>\_atributo de identificador implícito

O atributo de ACF **\[ \_ identificador \] implícito** especifica o identificador usado para funções que não incluem um identificador explícito como um parâmetro de procedimento.

``` syntax
implicit_handle(handle-type handle-name)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo de identificador* 
</dt> <dd>

Especifica o tipo de dados de identificador, como o tipo de base [**Handle \_ t**](handle-t.md) ou um tipo de identificador definido pelo usuário.

</dd> <dt>

*nome do identificador* 
</dt> <dd>

Especifica o nome do identificador.

</dd> </dl>

## <a name="remarks"></a>Comentários

O identificador especificado pelo atributo **\[ \_ identificador \] implícito** é usado de maneiras diferentes, dependendo da natureza do procedimento. Se o procedimento for remoto, o identificador será usado como o identificador de associação para a chamada remota. O identificador implícito também pode ser usado para estabelecer uma associação inicial para uma função que usa um identificador de contexto. Se o procedimento for um procedimento de serialização, o identificador será usado como um identificador de serialização que controla a operação. No caso do tipo serialização, o identificador é usado como o identificador de serialização para todos os tipos serializados.

O atributo **\[ \_ identificador \] implícito** especifica uma variável global que contém um identificador usado por qualquer função que precise de identificadores implícitos.

O tipo de identificador de associação implícita deve ser um [**identificador \_ t**](handle-t.md) (ou um tipo com base no **identificador \_ t**) ou um tipo de identificador definido pelo usuário especificado com o atributo [**Handle**](handle.md) . O identificador de serialização implícita deve ser um tipo com base no **identificador \_ t**.

Se o tipo de identificador implícito não estiver definido no arquivo IDL ou em todos os arquivos incluídos e importados pelo arquivo IDL para o computador MIDL, você deverá fornecer o arquivo que contém a definição de tipo de identificador ao compilar os stubs. Use a instrução ACF [**include**](include.md) para incluir o arquivo que contém a definição do tipo de identificador.

O atributo de **\[ \_ identificador \] implícito** pode ocorrer uma vez, no máximo. O atributo **\[ \_ identificador \] implícito** só poderá ocorrer [**\[ \_ \]**](auto-handle.md) se os atributos identificador automático e [**\[ \_ identificador \] explícito**](explicit-handle.md) não ocorrerem.

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

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**\_identificador explícito**](explicit-handle.md)
</dt> <dt>

[**lidar com \_ t**](handle-t.md)
</dt> <dt>

[**incluir**](include.md)
</dt> </dl>

 

 




