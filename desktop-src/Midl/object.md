---
title: atributo de objeto
description: O atributo \ object\ interface identifica uma interface COM.
ms.assetid: 51e34ef3-eea7-45f4-b961-a9f742700fe5
keywords:
- atributo de objeto MIDL
topic_type:
- apiref
api_name:
- object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ddf51e020cdcd5d13dde6938a58ea5e51f22d9dd03f8632312b3d6b8453a9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383504"
---
# <a name="object-attribute"></a>atributo de objeto

O **\[ atributo \]** de interface de objeto identifica uma interface COM. (Uma lista de atributos de interface que não inclui o **\[ atributo de \]** objeto indica uma interface RPC DCE.)

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

*string-uuid* 
</dt> <dd>

Uma cadeia de caracteres UUID gerada pelo utilitário Uuidgen. Você pode colocar a cadeia de caracteres UUID entre aspas.

</dd> <dt>

*interface-attribute-list* 
</dt> <dd>

Outros atributos que se aplicam à interface como um todo.

</dd> <dt>

*interface-name* 
</dt> <dd>

O nome da interface.

</dd> <dt>

*interface base* 
</dt> <dd>

A interface COM da qual essa interface deriva. A interface base deve ser [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)ou outra interface COM que deriva, direta ou indiretamente, de **IUnknown** ou **IDispatch**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma lista de atributos de interface para uma interface COM deve incluir o **\[** [**atributo uuid,**](uuid.md) **\]** mas não pode incluir o atributo **\[** [**de**](version.md) **\]** versão.

Por padrão, compilar uma interface COM com o compilador MIDL gera os arquivos necessários para criar uma DLL de proxy. Essa DLL contém o código para dar suporte ao uso da interface COM personalizada por aplicativos cliente e servidores de objeto. No entanto, se a lista de atributos de interface para uma interface COM especificar o atributo **\[** [**local,**](local.md) o **\]** compilador MIDL gerará apenas o arquivo de header da interface.

O compilador MIDL gera automaticamente um tipo de dados de interface para uma interface COM. Como alternativa, você pode usar [**typedef**](typedef.md) com a palavra-chave [**de interface**](interface.md) para definir explicitamente um tipo de dados de interface. A especificação de interface pode usar o tipo de dados de interface em parâmetros de função e valores de retorno, [**membros de struct**](struct.md) e [**união**](union.md) e outras declarações de tipo. O exemplo a seguir ilustra o uso de um tipo de dados [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) gerado automaticamente:

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

Em uma interface COM, todas as funções membro da interface são assumidas como funções virtuais. Uma função virtual tem um ponteiro **this implícito** como o primeiro parâmetro. A tabela de funções virtuais contém uma entrada para cada função membro da interface.

As funções membro da interface de objeto não **\[** [**local**](local.md) **\]** devem ter um valor de retorno HRESULT ou SCODE. (Observe que as versões anteriores do MIDL permitiam que as funções de membro retornam [**void.**](void.md) No entanto, começando com a versão MIDL 3.0, retornar **void** gera um erro do compilador.) Ter um valor de retorno de HRESULT ou SCODE significa que, se uma exceção for gerada durante uma chamada remota, os proxies gerados capturarão a exceção e retornarão o código de exceção no valor de retorno. Se o aplicativo puder ignorar erros que ocorrem durante uma chamada de procedimento remoto, você poderá especificar HRESULT como o tipo de retorno sem verificar o valor de retorno após a chamada.

Se você estiver recompilando um aplicativo antigo, alterar os tipos de retorno poderá introduzir problemas de compatibilidade com compatibilidade com backward quando o servidor enviar o resultado recém-introduzido ao cliente. Como alternativa à alteração do tipo de retorno, você pode rotular a função que retorna [**void**](void.md) com a chamada como **\[** [**\_**](call-as.md) **\]** atributo, tornando-a uma função local. Em seguida, defina uma função remota relacionada com os mesmos parâmetros, mas com o tipo de retorno HRESULT. A função local pode criar uma exceção com base nesse valor HRESULT, se necessário.

O **\[ \] atributo** de objeto não está disponível quando você compila usando a opção [**/osf do**](-osf.md) compilador MIDL.

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

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**iid \_ é**](iid-is.md)
</dt> <dt>

[**Interface**](interface.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 