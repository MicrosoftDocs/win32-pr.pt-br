---
title: atributo defaultvalue
description: O atributo \ defaultvalue\ permite que você especifique um valor padrão para um parâmetro opcional digitado.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- atributo defaultvalue MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f38fe7dfc99c5c9c1c6a7cae1a5fdd5750c5f3e9af37e56706b27300876da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067346"
---
# <a name="defaultvalue-attribute"></a>atributo defaultvalue

O **\[ atributo \] defaultvalue** permite que você especifique um valor padrão para um parâmetro opcional digitado.

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

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função à qual o **\[ atributo defaultvalue \]** será aplicado.

</dd> <dt>

*mandatory-param-list* 
</dt> <dd>

Especifica em ou mais parâmetros necessários.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica uma lista de um ou mais atributos, separados por vírgulas, que se aplicam ao parâmetro .

</dd> <dt>

*param-type* 
</dt> <dd>

Indica o tipo do parâmetro opcional.

</dd> <dt>

*param-name* 
</dt> <dd>

Especifica o nome do parâmetro opcional.

</dd> <dt>

*optional-param-list* 
</dt> <dd>

Especifica zero ou mais parâmetros adicionais, cada um deles deve ter um valor padrão.

</dd> </dl>

## <a name="remarks"></a>Comentários

O valor padrão especificado para o parâmetro pode ser qualquer constante ou uma expressão que é resolvida para uma constante, que pode ser representada por **uma VARIANT**. Especificamente, você não pode aplicar o **\[ atributo \] defaultvalue** a um parâmetro que seja uma estrutura, uma matriz ou um tipo **SAFEARRAY.**

O compilador MIDL aceita a seguinte ordenação de parâmetros (da esquerda para a direita):

1.  Parâmetros necessários (parâmetros que não têm o valor padrão **\[ \] ou** atributos **\[** [**opcionais),**](optional.md) **\]**
2.  parâmetros opcionais com ou sem o **\[ atributo defaultvalue, \]**
3.  parâmetros com o **\[ atributo opcional \]** e sem o atributo **\[ defaultvalue, \]**
4.  **\[**[**Parâmetro lcid,**](lcid.md) **\]** se for o caso,
5.  **\[**[**retval**](retval.md) **\]** Parâmetro

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

[**Interface**](interface.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> <dt>

[**Opcional**](optional.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**retval**](retval.md)
</dt> <dt>

[Typeflags](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 