---
title: anotar atributo
description: O atributo \ anotar \ permite que você especifique uma cadeia de caracteres de anotação SAL para o método, o parâmetro ou o campo de estrutura especificado.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- atributo de anotação MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642296"
---
# <a name="annotate-attribute"></a>anotar atributo

O atributo **\[ anotar \]** permite que você especifique uma cadeia de caracteres de anotação sal para o método, o parâmetro ou o campo de estrutura especificado.

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cadeia de caracteres* 
</dt> <dd>

Cadeia de caracteres de anotação SAL especificada.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos incluem [**\[ \] retorno de chamada**](callback.md); os atributos de ponteiro [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e a cadeia de [**\[ caracteres \]**](string.md)de atributos de uso, [**\[ ignore \]**](ignore.md)e o [**\[ \_ identificador \] de contexto**](context-handle.md). Vários atributos devem ser separados por vírgulas.

</dd> <dt>

*função-declaradora* 
</dt> <dd>

Especifica o especificador de tipo, o nome da função e a lista de parâmetros para a função.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo de **base \_**, [**\[ struct \]**](struct.md), [**Union**](union.md)ou tipo de [**\[ enumeração \]**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador de ponteiro* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que um Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**\[ const \]**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Especifica zero ou mais atributos apropriados para o tipo de parâmetro. Atributos de parâmetro com o atributo [**\[ \] in**](in.md) também podem pegar o atributo direcional [**\[ out \]**](out-idl.md); os atributos de campo [**\[ First \_ são \]**](first-is.md), [**\[ Last \_ is \]**](last-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ Max \_ is \]**](max-is.md), [**\[ Size \_ is \]**](size-is.md)e [**\[ switch \_ Type \]**](switch-type.md); os atributos pointer [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)ou [**\[ PTR \]**](ptr.md); e o [**\[ \_ identificador \] de contexto**](context-handle.md) e a [**\[ cadeia \] de caracteres**](string.md)de atributos de uso. O atributo de uso [**\[ ignore \]**](ignore.md) não pode ser usado como um atributo de parâmetro. Vários atributos devem ser separados por vírgulas.

</dd> <dt>

*Declarador* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**\[ matrizes \]**](../rpc/arrays.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ anotar \]** permite substituir anotações sal geradas por MIDL ou adicioná-las em locais onde o MIDL não gera uma anotação explicitamente. Se [**/sal**](-sal.md) não for especificado na linha de comando, esse atributo será ignorado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**/sal \_ local**](-sal-local.md)
</dt> </dl>

 

 