---
title: atributo Async
description: O atributo \ Async \ ACF define uma chamada de procedimento remoto como uma operação assíncrona.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL de atributo assíncrono
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917222"
---
# <a name="async-attribute"></a>atributo Async

O \[  \] atributo Async ACF define uma chamada de procedimento remoto como uma operação assíncrona.

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*aceitar-ACF-atributos* 
</dt> <dd>

Especifica atributos de configuração de aplicativo opcionais.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função no arquivo IDL.

</dd> <dt>

*parâmetro-lista* 
</dt> <dd>

Especifica uma lista de parâmetros opcionais.

</dd> </dl>

## <a name="remarks"></a>Comentários

Este atributo não é aplicável em interfaces COM.

Para declarar uma função RPC como assíncrona, primeiro declare a função como parte de uma definição de interface em um arquivo IDL. Em seguida, modifique essa declaração de função, dentro do arquivo de configuração de aplicativo (ACF), aplicando o \[  \] atributo Async. Observe que a declaração de função não faz menção do identificador assíncrono e que o identificador de associação é o primeiro parâmetro. A aplicação do \[ atributo **Async** \] no arquivo ACF gera o código apropriado para que, quando essa função for chamada, o servidor assíncrono Espere receber um identificador assíncrono antes dos outros parâmetros.

> [!Note]  
> O atributo Async não pode ser usado com a opção de linha de comando [**/OSF**](-osf.md)

 

## <a name="examples"></a>Exemplos

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[RPC assíncrono](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 