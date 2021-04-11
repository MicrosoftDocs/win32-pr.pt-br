---
title: error_status_t atributo
description: A \_ \_ palavra-chave status de erro t designa um tipo para um objeto que contém informações de status de comunicação ou de status de falha.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t do atributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293085"
---
# <a name="error_status_t-attribute"></a>\_atributo t de status de erro \_

A palavra-chave **status de erro \_ \_ t** designa um tipo para um objeto que contém informações de status de comunicação ou de status de falha.

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

*ACF-função-atributos* 
</dt> <dd>

Especifica zero ou mais atributos de função de ACF, como **\[** [**\_ status de comunicação**](comm-status.md) **\]** , **\[** [**\_ status de falha**](fault-status.md) **\]** ou **\[** [**Nocode**](nocode.md) **\]** . Os atributos de função são colocados entre colchetes. Zero ou mais atributos podem ser aplicados a uma função. Separe vários atributos de função com vírgulas.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função, conforme definido no arquivo IDL.

</dd> <dt>

*ACF-parâmetros-atributos* 
</dt> <dd>

Especifica os atributos que se aplicam a um parâmetro. Observe que zero, um ou mais atributos podem ser aplicados ao parâmetro. Separe vários atributos de parâmetro com vírgulas. Os atributos de parâmetro são colocados entre colchetes. Atributos de parâmetro IDL, como atributos direcionais, não são permitidos no ACF.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o parâmetro para a função, conforme definido no arquivo IDL. Cada parâmetro para a função deve ser especificado na mesma sequência, usando o mesmo nome definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **tipo \_ \_ t de status de erro** é usado como parte da arquitetura de tratamento de exceção em IDL. Esse tipo é mapeado para um [**longo**](long.md) [**não assinado**](unsigned.md) . Os aplicativos que capturam situações de erro têm um **\[** parâmetro [**out**](out-idl.md) **\]** ou um tipo de retorno de um procedimento especificado como **status de erro \_ \_ t** e qualificam o **status de erro \_ \_ t** com os **\[** atributos [**\_ status de comunicação**](comm-status.md) **\]** ou **\[** [**\_ status de falha**](fault-status.md) **\]** no ACF. Se o parâmetro ou tipo de retorno não tiver sido qualificado com os atributos **\[ \_ status \] de comunicação** ou **\[ \_ status \] de falha** , o parâmetro funcionará como se fosse um longo não assinado.

A partir da versão 2,0, o compilador MIDL gera stubs que contêm a arquitetura de tratamento de erros apropriada. No entanto, as versões anteriores do compilador MIDL trataram um parâmetro ou um tipo de retorno de **status de erro \_ \_ t** , como se os atributos status de **\[** [**comunicação \_**](comm-status.md) **\]** e **\[** [**\_ status de falha**](fault-status.md) **\]** fossem aplicados, mesmo que eles não fossem. Com o MIDL 2,0 ou posterior, você deve aplicar explicitamente os atributos **\[ \_ status \] de comunicação** e **\[ \_ status \] de falha** ao parâmetro ou procedimento no ACF.

O tipo de **status de erro \_ \_ t** é um dos tipos predefinidos da linguagem de definição de interface. Tipos predefinidos podem aparecer como especificadores de tipo em declarações de [**typedef**](typedef.md) , em declarações gerais e em declaradores de função (como o tipo de retorno de função ou como especificadores de tipo de parâmetro).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**status de comunicação \_**](comm-status.md)
</dt> <dt>

[**status de falha \_**](fault-status.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Longas**](long.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**não assinados**](unsigned.md)
</dt> </dl>

 

 




