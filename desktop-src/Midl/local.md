---
title: atributo local
description: O atributo \ local \ especifica para o compilador MIDL que uma interface ou função não é remota.
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- atributo local MIDL
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105754659"
---
# <a name="local-attribute"></a>atributo local

O atributo **\[ local \]** especifica o compilador MIDL que uma interface ou função não é remota.

``` syntax
[ 
    local 
    [, interface-attribute-list] 
] 
interface interface-name
{
}

[ 
    object, 
    uuid(string-uuid), 
    local [, interface-attribute-list] 
]
interface interface-name
{
}

[ local [, function-attribute-list] ] function-declarator ;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica outros atributos que se aplicam à interface como um todo. O ponto de extremidade dos atributos **\[** [](endpoint.md) **\]** , a **\[** [**versão**](version.md) **\]** e o **\[** [**ponteiro \_ padrão**](pointer-default.md) **\]** são opcionais. Quando você compila com a opção de [**\_ configuração/app**](-app-config.md) , o **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** ou o **\[** [**\_ identificador automático**](auto-handle.md) **\]** também pode estar presente. Separe vários atributos com vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome pelo qual os componentes de software podem delinear a interface.

</dd> <dt>

*Cadeia de caracteres-UUID* 
</dt> <dd>

Especifica uma cadeia de caracteres UUID gerada pelo utilitário Uuidgen. Se você não estiver usando a opção de compilador MIDL [**/OSF**](-osf.md), poderá colocar a cadeia de caracteres UUID entre aspas.

</dd> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à função. Os atributos de função válidos são **\[** [**retorno de chamada**](callback.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** , **\[** [**ignore**](ignore.md) **\]** e o **\[** [**\_ identificador de contexto**](context-handle.md) **\]** . Separe vários atributos com vírgulas.

</dd> <dt>

*função-declaradora* 
</dt> <dd>

Especifica o especificador de tipo, o nome da função e a lista de parâmetros para a função.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ local \]** pode ser aplicado a funções individuais ou à interface como um todo.

Quando usado no cabeçalho da interface, o atributo **\[ local \]** permite que você use o compilador MIDL como um gerador de cabeçalho. O compilador não gera stubs para nenhuma função e não garante que o cabeçalho possa ser transmitido.

Para uma interface RPC, o atributo **\[ local \]** não pode ser usado ao mesmo tempo que o **\[** atributo [**UUID**](uuid.md) **\]** . O **\[ UUID \]** ou o **\[ local \]** devem estar presentes no cabeçalho da interface e o que você escolher deve ocorrer exatamente uma vez.

Para uma interface COM (identificada pelo **\[** atributo de interface de [**objeto**](object.md) **\]** ), a lista de atributos de interface pode incluir o atributo **\[ local \]** , embora o **\[** atributo [**UUID**](uuid.md) **\]** esteja presente.

Quando usado em uma função individual, o atributo **\[ local \]** designa um procedimento local para o qual nenhum stub é gerado. Usar o **\[ local \]** como um atributo de função é uma extensão da Microsoft para o DCE IDL. Portanto, esse atributo não estará disponível quando você compilar usando a opção MIDL [**/OSF**](-osf.md)

Observe que uma interface sem atributos pode ser importada para um arquivo IDL base. No entanto, a interface deve conter apenas tipos de texto sem procedimentos. Se até um procedimento estiver contido na interface, um atributo local ou UUID deverá ser especificado.

## <a name="examples"></a>Exemplos

``` syntax
/* IDL file #1 */ 
[
    local
] 
interface local_procs 
{ 
    void MyLocalProc(void);
} 
 
/* IDL file #2 */ 
[
    object, 
    uuid(12345678-1234-1234-123456789ABC), 
    local
] 
interface local_object_procs : IUnknown
{ 
    void MyLocalObjectProc(void);
} 
 
/* IDL file #3 */ 
[
    uuid(87654321-1234-1234-123456789ABC)
] 
interface mixed_procs 
{ 
    [local] void MyLocalProc(void); 
    HRESULT MyRemoteProc([in] short sParam); 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**configuração do/App \_**](-app-config.md)
</dt> <dt>

[**\_identificador automático**](auto-handle.md)
</dt> <dt>

[**retorno de chamada**](callback.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ignorar**](ignore.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**padrão de ponteiro \_**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**diferente**](unique.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 




