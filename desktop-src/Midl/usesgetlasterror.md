---
title: atributo usesgetlasterror
description: O atributo \ usesgetlasterror \ sinaliza ao chamador que ele pode chamar GetLastError para recuperar o código de erro.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror do atributo MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640559"
---
# <a name="usesgetlasterror-attribute"></a>atributo usesgetlasterror

O atributo **\[ usesgetlasterror \]** sinaliza ao chamador que ele pode chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o código de erro.

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*atributos de módulo* 
</dt> <dd>

Zero ou mais atributos MIDL que serão aplicados ao [**módulo**](module.md).

</dd> <dt>

*nome do módulo* 
</dt> <dd>

O nome do identificador do [**módulo**](module.md).

</dd> <dt>

*ID de entrada* 
</dt> <dd>

Especifica o ponto de entrada do módulo – nome da função ou número de identificação de inteiro.

</dd> <dt>

*outros atributos* 
</dt> <dd>

Zero ou mais atributos MIDL que serão aplicados ao procedimento remoto.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

O tipo dos dados que o procedimento remoto retornará após a conclusão.

</dd> <dt>

*nome da função* 
</dt> <dd>

O nome do procedimento remoto conforme definido no arquivo IDL.

</dd> <dt>

*parâmetro-lista* 
</dt> <dd>

Zero ou mais parâmetros para o procedimento remoto.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ \] usesgetlasterror** pode ser definido em um ponto de entrada de módulo, se esse ponto de entrada usar a função [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) do Windows para retornar códigos de erro. O atributo informa ao chamador que, se houver um erro ao chamar essa função, o chamador poderá chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o código de erro.

## <a name="examples"></a>Exemplos

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 