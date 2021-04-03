---
title: atributo defaultcollelem
description: O atributo \ defaultcollelem \ sinaliza uma propriedade como uma função de acessador para um elemento da coleção padrão.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- defaultcollelem do atributo MIDL
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007494"
---
# <a name="defaultcollelem-attribute"></a>atributo defaultcollelem

O atributo **\[ defaultcollelem \]** sinaliza uma propriedade como uma função de acessador para um elemento da coleção padrão.

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade-atributo-lista* 
</dt> <dd>

Outros atributos que se aplicam à propriedade.

</dd> <dt>

*tipo de retorno* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da propriedade* 
</dt> <dd>

O nome da propriedade.

</dd> <dt>

*prop-param-List* 
</dt> <dd>

Uma lista de zero ou mais parâmetros associados à propriedade.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ defaultcollelem \]** é usado para a otimização de código do Visual BasicÂ®. Se um membro de uma interface ou dispinterface for sinalizado como uma função de acessador, a chamada vai diretamente para esse membro.

O uso de **\[ defaultcollelem \]** deve ser consistente para uma propriedade. Por exemplo, se você usar o atributo em uma propriedade *Get* , ele também deverá estar presente em uma propriedade *Let* .

### <a name="typeflags-representation"></a>Representação TYPEFLAGS

A presença de FUNCFLAG \_ FDEFAULTCOLLELEM ou VARFLAG \_ FDEFAULTCOLLELEM.

## <a name="examples"></a>Exemplos

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe do arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Exemplo de arquivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Gerando uma biblioteca de tipos com MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 