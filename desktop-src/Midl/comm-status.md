---
title: comm_status atributo
description: O atributo \ status de \ Comm \_ \ ACF faz com que um código de erro seja retornado quando ocorre um erro de comunicação durante a execução de uma função.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status do atributo MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719f66d6849a21d67d9349a9e9fd728defb4a0663e4436701d06f20209f4d5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384688"
---
# <a name="comm_status-attribute"></a>atributo de status de comunicação \_

O atributo ACF de **\[ \_ status \] de comunicação** faz com que um código de erro seja retornado quando ocorre um erro de comunicação durante a execução de uma função.

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ACF-função-atributos* 
</dt> <dd>

Especifica zero ou mais atributos de função de ACF, como **\[ \_ status \] de comunicação** e **\[** [**Nocode**](nocode.md) **\]** . Os atributos de função são colocados entre colchetes. Zero ou mais atributos podem ser aplicados a uma função. Separe vários atributos de função com vírgulas. Observe que, se o **\[ \_ status \] de comunicação** aparecer como um atributo de função, ele também não poderá aparecer como um atributo de parâmetro.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parâmetros-atributos* 
</dt> <dd>

Especifica os atributos que se aplicam a um parâmetro. Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro. Separe vários atributos de parâmetro com vírgulas. Os atributos de parâmetro são colocados entre colchetes. Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF. Observe que, se o **\[ \_ status \] de comunicação** aparecer como um atributo de parâmetro, ele também não poderá aparecer como um atributo de função.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o parâmetro para a função, conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo de **\[ \_ status \] de comunicação** pode ser usado como um atributo de função ou como um atributo de parâmetro, mas pode aparecer apenas uma vez por função. Ele pode ser aplicado à função ou a um parâmetro em cada função.

O atributo de **\[ \_ status \] de comm** pode ser aplicado somente a funções que retornam o tipo status de [**erro \_ \_ t**](error-status-t.md). Quando ocorre um erro de comunicação durante a execução da função, um código de erro é retornado.

Quando o **\[ \_ status \] de comunicação** é usado como um atributo de parâmetro, o parâmetro deve ser definido no arquivo IDL e deve ser um **\[** parâmetro [**out**](out-idl.md) **\]** do tipo [**status de erro \_ \_ t**](error-status-t.md). Quando ocorre um erro de comunicação durante a execução da função, o parâmetro é definido como o código de erro. Quando a chamada remota for concluída com êxito, o procedimento definirá o valor.

É possível que os atributos **\[ \_ \] status de comunicação** e **\[** [**\_ status de falha**](fault-status.md) sejam **\]** exibidos em uma única função, como atributos de função ou atributos de parâmetro. Se ambos os atributos forem atributos de função ou se se aplicarem ao mesmo parâmetro e nenhum erro ocorrer, a função ou o parâmetro terá o valor **status de erro \_ \_ OK**. Caso contrário, ele conterá o valor de status de **\[ comunicação \_ \]** ou de **\[ \_ estado \] de falha** apropriado. Como os valores retornados para o **\[ \_ status \] de comunicação** são diferentes dos valores retornados para o **\[ \_ status \] de falha**, os valores retornados são prontamente interpretados.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**status de erro \_ \_ t**](error-status-t.md)
</dt> <dt>

[**status de falha \_**](fault-status.md)
</dt> <dt>

[**Nocode**](nocode.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> </dl>

 

 




