---
title: error_status_t atributo
description: A \_ palavra-chave error status \_ t designa um tipo para um objeto que contém informações de status de comunicação ou status de falha.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t atributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02e404992e8fca98eba41f5ea85571160582827816a945d7ab8db505b28ba0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067266"
---
# <a name="error_status_t-attribute"></a>atributo \_ t de status de \_ erro

A **\_ palavra-chave error status \_ t** designa um tipo para um objeto que contém informações de status de comunicação ou status de falha.

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ACF-function-attributes* 
</dt> <dd>

Especifica zero ou mais atributos de função ACF, como **\[** [**status de \_ vírgula, status**](comm-status.md)de **\]** **\[** [**\_ falha**](fault-status.md) **\]** ou **\[** [**nocode.**](nocode.md) **\]** Os atributos de função são incluídos entre colchetes. Zero ou mais atributos podem ser aplicados a uma função. Separe vários atributos de função com vírgulas.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Especifica atributos que se aplicam a um parâmetro. Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro . Separe vários atributos de parâmetro com vírgulas. Os atributos de parâmetro são incluídos entre colchetes. Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Especifica o parâmetro para a função conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **tipo \_ \_ t de status** de erro é usado como parte da arquitetura de tratamento de exceção em IDL. Esse tipo é mapeado para [**um long sem assinatura.**](unsigned.md) [](long.md) Os aplicativos que capturam situações de erro têm um parâmetro out ou um tipo de retorno de um procedimento especificado como status de erro t e qualificam o status de erro t com o status da vírgula ou atributos de status de falha **\[** [](out-idl.md) **\]** no **\_ \_** **\_ \_** **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** ACF. Se o parâmetro ou o tipo de retorno não tiver sido qualificado com os atributos **\[ \_ de status \]** de vírgula ou **\[ \_ status \]** de falha, o parâmetro operará como se fosse um longo sem assinatura.

A partir da versão 2.0, o compilador MIDL gera stubs que contêm a arquitetura de tratamento de erros adequada. No entanto, as versões anteriores do compilador MIDL manipulavam um parâmetro ou retornavam o tipo de status de erro **\_ \_ t** como se os atributos de status de vírgula e status de falha fossem aplicados, mesmo que não **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** fossem. Com MIDL 2.0 ou posterior, você deve aplicar explicitamente os atributos **\[ \_ status \]** de vírgula e **\[ \_ status \]** de falha ao parâmetro ou procedimento no ACF.

O **tipo \_ \_ t de status** de erro é um dos tipos predefinidos da linguagem de definição de interface. Tipos predefinidos podem aparecer como especificadores de tipo em declarações [**typedef,**](typedef.md) em declarações gerais e em declaradores de função (como o tipo de retorno de função ou como especificadores de tipo de parâmetro).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**status do \_ comm**](comm-status.md)
</dt> <dt>

[**status \_ de falha**](fault-status.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




