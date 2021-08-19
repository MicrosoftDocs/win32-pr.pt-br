---
title: Atributo async_uuid
description: O atributo \ Async \_ UUID \ interface direciona o compilador MIDL para definir versões síncronas e assíncronas de uma interface com.
ms.assetid: 1c20eaa1-78b5-4463-a8c1-d81e55d5c618
keywords:
- async_uuid do atributo MIDL
topic_type:
- apiref
api_name:
- async_uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a784cadf470fa312a82e473f3934dbda1a2b6dce20d2ae34c7074c309398cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808230"
---
# <a name="async_uuid-attribute"></a>\_atributo de UUID assíncrono

O atributo de interface do **\[ Async \_ UUID \]** direciona o compilador MIDL para definir versões síncronas e assíncronas de uma interface com.

``` syntax
[ 
    object, 
    uuid(string-uuid1), 
    async_uuid(string-uuid2)[ [, interface-attribute-list] 
]
interface interface-name : base-interface
{
    interface-definition
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cadeia de caracteres-uuid1* 
</dt> <dd>

Uma cadeia de caracteres UUID, gerada pelo utilitário Uuidgen, que identifica a versão síncrona da interface.

</dd> <dt>

*Cadeia de caracteres-uuid2* 
</dt> <dd>

Uma cadeia de caracteres UUID, gerada pelo utilitário Uuidgen, que identifica a versão assíncrona da interface.

</dd> <dt>

*interface-atributo-lista* 
</dt> <dd>

Outros atributos que se aplicam à interface como um todo. Você não pode usar o atributo [**\[ version \]**](version.md) em uma interface com.

</dd> <dt>

*nome da interface* 
</dt> <dd>

O nome da interface.

</dd> <dt>

*interface base* 
</dt> <dd>

A interface da qual essa interface deriva. A interface base deve ser **IUnknown** ou uma interface assíncrona que derive, direta ou indiretamente, de **IUnknown**.

</dd> <dt>

*interface-definição* 
</dt> <dd>

Especifica as instruções IDL que formam a definição da interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

o uso deste atributo requer Windows 2000 ou versões posteriores do Windows.

Quando você aplica o atributo **\[ \_ UUID \] do Async** a uma interface com (ou seja, uma interface que tem o atributo [**\[ Object \]**](object.md) ), o compilador MIDL gera uma definição assíncrona da interface, além da versão síncrona tradicional. A interface assíncrona terá os mesmos nomes que a interface síncrona, mas com um prefixo "Async". O identificador de interface (IID) será o UUID especificado como um parâmetro para o atributo **\[ Async \_ UUID \]** .

Para a interface assíncrona, MIDL divide cada método em métodos de *início* e *término* separados. O método *begin* tem o nome do método síncrono com um prefixo "Begin \_ " e inclui todos os parâmetros [**\[ in \]**](in.md) do método síncrono. O método *Finish* tem o nome do método síncrono com um prefixo "Finish \_ " e inclui todos os parâmetros de [**\[ saída \]**](out-idl.md) do método síncrono. Se o método síncrono tiver quaisquer parâmetros **\[ in, \] out,** eles serão incluídos nos métodos assíncronos *begin* e *Finish* .

Se um método de interface assíncrona tiver a [**\[ chamada \_ como \]**](call-as.md) atributo, MIDL irá gerar declarações para os métodos *begin* e *Finish* . Você deve implementar os dois métodos.

Cada interface assíncrona é um modificador em uma interface síncrona e, como tal, não tem um grafo de herança separado. Isso significa que você não pode definir uma interface síncrona a partir de uma interface assíncrona (diferente de **IUnknown**). Nem as interfaces síncronas podem herdar de interfaces assíncronas. O compilador MIDL emitirá uma mensagem de erro se você tentar uma delas.

## <a name="examples"></a>Exemplos

``` syntax
[
    object, 
    uuid(0c733a30-2a1c-11ce-ade5-00aa0044773d),
    async_uuid(1c733a30-2a1c-11ce-ade5-00aa0044773d),
    pointer_default(unique)
]
interface IMyInterface : IUnknown
{
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Definição de interfaces COM](/windows/desktop/com/defining-com-interfaces)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**chamar \_ como**](call-as.md)
</dt> <dt>

[**IID \_ é**](iid-is.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 