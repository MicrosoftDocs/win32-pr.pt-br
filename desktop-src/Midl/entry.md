---
title: atributo entry
description: O atributo \ entry\ especifica uma função ou constante exportada em um módulo identificando o ponto de entrada na DLL.
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- atributo de entrada MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f6dab1681cb04adbd48c4a27c14a359c87624870a43c118c6dd1a589689c00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013924"
---
# <a name="entry-attribute"></a>atributo entry

O **\[ atributo \]** de entrada especifica uma função ou constante exportada em um módulo identificando o ponto de entrada na DLL.

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

*uuid-number* 
</dt> <dd>

Especifica um número de identificação universalmente exclusivo para o [**módulo**](module.md).

</dd> <dt>

*entry-id* 
</dt> <dd>

Especifica o nome da função do ponto de entrada do módulo ou o número de identificação de inteiro.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos para o compilador MIDL a ser aplicado ao [**módulo**](module.md).

</dd> <dt>

*Modulename* 
</dt> <dd>

Especifica o nome que outros componentes de software usam para denotar o [**módulo**](module.md).

</dd> <dt>

*elementlist* 
</dt> <dd>

Especifica uma ou mais instruções de definição de elemento de módulo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a *variável entryid* do atributo **\[ de entrada \]** for uma cadeia de caracteres, esse será um ponto de entrada nomeado. Se *entryid* for um número, o ponto de entrada será definido por um ordinal. Esse atributo fornece uma maneira de obter o endereço de uma função em um módulo.

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

[**Dllname**](dllname-str-.md)
</dt> <dt>

[**Módulo**](module.md)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 