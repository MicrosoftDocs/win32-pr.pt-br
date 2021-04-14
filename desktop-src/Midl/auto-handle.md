---
title: auto_handle atributo
description: O atributo \ \_ identificador auto \ ACF direciona o stub para estabelecer automaticamente a associação para uma função que não tem um parâmetro de identificador de ligação explícito. Observe que esse atributo está obsoleto e não tem mais suporte.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle do atributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e9a4c91fac8553867536f4f5a8c3094e0f0ff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453763"
---
# <a name="auto_handle-attribute"></a>\_manipular atributo automaticamente

O atributo de ACF de **\[ \_ identificador \] automático** direciona o stub para estabelecer automaticamente a associação para uma função que não tem um parâmetro de identificador de ligação explícito.

> [!Note]  
> Este atributo está obsoleto e não tem mais suporte. O uso da opção [**/robust**](-robust.md) é recomendado.

 

``` syntax
[ 
    auto_handle [, interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à interface como um todo, como [**código**](code.md) ou [**Nocode**](nocode.md). Separe os atributos de interface com vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*interface-definição* 
</dt> <dd>

Especifica as instruções IDL que formam a definição da interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ \_ identificador \] automático** é exibido no cabeçalho da interface do ACF. Ele também aparece no cabeçalho da interface do arquivo IDL quando você especifica a [**\_ configuração do/App**](-app-config.md)do compilador MIDL.

Quando o cliente chama uma função que usa associação automática e nenhuma associação a um servidor existe, o stub estabelece automaticamente a associação. A associação é reutilizada para chamadas subsequentes para outras funções na interface que usam associação automática. O programa de aplicativo cliente não precisa declarar ou executar nenhum processamento relacionado ao identificador de associação.

Quando o ACF não estiver presente ou não incluir o atributo de [**\[ \_ identificador \] implícito**](implicit-handle.md) , o compilador MIDL usará o **\[ \_ \] identificador auto** e emitirá uma mensagem informativa. O compilador MIDL também usa o **\[ \_ identificador \] auto**, se necessário, para estabelecer a associação inicial para um [**\[ \_ identificador \] de contexto**](context-handle.md).

O atributo de **\[ \_ identificador \] automático** só poderá ocorrer se o [**\[ \_ identificador \] implícito**](implicit-handle.md) ou o atributo de [**\[ \_ identificador \] explícito**](explicit-handle.md) não ocorrer. O atributo de **\[ \_ identificador \] automático** pode ocorrer no cabeçalho de interface ACF ou IDL no máximo uma vez.

> [!Note]  
> Você não poderá usar a associação automática (com o atributo **\[ \_ identificador \] automático** ou por padrão) se estiver processando dados por meio de pipes.

 

## <a name="examples"></a>Exemplos

``` syntax
[
    auto_handle
] 
interface MyInterface 
{ 
    /* Interface definition goes here*/
} 
[
    auto_handle, 
    code
] 
interface MyInterface
{ 
    /* Interface definition goes here*/
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**configuração do/App \_**](-app-config.md)
</dt> <dt>

[**auto-completar**](code.md)
</dt> <dt>

[**\_identificador explícito**](explicit-handle.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**Nocode**](nocode.md)
</dt> </dl>

 

 




