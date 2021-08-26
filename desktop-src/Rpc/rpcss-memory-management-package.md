---
title: Pacote de gerenciamento de memória RpcSs
description: O par de alocador/desaloqueador padrão usado pelos stubs e o tempo de executar ao alocar memória em nome do aplicativo é o usuário médio alocado/usuário médio \_ \_ \_ \_ livre.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93648b56ed47eb98a83b27a39b606fa2a51de9bf5791ad1b732e7169ef5dfa63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018176"
---
# <a name="rpcss-memory-management-package"></a>Pacote de gerenciamento de memória RpcSs

O par de alocador/desaloqueador padrão usado pelos stubs e o tempo de executar ao alocar memória em nome do aplicativo é o usuário médio alocar o usuário **\_ \_** / **midl \_ \_ gratuito.** No entanto, você pode escolher o pacote RpcSs em vez do padrão usando o atributo ACF **\[ enable \_ \] allocate**. O pacote RpcSs consiste em funções RPC que começam com o **prefixo RpcSs** ou **RpcSm**. O pacote RpcSs não é recomendado para Windows aplicativos.

> [!Note]  
> O Pacote de Gerenciamento de Memória Rpcss está obsoleto. É recomendável que [**o usuário médio \_ \_ alocar e**](/windows/desktop/Midl/midl-user-allocate-1) o usuário [**midl \_ \_ gratuito**](/windows/desktop/Midl/midl-user-free-1) sejam usados em seu lugar.

 

No **modo /osf,** o pacote RpcSs é habilitado para stubs gerados por MIDL automaticamente quando ponteiros completos são usados, quando os argumentos exigem alocação de memória ou como resultado do uso do atributo **\[ enable \_ allocate. \]** No modo padrão (Estendido da Microsoft), o pacote RpcSs é habilitado somente quando o atributo **\[ enable \_ \] allocate** é usado. O **\[ atributo enable \_ allocate \]** habilita o ambiente RpcSs pelos stubs do lado do servidor. O lado do cliente é alertado para a possibilidade de que o pacote RpcSs possa ser habilitado. No **modo /osf,** o lado do cliente não é afetado.

Quando o pacote RpcSs está habilitado, a alocação de memória no lado do servidor é realizada com o alocador de gerenciamento de memória RpcSs privado e o par de alocador de desalocador. Você pode alocar memória usando o mesmo mecanismo chamando [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (ou [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)). Após o retorno do stub do servidor, toda a memória alocada pelo pacote RpcSs é liberada automaticamente. O exemplo a seguir mostra como habilitar o pacote RpcSs:

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

Seu aplicativo pode liberar explicitamente a memória invocando a [**função RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) ou [**RpcSmFree.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) Observe que essas funções não liberam memória. Eles o marcam para exclusão. A biblioteca RPC libera a memória quando o programa chama [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) ou [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

Você também pode habilitar o ambiente de gerenciamento de memória para seu aplicativo chamando a [**rotina RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (e pode desabilitá-lo chamando a [**rotina RpcSmDisableAllocate).**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) Uma vez habilitado, o código do aplicativo pode alocar e desalocar memória chamando funções do pacote RpcSs.

 

 