---
title: Pacote de gerenciamento de memória de RpcSs
description: O par de alocador/desalocador padrão usado pelos stubs e o tempo de execução ao alocar memória em nome do aplicativo é o usuário de MIDL \_ \_ alocar/MIDL \_ user \_ Free.
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454260"
---
# <a name="rpcss-memory-management-package"></a>Pacote de gerenciamento de memória de RpcSs

O par de alocador/desalocador padrão usado pelos stubs e tempo de execução ao alocar memória em nome do aplicativo é **MIDL \_ usuário \_ alocar** / **usuário de MIDL \_ \_ gratuito**. No entanto, você pode escolher o pacote RpcSs em vez do padrão usando o atributo ACF **\[ habilitar \_ alocação \]**. O pacote RpcSs consiste em funções RPC que começam com o prefixo **RPCSS** ou **RPCSS**. O pacote RpcSs não é recomendado para aplicativos do Windows.

> [!Note]  
> O pacote de gerenciamento de memória do RPCSS está obsoleto. É recomendável que [**o \_ usuário \_ de MIDL aloque**](/windows/desktop/Midl/midl-user-allocate-1) e o [**usuário de MIDL \_ \_ livre**](/windows/desktop/Midl/midl-user-free-1) sejam usados em seu lugar.

 

No modo **/OSF** , o pacote RPCSS é habilitado para stubs gerados por MIDL automaticamente quando são usados ponteiros completos, quando os argumentos exigem alocação de memória ou como resultado do uso do atributo **\[ Enable \_ ALLOCATE \]** . No modo padrão (Microsoft Extended), o pacote RpcSs é habilitado somente quando o atributo **\[ habilitar \_ alocação \]** é usado. O atributo **\[ habilitar \_ alocação \]** habilita o ambiente RPCSS pelos stubs do lado do servidor. O lado do cliente se torna alertado sobre a possibilidade de habilitar o pacote RpcSs. No modo **/OSF** , o lado do cliente não é afetado.

Quando o pacote RpcSs está habilitado, a alocação de memória no lado do servidor é realizada com o par do alocador de gerenciamento de memória e desalocação de RpcS particulares. Você pode alocar memória usando o mesmo mecanismo chamando [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (ou [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)). Após o retorno do stub do servidor, toda a memória alocada pelo pacote RpcSs é liberada automaticamente. O exemplo a seguir mostra como habilitar o pacote RpcSs:

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

O aplicativo pode liberar memória explicitamente invocando a função [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) ou [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) . Observe que essas funções não liberam realmente a memória. Eles o marcam para exclusão. A Biblioteca RPC libera a memória quando o programa chama [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) ou [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).

Você também pode habilitar o ambiente de gerenciamento de memória para seu aplicativo chamando a rotina [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) (e você pode desabilitá-lo chamando a rotina [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) ). Uma vez habilitado, o código do aplicativo pode alocar e desalocar memória chamando funções do pacote RpcSs.

 

 