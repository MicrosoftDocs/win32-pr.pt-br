---
title: auto_handle atributo
description: O atributo \ auto handle\ ACF direciona o stub para estabelecer automaticamente a associação para uma função que não tem um parâmetro de alça de associação \_ explícita. Observação Este atributo está obsoleto e não tem mais suporte.
ms.assetid: a402b933-f69b-4dfe-b0c5-b034d65d4a84
keywords:
- auto_handle atributo MIDL
topic_type:
- apiref
api_name:
- auto_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1f42a2fb643a2ce643437aad73b13c6e55d3462e92f9ce52ba208c6dc5cb68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807879"
---
# <a name="auto_handle-attribute"></a>atributo \_ auto handle

O **\[ atributo \_ \]** ACF de lidar automaticamente direciona o stub para estabelecer automaticamente a associação para uma função que não tem um parâmetro de alça de associação explícito.

> [!Note]  
> Esse atributo está obsoleto e não tem mais suporte. É recomendável [**usar a opção /robust.**](-robust.md)

 

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

*interface-attribute-list* 
</dt> <dd>

Especifica zero ou mais atributos que se aplicam à interface como um todo, como [**código**](code.md) [**ou nocode.**](nocode.md) Atributos de interface separados com vírgulas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*interface-definition* 
</dt> <dd>

Especifica instruções IDL que formam a definição da interface.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \_ de \]** alça automática aparece no header da interface do ACF. Ele também aparece no header da interface do arquivo IDL quando você especifica a opção do compilador MIDL [**/configuração \_ do aplicativo**](-app-config.md).

Quando o cliente chama uma função que usa associação automática e nenhuma associação a um servidor existe, o stub estabelece automaticamente a associação. A associação é reutilizada para chamadas subsequentes para outras funções na interface que usam associação automática. O programa de aplicativo cliente não precisa declarar ou executar nenhum processamento relacionado ao alça de associação.

Quando o ACF não está presente [**\[ \_ \]**](implicit-handle.md) ou não inclui o atributo de alça implícita, o compilador **\[ \_ \]** MIDL usa o manipular automaticamente e emite uma mensagem informacional. O compilador MIDL também usa **\[ o manipular \_ automaticamente \]**, se necessário, para estabelecer a associação inicial para um alça [**\[ de \_ contexto \]**](context-handle.md).

O **\[ atributo de \_ alça \]** automática só poderá ocorrer se o [**\[ atributo de alça \_ implícita \]**](implicit-handle.md) [**\[ ou de \_ \]**](explicit-handle.md) alça explícita não ocorrer. O **\[ atributo \_ de \]** alça automática pode ocorrer no header da interface ACF ou IDL no máximo uma vez.

> [!Note]  
> Você não poderá usar a associação automática (com o atributo **\[ de \_ alça \]** automática ou por padrão) se estiver processando dados por meio de pipes.

 

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

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**Código**](code.md)
</dt> <dt>

[**alça \_ explícita**](explicit-handle.md)
</dt> <dt>

[**alça de \_ contexto**](context-handle.md)
</dt> <dt>

[**alça \_ implícita**](implicit-handle.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> </dl>

 

 




