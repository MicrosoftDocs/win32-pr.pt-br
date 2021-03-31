---
title: atributo in
description: O atributo \ in \ indica que um parâmetro deve ser passado do procedimento de chamada para o procedimento chamado.
ms.assetid: 85d5617e-8b73-449a-9627-2c8d5ab2b629
keywords:
- no atributo MIDL
topic_type:
- apiref
api_name:
- in
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606a834b394197960777fa485d112a94212ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103641016"
---
# <a name="in-attribute"></a>atributo in

O atributo **\[ in \]** indica que um parâmetro deve ser passado do procedimento de chamada para o procedimento chamado.

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ in [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[ retorno de chamada \]**, **\[ local \]**, **\[ referência \]** de atributo de ponteiro, **\[ exclusivo \]** ou **\[ PTR \]**, e a cadeia de **\[ caracteres \]** de atributos de uso, **\[ ignorar \]** e **\[ \_ identificador \] de contexto**.

</dd> <dt>

*especificador de tipo* 
</dt> <dd>

Especifica um tipo de **base \_**, [**struct**](struct.md), [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo. Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.

</dd> <dt>

*Declarador de ponteiro* 
</dt> <dd>

Especifica zero ou mais declaradores de ponteiro. Um Declarador de ponteiro é o mesmo que o Declarador de ponteiro usado em C; Ele é construído a partir do \* designador, modificadores, como **distante** e o qualificador [**const**](const.md).

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome do procedimento remoto.

</dd> <dt>

*lista de atributos de parâmetro* 
</dt> <dd>

Especifica zero ou mais atributos apropriados para o tipo de parâmetro especificado. Atributos de parâmetro com o atributo **\[ \] in** também podem pegar o atributo direcional **\[ out \]**; os atributos de campo **\[ First \_ são \]**, **\[ Last \_ is \]**, **\[ length \_ is \]**, **\[ Max \_ is \]**, **\[ Size \_ is \]** e **\[ switch \_ Type \]**; o atributo ponteiro **\[ ref \]**, **\[ Unique \]** ou **\[ PTR \]**; e o **\[ \_ identificador \] de contexto** e a cadeia de **\[ caracteres \]** de atributos de uso. O atributo de uso **\[ ignore \]** não pode ser usado como um atributo de parâmetro. Separe vários atributos com vírgulas.

</dd> <dt>

*Declarador* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). O Declarador de parâmetro no Declarador de função, como o nome do parâmetro, é opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo in tem um atributo **\[ \] de** inverso **\[** [**,**](out-idl.md) **\]** que indica que um parâmetro deve ser retornado do procedimento chamado para o procedimento de chamada. Os atributos in e **\[ out \]** são conhecidos como atributos **\[ de \]** parâmetro direcional, pois especificam a direção em que os parâmetros são passados. Um parâmetro pode ser definido como **\[ in \]**, **\[ out \]** ou **\[ in**, **out \]**.

O atributo **\[ in \]** identifica parâmetros que são empacotados pelo stub do cliente para transmissão para o servidor.

O atributo in é aplicado a um parâmetro por padrão quando nenhum atributo **\[ de \]** parâmetro direcional é especificado.

## <a name="examples"></a>Exemplos

``` syntax
HRESULT MyFunction([in] short count);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_alocar usuário de MIDL \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**fora**](out-idl.md)
</dt> </dl>

 

 