---
title: atributo dispinterface
description: A instrução dispinterface define um conjunto de propriedades e métodos nos quais você pode chamar a invocação IDispatch.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- MIDL de atributo de dispinterface
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823754"
---
# <a name="dispinterface-attribute"></a>atributo dispinterface

A instrução **dispinterface** define um conjunto de propriedades e métodos nos quais você pode chamar **IDispatch:: Invoke**. Uma dispinterface pode ser definida por meio da listagem explícita do conjunto de métodos e propriedades com suporte (sintaxe 1) ou da listagem de uma única interface (sintaxe 2).

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*attributes* 
</dt> <dd>

Especifica os atributos que se aplicam a toda a **dispinterface**. Os seguintes atributos são aceitos: **\[** [**HelpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**ArquivoDeAjuda**](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**extensível**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**version**](version.md) **\]** .

</dd> <dt>

*dispinterface-nome* 
</dt> <dd>

O nome pelo qual a **dispinterface** é conhecida na biblioteca de tipos. Esse nome deve ser exclusivo na biblioteca de tipos.

</dd> <dt>

*lista de propriedades* 
</dt> <dd>

(Sintaxe 1) Uma lista opcional de propriedades com suporte pelo objeto, declarada na forma de variáveis. Essa é a forma abreviada de declarar as funções de propriedade na lista de métodos. Consulte a seção de comentários para obter detalhes.

</dd> <dt>

*lista de métodos* 
</dt> <dd>

(Sintaxe 1) Uma lista que inclui um protótipo de função para cada método e Propriedade na **dispinterface**. Qualquer número de definições de função pode aparecer em *methlist*. Uma função em *methlist* tem o seguinte formato:

**\[  atributos \]** *ReturnType methname tipo paramName ***(*** params * * *);**

Os atributos a seguir são aceitos em um método em uma **dispinterface**: **\[ \] HelpString**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**propputref**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** e **\[** [**vararg**](vararg.md) **\]** . Se **\[ vararg \]** for especificado, o último parâmetro deverá ser uma matriz segura de tipo **Variant** .

A lista de parâmetros é uma lista delimitada por vírgula, cada elemento do qual tem o seguinte formato:

**\[***atributos***\]**

O *tipo* pode ser qualquer tipo declarado ou interno, ou um ponteiro para qualquer tipo. Os atributos em parâmetros são:

**\[**[**entrada**](in.md) **\]** , **\[** [**saída**](out-idl.md) **\]** , **\[** [**opcional**](optional.md) **\]** , **\[ cadeia \] de caracteres**

</dd> <dt>

*nome da interface* 
</dt> <dd>

(Sintaxe 2) O nome da interface a ser declarada como uma interface IDispatch.

</dd> </dl>

## <a name="remarks"></a>Comentários

O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):

1.  Parâmetros necessários (parâmetros que não têm os \[ atributos DefaultValue \] ou \[ optional \] ),
2.  parâmetros opcionais com ou sem \[ o \] atributo DefaultValue,
3.  parâmetros com o \[ \] atributo opcional e sem o \[ \] atributo DefaultValue,
4.  \[parâmetro [**LCID**](lcid.md) \] , se houver,
5.  \[[**retval**](retval.md) \] meter

As funções de método são especificadas exatamente conforme descrito na página de referência para o [**módulo**](module.md) , exceto pelo fato de que o atributo de \[ [**entrada**](entry.md) \] não é permitido. Observe que STDOLE32. TLB (STDOLE. O TLB em sistemas de 16 bits) deve ser importado, pois uma **dispinterface** herda de IDispatch.

Você pode declarar Propriedades nas listas Propriedades ou métodos. A declaração de propriedades na lista de propriedades não indica o tipo de acesso que a propriedade dá suporte (ou seja, Get, PUT ou PUTREF). Especifique o \[ [](readonly.md) \] atributo ReadOnly para propriedades que não dão suporte a Put ou PUTREF. Se você declarar as funções de propriedade na lista de métodos, todas as funções de uma propriedade terão o mesmo identificador.

Usando a primeira sintaxe, as marcas Properties: and: são obrigatórias. O \[ atributo [**ID**](id.md) \] também é necessário em cada membro. Por exemplo:

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

Diferentemente dos membros da interface, os membros de dispinterface não podem usar o atributo [**retval**](retval.md) para retornar um valor além de um código de erro HRESULT. O \[ [](lcid.md) \] atributo LCID é, da mesma forma, inválido para dispinterfaces, porque IDispatch:: Invoke passa um LCID. No entanto, é possível redeclarar uma interface que usa esses atributos.

Usando a segunda sintaxe, as interfaces que dão suporte a IDispatch e são declaradas anteriormente em um script ODL podem ser redeclarados como interfaces IDispatch da seguinte maneira:

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

O exemplo anterior declara todos os membros de Hello e todos os membros que Hello herda como suporte a IDispatch. Nesse caso, se Hello tiver sido declarado anteriormente com \[ \] \[ os membros LCID e retval \] que retornaram HRESULTs, MkTypLib removeria cada \[ \] parâmetro LCID e tipo de retorno HRESULT e, em vez disso, marcaria o tipo de retorno como o do \[ \] parâmetro retval.

> [!Note]  
> A ferramenta de Mktyplib.exe está obsoleta. Em vez disso, use o compilador MIDL.

 

As propriedades e os métodos de uma Dispinterface não fazem parte do VTBL da dispinterface. Consequentemente, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) e [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) não podem ser usados para implementar IDispatch:: Invoke. A dispinterface é usada quando um aplicativo precisa expor funções não VTBL existentes por meio da automação. Esses aplicativos podem implementar IDispatch:: Invoke examinando o parâmetro dispidMember e chamando diretamente a função correspondente.

## <a name="examples"></a>Exemplos

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**oculto**](hidden.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**adicional**](optional.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**nonextensible**](nonextensible.md)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**Restricted**](restricted.md)
</dt> <dt>

[**Strings**](string.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> <dt>

[**vararg**](vararg.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 