---
title: fault_status atributo
description: O atributo \ \_ status de falha \ ACF especifica que um código de erro de tipo status de erro \_ \_ t indica uma falha do procedimento remoto, em vez de outros tipos de problemas, como erros de comunicação.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status do atributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638427"
---
# <a name="fault_status-attribute"></a>atributo de status de falha \_

O atributo ACF de **\[ \_ status \] de falha** especifica que um código de erro de tipo status de [**erro \_ \_ t**](error-status-t.md) indica uma falha do procedimento remoto, em vez de outros tipos de problemas, como erros de comunicação.

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

*ACF-função-atributos* 
</dt> <dd>

Especifica zero ou mais atributos de função de ACF, como **\[ \_ status \] de falha** e **\[** [**Nocode**](nocode.md) **\]** . Os atributos de função são colocados entre colchetes. Observe que zero ou mais atributos podem ser aplicados a uma função. Separe vários atributos de função com vírgulas. Observe também que, se o **\[ \_ status \] de falha** aparecer como um atributo de função, ele também não poderá aparecer como um atributo de parâmetro.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parâmetros-atributos* 
</dt> <dd>

Especifica os atributos que se aplicam a um parâmetro. Observe que zero ou mais atributos podem ser aplicados ao parâmetro. Os atributos de parâmetro são colocados entre colchetes. Separe vários atributos de parâmetro com vírgulas. Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF. Observe que, se o **\[ \_ status \] de falha** aparecer como um atributo de parâmetro, ele também não poderá aparecer como um atributo de função.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o parâmetro para a função, conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ \_ status \] de falha** pode ser usado como um atributo de função ou como um atributo de parâmetro, mas pode aparecer apenas uma vez por função. Ele pode ser aplicado à própria função ou a um parâmetro em cada função.

O atributo **\[ \_ status \] de falha** pode ser aplicado somente a funções que retornam o tipo status de [**erro \_ \_ t**](error-status-t.md). Quando o procedimento remoto falha de forma que faz com que uma PDU de falha seja retornada, um código de erro é retornado.

Quando o **\[ \_ status \] de falha** é usado como um atributo de parâmetro, o parâmetro deve ser um **\[** parâmetro [**out**](out-idl.md) **\]** do tipo [**status de erro \_ \_ t**](error-status-t.md). Se ocorrer um erro de servidor, o parâmetro será definido como o código de erro. Quando a chamada remota for concluída com êxito, o procedimento definirá o valor.

O parâmetro associado ao atributo **\[ \_ status \] de falha** não precisa ser especificado no arquivo IDL. Quando o parâmetro não é especificado, um novo parâmetro [**out**](out-idl.md) do tipo [**status de erro \_ \_ t**](error-status-t.md) é gerado após o último parâmetro definido no arquivo IDL do DCE.

É possível que os atributos **\[ \_ \] status de falha** e **\[** [**\_ status de comunicação**](comm-status.md) **\]** apareçam em uma única função, seja como atributos de função ou atributos de parâmetro. Se ambos os atributos forem atributos de função ou se se aplicarem ao mesmo parâmetro e nenhum erro ocorrer, a função ou o parâmetro terá o valor **status de erro \_ \_ OK**. Caso contrário, ele contém o valor de código de status apropriado. Como os valores retornados para o **\[ \_ status \] de falha** são diferentes dos valores retornados para o **\[ \_ status \] de comunicação**, os valores retornados são prontamente interpretados.

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**status de comunicação \_**](comm-status.md)
</dt> <dt>

[**status de erro \_ \_ t**](error-status-t.md)
</dt> <dt>

[**Nocode**](nocode.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> </dl>

 

 




