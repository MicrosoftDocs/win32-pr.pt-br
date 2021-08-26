---
title: A função midl_user_free
description: A \_ função gratuita do usuário MIDL \_ deve ser fornecida por desenvolvedores de RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ca52635da5bedb60fdc7f94165ad9c888c030d5fe3340c53dfc970a90ff49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080816"
---
# <a name="the-midl_user_free-function"></a>A \_ função gratuita do usuário MIDL \_

A **função \_ \_ gratuita do usuário MIDL** deve ser fornecida por desenvolvedores de RPC. Ele aloca memória para os stubs RPC e rotinas de biblioteca. A **função \_ \_ gratuita do usuário MIDL** deve corresponder ao seguinte protótipo:

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

O parâmetro *pBuffer* especifica um ponteiro para a memória a ser liberada. O aplicativo cliente e o aplicativo de servidor devem implementar a função do **\_ usuário \_ MIDL** , a menos que você esteja compilando no modo uso-Compatibility ([**/OSF**](/windows/desktop/Midl/-osf)). A função de **\_ usuário \_ de MIDL** deve ser capaz de liberar todo o armazenamento alocado por [**\_ \_ alocação de usuário MIDL**](the-midl-user-allocate-function.md).

Aplicativos e stubs chamam o **\_ usuário MIDL \_ gratuito** ao lidar com objetos alocados:

-   O aplicativo de servidor deve chamar o **\_ usuário MIDL \_ gratuitamente** para liberar memória alocada pelo aplicativo, como ao excluir um nó de dados alocado dinamicamente.
-   O stub de servidor chama o **\_ usuário MIDL \_ gratuitamente** para liberar memória no servidor após o marshaling de todos os \[ \] argumentos, os \[ \] argumentos de \[ saída \] e o valor de retorno da função.

por exemplo, o programa de exemplo RPC Windows que exibe "olá, mundo" implementa o **\_ usuário midl \_ gratuitamente** em termos da função C livre:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Se o pacote RpcSs estiver habilitado (por exemplo, como resultado do uso do atributo \[ [**habilitar \_ alocação**](/windows/desktop/Midl/enable-allocate) \] ), o programa do servidor deverá usar o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) para liberar memória. Para obter mais informações, consulte [pacote de gerenciamento de memória do RPCSS](rpcss-memory-management-package.md).

 

 

 