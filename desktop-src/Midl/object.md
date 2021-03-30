---
title: atributo de objeto
description: O atributo \ Object \ interface identifica uma interface COM.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- MIDL de atributo de objeto
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb2c21246282646dcf6ae488411316e07ab62b2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640858"
---
# <a name="object-attribute"></a>atributo de objeto

O atributo de interface de **\[ objeto \]** identifica uma interface com. (Uma lista de atributos de interface que não inclui o atributo **\[ Object \]** indica uma interface RPC DCE.)

``` syntax
[ 
    object, 
    uuid(string-uuid)
    [ , interface-attribute-list] 
] 
interface interface-name : base-interface
{
...    
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cadeia de caracteres-UUID* 
</dt> <dd>

Uma cadeia de caracteres UUID gerada pelo utilitário Uuidgen. Você pode colocar a cadeia de caracteres UUID entre aspas.

</dd> <dt>

*interface-atributo-lista* 
</dt> <dd>

Outros atributos que se aplicam à interface como um todo.

</dd> <dt>

*nome da interface* 
</dt> <dd>

O nome da interface.

</dd> <dt>

*interface base* 
</dt> <dd>

A interface COM da qual essa interface deriva. A interface base deve ser [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)ou outra interface com que derive, direta ou indiretamente, de **IUnknown** ou **IDispatch**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma lista de atributos de interface para uma interface COM deve incluir o **\[** atributo [**UUID**](uuid.md) **\]** , mas não pode incluir o **\[** [](version.md) **\]** atributo Version.

Por padrão, a compilação de uma interface com com o compilador MIDL gera os arquivos necessários para criar uma DLL de proxy. Essa DLL contém o código para dar suporte ao uso da interface COM personalizada por aplicativos cliente e servidores de objetos. No entanto, se a lista de atributos de interface de uma interface COM especificar o **\[** atributo [**local**](local.md) **\]** , o compilador MIDL gerará apenas o arquivo de cabeçalho da interface.

O compilador MIDL gera automaticamente um tipo de dados de interface para uma interface COM. Como alternativa, você pode usar [**typedef**](typedef.md) com a palavra-chave [**interface**](interface.md) para definir explicitamente um tipo de dados de interface. A especificação de interface pode usar o tipo de dados de interface nos parâmetros de função e valores de retorno, membros de [**struct**](struct.md) e [**Union**](union.md) e outras declarações de tipo. O exemplo a seguir ilustra o uso de um tipo de dados [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) gerado automaticamente:

``` syntax
[
    object, 
    uuid (ABCDEFOO-1234-1234-5678-ABCDEF123456)
] 
interface IStream : IUnknown
{ 
    typedef IStream * LPSTREAM; 
    // Other interface definition statements.
}
```

Em uma interface COM, todas as funções de membro de interface são consideradas como funções virtuais. Uma função virtual tem um indicador implícito **desse** ponteiro como o primeiro parâmetro. A tabela de funções virtuais contém uma entrada para cada função de membro de interface.

**\[**[](local.md) **\]** Funções de membro de interface de objeto não local devem ter um valor de retorno de HRESULT ou SCODE. (Observe que as versões anteriores do MIDL permitiam que as funções de membro retornassem [**void**](void.md). No entanto, a partir do MIDL versão 3,0, retornar **void** gera um erro do compilador.) Ter um valor de retorno de HRESULT ou SCODE significa que, se uma exceção for gerada durante uma chamada remota, os proxies gerados capturarão a exceção e retornarão o código de exceção no valor de retorno. Se seu aplicativo puder ignorar os erros que ocorrem durante uma chamada de procedimento remoto, você poderá especificar HRESULT como o tipo de retorno sem verificar o valor de retorno após a chamada.

Se você estiver recompilando um aplicativo antigo, alterar os tipos de retorno poderá apresentar problemas de compatibilidade com versões anteriores quando o servidor enviar o resultado introduzido recentemente ao cliente. Como alternativa à alteração do tipo de retorno, você pode rotular a função que retorna [**void**](void.md) com a **\[** [**chamada \_ como**](call-as.md) **\]** atributo, tornando-a uma função local. Em seguida, defina uma função remota relacionada com os mesmos parâmetros, mas com o tipo de retorno de HRESULT. A função local pode gerar uma exceção com base nesse valor HRESULT, se necessário.

O atributo **\[ \] Object** não está disponível quando você compila usando a opção [**/OSF**](-osf.md) do compilador MIDL.

## <a name="examples"></a>Exemplos

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    object
] 
interface IMyInterface : IUnknown
{
    // Interface definition statements.
}

[
    uuid(87654321-1234-1234-1234-123456789ABC), 
    object, 
    local
] 
interface ILocalInterface : ISomeOldCOMInterface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**chamar \_ como**](call-as.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**IID \_ é**](iid-is.md)
</dt> <dt>

[**interface**](interface.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 