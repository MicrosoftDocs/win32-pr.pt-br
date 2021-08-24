---
title: enable_allocate atributo
description: O atributo \ enable allocate\ ACF especifica que o código stub do servidor deve habilitar \_ o ambiente de gerenciamento de memória de stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate atributo MIDL
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
# <a name="enable_allocate-attribute"></a>\_habilitar atributo allocate

O **\[ atributo \_ habilitar alocar \]** ACF especifica que o código stub do servidor deve habilitar o ambiente de gerenciamento de memória de stub.

> [!Note]  
> O **\[ atributo enable \_ allocate \]** está obsoleto e não tem mais suporte.

 

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

*optional-attribute-list* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos MIDL adicionais.

</dd> <dt>

*interface-name* 
</dt> <dd>

O nome da interface à qual o **\[ atributo enable \_ \] alle** será aplicado.

</dd> </dl>

## <a name="remarks"></a>Comentários

No modo padrão, o stub do servidor habilita o ambiente de memória somente quando o **\[ atributo enable \_ allocate \]** é usado. O ambiente de gerenciamento de memória deve ser habilitado antes que a memória possa ser alocada usando [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate). No **modo osf** (quando você compila usando a opção [**/osf),**](-osf.md) o stub habilita esse ambiente automaticamente ou na solicitação quando o atributo **\[ enable \_ allocate \]** é usado.

O stub do lado do cliente pode ser sensível ao ambiente de gerenciamento de memória **Rpcss.** Se um stub de cliente sensível for executado quando o pacote **Rpcss** estiver desabilitado, os alocadores/desalocadores de usuário padrão serão chamados (por [exemplo, \_ \_](/windows/desktop/Rpc/the-midl-user-allocate-function)o usuário médio alocará o usuário /  [midl \_ \_](/windows/desktop/Rpc/the-midl-user-free-function)gratuito). Quando habilitado, o **pacote Rpcss** usa o par allocator/deallocator do pacote. No modo padrão, o cliente é sensível somente quando o **\[ atributo enable \_ allocate \]** é usado. Normalmente, o stub do lado do cliente opera no ambiente desabilitado. No **modo osf** (quando você compila usando a opção [**/osf),**](-osf.md) o cliente é sempre sensível ao ambiente de gerenciamento de memória **Rpcss** e, portanto, o atributo **\[ enable \_ allocate \]** não afetará os stubs do cliente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 