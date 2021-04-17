---
title: A função midl_user_free
description: A \_ função gratuita do usuário MIDL \_ deve ser fornecida por desenvolvedores de RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366624"
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

Por exemplo, o programa de exemplo RPC do Windows que exibe "Olá, mundo" implementa o **\_ usuário MIDL \_ gratuitamente** em termos da função C livre:


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> Se o pacote RpcSs estiver habilitado (por exemplo, como resultado do uso do atributo \[ [**habilitar \_ alocação**](/windows/desktop/Midl/enable-allocate) \] ), o programa do servidor deverá usar o [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) para liberar memória. Para obter mais informações, consulte [pacote de gerenciamento de memória do RPCSS](rpcss-memory-management-package.md).

 

 

 