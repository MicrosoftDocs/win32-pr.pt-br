---
title: fault_status atributo
description: O atributo \ status de falha\ ACF especifica que um código de erro do tipo status de erro t indica uma falha do procedimento remoto, em vez de outros tipos de problemas, como erros \_ \_ de \_ comunicação.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status atributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f5126c5ee089729089179fa99f881f1e236859e3111ed3937323eb8b122d2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013904"
---
# <a name="fault_status-attribute"></a>atributo \_ de status de falha

O atributo ACF de **\[ \_ status \]** de falha especifica que um código de erro do tipo status de [**erro \_ \_ t**](error-status-t.md) indica uma falha do procedimento remoto, em vez de outros tipos de problemas, como erros de comunicação.

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ACF-function-attributes* 
</dt> <dd>

Especifica zero ou mais atributos de função ACF, como **\[ status de \_ falha \]** e **\[** [**nocode.**](nocode.md) **\]** Os atributos de função são incluídos entre colchetes. Observe que zero ou mais atributos podem ser aplicados a uma função. Separe vários atributos de função com vírgulas. Observe também que, se **\[ o status \_ de \]** falha aparecer como um atributo de função, ele também não poderá aparecer como um atributo de parâmetro.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica atributos que se aplicam a um parâmetro. Observe que zero ou mais atributos podem ser aplicados ao parâmetro . Os atributos de parâmetro são incluídos entre colchetes. Separe vários atributos de parâmetro com vírgulas. Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF. Observe que, se **\[ o status \_ de \]** falha aparecer como um atributo de parâmetro, ele também não poderá aparecer como um atributo de função.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica o parâmetro para a função conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo de \_ status \]** de falha pode ser usado como um atributo de função ou como um atributo de parâmetro, mas pode aparecer apenas uma vez por função. Ele pode ser aplicado à própria função ou a um parâmetro em cada função.

O **\[ atributo de \_ \] status** de falha pode ser aplicado somente a funções que retornam o [**status de erro de tipo \_ \_ t**](error-status-t.md). Quando o procedimento remoto falha de uma maneira que faz com que uma PDU de falha seja retornada, um código de erro é retornado.

Quando **\[ o status \_ de \]** falha é usado como um atributo de parâmetro, o parâmetro deve ser um parâmetro de saída **\[** [](out-idl.md) **\]** do status de [**erro do tipo \_ \_ t**](error-status-t.md). Se ocorrer um erro de servidor, o parâmetro será definido como o código de erro. Quando a chamada remota for concluída com êxito, o procedimento define o valor.

O parâmetro associado ao atributo **\[ \_ de status \]** de falha não precisa ser especificado no arquivo IDL. Quando o parâmetro não é [](out-idl.md) especificado, um novo parâmetro de saída do tipo status de erro [**\_ \_ t**](error-status-t.md) é gerado após o último parâmetro definido no arquivo IDL de DCE.

É possível que os atributos status de **\[ \_ \] falha** e status de vírgula apareçam em uma única função, como atributos de função ou atributos **\[** [**\_**](comm-status.md) de **\]** parâmetro. Se ambos os atributos são atributos de função ou se eles se aplicam ao mesmo parâmetro e nenhum erro ocorre, a função ou o parâmetro tem o status de **\_ erro de valor \_ ok**. Caso contrário, ele conterá o valor de código de status apropriado. Como os valores **\[ retornados \_ para o status \]** de falha são diferentes dos valores retornados para o status de **\[ \_ vírgula, \]** os valores retornados são prontamente interpretados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**status do \_ comm**](comm-status.md)
</dt> <dt>

[**status \_ de \_ erro t**](error-status-t.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




