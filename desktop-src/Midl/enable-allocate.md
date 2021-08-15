---
title: enable_allocate atributo
description: O atributo \ Enable \_ ALLOCATE \ ACF especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate do atributo MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f44b3a2f11094c37edf24f5fc00bbd8229d65dc2a54292acd2ca3221472e85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979616"
---
# <a name="enable_allocate-attribute"></a>Habilitar \_ atributo de alocação

O atributo **\[ habilitar \_ alocação \]** ACF especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.

> [!Note]  
> O atributo **\[ habilitar \_ alocação \]** é obsoleto e não tem mais suporte.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos opcionais* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos MIDL adicionais.

</dd> <dt>

*nome da interface* 
</dt> <dd>

O nome da interface à qual o atributo de **\[ habilitação de \_ \] imrevestimento** será aplicado.

</dd> </dl>

## <a name="remarks"></a>Comentários

No modo padrão, o stub de servidor habilita o ambiente de memória somente quando o atributo de **\[ \_ alocação \] de habilitação** é usado. O ambiente de gerenciamento de memória deve ser habilitado para que a memória possa ser alocada usando [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate). No modo **uso** (quando você compila usando a opção [**/OSF**](-osf.md) ), o stub habilita esse ambiente automaticamente ou sob solicitação quando o atributo de **\[ \_ alocação \] de habilitação** é usado.

O stub do lado do cliente pode ser sensível ao ambiente de gerenciamento de memória do **RPCSS** . Se um stub de cliente confidencial for executado quando o pacote **RPCSS** estiver desabilitado, os alocadores/desalocadores de usuário padrão serão chamados (por exemplo, o [ \_ usuário MIDL \_ alocar](/windows/desktop/Rpc/the-midl-user-allocate-function)o /  [ \_ usuário MIDL \_ gratuito](/windows/desktop/Rpc/the-midl-user-free-function)). Quando habilitado, o pacote **RPCSS** usa o par de alocador/desalocador do pacote. No modo padrão, o cliente é confidencial somente quando o atributo **\[ habilitar \_ alocação \]** é usado. Normalmente, o stub do lado do cliente opera no ambiente desabilitado. No modo **uso** (quando você compila usando a opção [**/OSF**](-osf.md) ), o cliente sempre é sensível ao ambiente de gerenciamento de memória do **RPCSS** e, portanto, o atributo **\[ habilitar \_ alocação \]** não afetará os stubs do cliente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[\_alocar usuário de MIDL \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[usuário de MIDL \_ \_ gratuito](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 