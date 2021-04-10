---
title: atributo entry
description: O atributo \ entry \ especifica uma função exportada ou constante em um módulo identificando o ponto de entrada na DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- MIDL do atributo de entrada
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293929"
---
# <a name="entry-attribute"></a>atributo entry

O atributo de **\[ entrada \]** especifica uma função exportada ou constante em um módulo identificando o ponto de entrada na dll.

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*UUID-número* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para o [**módulo**](module.md).

</dd> <dt>

*ID de entrada* 
</dt> <dd>

Especifica o nome da função do ponto de entrada do módulo ou o número de identificação do inteiro.

</dd> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica zero ou mais atributos para o compilador MIDL aplicar ao [**módulo**](module.md).

</dd> <dt>

*ModuleName* 
</dt> <dd>

Especifica o nome que outros componentes de software usam para denotar o [**módulo**](module.md).

</dd> <dt>

*elementolist* 
</dt> <dd>

Especifica uma ou mais instruções de definição de elemento de módulo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a variável *EntryID* do atributo de **\[ entrada \]** for uma cadeia de caracteres, esse será um ponto de entrada nomeado. Se *EntryID* for um número, o ponto de entrada será definido por um ordinal. Esse atributo fornece uma maneira de obter o endereço de uma função em um módulo.

## <a name="examples"></a>Exemplos

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**nomedadll**](dllname-str-.md)
</dt> <dt>

[**modulo**](module.md)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 