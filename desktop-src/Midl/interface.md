---
title: atributo de interface
description: A palavra-chave interface especifica o nome da interface. O nome da interface deve ser fornecido no arquivo IDL e no ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- atributo de interface MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823699"
---
# <a name="interface-attribute"></a>atributo de interface

A palavra-chave **interface** especifica o nome da interface. O nome da interface deve ser fornecido no arquivo IDL e no ACF.

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica os atributos que se aplicam à interface como um todo. Atributos de interface válidos para um arquivo IDL incluem **\[** [**ponto de extremidade**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**objeto**](object.md) **\]** , **\[** [**\_ padrão de ponteiro**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**versão**](version.md) **\]** . Atributos de interface válidos para um ACF incluem **\[** [**codificação**](encode.md) **\]** , **\[** [**decodificação**](decode.md) **\]** , **\[** [**\_ identificador automático**](auto-handle.md) **\]** ou **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** e **\[** [**código**](code.md) **\]** ou **\[** [**Nocode**](nocode.md) **\]** .

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface. O nome da interface deve ser um nome exclusivo e deve começar com um caractere alfabético ou de sublinhado.

</dd> <dt>

*interface base* 
</dt> <dd>

Especifica o nome de uma interface da qual essa interface derivada herda funções de membro, códigos de status e atributos de interface. A interface derivada não herda definições de tipo. Para fazer isso, use a palavra-chave [**Import**](import.md) para importar o arquivo IDL da interface base.

</dd> <dt>

*Declarador-lista* 
</dt> <dd>

Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz. Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers). A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os nomes de interface no arquivo IDL e ACF devem ser os mesmos, exceto quando você usa o switch do compilador MIDL [**/ACF**](-acf.md).

O nome da interface forma a primeira parte do nome de estruturas de dados de identificador de interface que são parâmetros para as funções de tempo de execução RPC. Para obter mais informações, consulte [**RPC \_ If \_ Handle**](/windows/desktop/Rpc/rpc-if-handle).

Se o cabeçalho da interface incluir o **\[** atributo [**Object**](object.md) **\]** para indicar uma interface com, ele também deverá incluir o **\[** atributo [**UUID**](uuid.md) **\]** e deverá especificar a interface com base da qual ele é derivado. Para obter mais informações sobre interfaces COM, consulte **\[** [**Object**](object.md) **\]** .

Você também pode usar a palavra-chave **interface** com a palavra-chave [**typedef**](typedef.md) para definir um tipo de dados de interface.

## <a name="examples"></a>Exemplos

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**extremidade**](endpoint.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**local**](local.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**padrão de ponteiro \_**](pointer-default.md)
</dt> <dt>

[**RPC \_ se o \_ identificador**](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**personalizado**](uuid.md)
</dt> <dt>

[**Versão**](version.md)
</dt> </dl>

 

 