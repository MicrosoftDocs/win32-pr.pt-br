---
title: atributo defaultvalue
description: O atributo \ DefaultValue \ permite que você especifique um valor padrão para um parâmetro opcional tipado.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- atributo DefaultValue de MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294008"
---
# <a name="defaultvalue-attribute"></a>atributo defaultvalue

O atributo **\[ DefaultValue \]** permite que você especifique um valor padrão para um parâmetro opcional tipado.

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função à qual o atributo **\[ DefaultValue \]** será aplicado.

</dd> <dt>

*obrigatório-param-List* 
</dt> <dd>

Especifica um ou mais parâmetros necessários.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao parâmetro.

</dd> <dt>

*tipo de parâmetro* 
</dt> <dd>

Indica o tipo do parâmetro opcional.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o nome do parâmetro opcional.

</dd> <dt>

*opcional-lista de parâmetros* 
</dt> <dd>

Especifica zero ou mais parâmetros adicionais, cada um dos quais deve ter um valor padrão.

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor padrão especificado para o parâmetro pode ser qualquer constante ou uma expressão que seja resolvida para uma constante, que pode ser representada por uma **variante**. Especificamente, você não pode aplicar o atributo **\[ \] DefaultValue** a um parâmetro que é uma estrutura, uma matriz ou um tipo **SafeArray** .

O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):

1.  Parâmetros necessários (parâmetros que não têm os atributos **\[ DefaultValue \]** ou **\[** [**optional**](optional.md) **\]** ),
2.  parâmetros opcionais com ou sem o atributo **\[ DefaultValue \]** ,
3.  parâmetros com o atributo **\[ opcional \]** e sem o atributo **\[ DefaultValue \]** ,
4.  **\[** parâmetro [**LCID**](lcid.md) **\]** , se houver,
5.  **\[**[**retval**](retval.md) **\]** meter

## <a name="examples"></a>Exemplos

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**LCID**](lcid.md)
</dt> <dt>

[**adicional**](optional.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 