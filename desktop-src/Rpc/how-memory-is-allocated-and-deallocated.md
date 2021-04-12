---
title: Como a memória é alocada e desalocada
description: Por padrão, o código stub gerado pelo compilador MIDL chama funções fornecidas pelo usuário para alocar e liberar memória. Essas funções, chamadas \_ \_ de alocação de usuário de MIDL e usuário de MIDL \_ \_ gratuito, devem ser fornecidas pelo desenvolvedor e vinculadas ao aplicativo.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c32ac4d33fbd67f617f79125921ddfffc0de5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366413"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Como a memória é alocada e desalocada

Por padrão, o código stub gerado pelo compilador MIDL chama funções fornecidas pelo usuário para alocar e liberar memória. Essas funções, chamadas [**de \_ \_ alocação de usuário de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) e usuário de [**MIDL \_ \_ gratuito**](/windows/desktop/Midl/midl-user-free-1), devem ser fornecidas pelo desenvolvedor e vinculadas ao aplicativo.

Todos os aplicativos devem fornecer implementações de [**\_ \_ alocação de usuário MIDL**](/windows/desktop/Midl/midl-user-allocate-1) e [**usuário de MIDL \_ \_ gratuito**](/windows/desktop/Midl/midl-user-free-1), mesmo que os nomes dessas funções possam não aparecer explicitamente nos stubs. A única exceção é quando você está compilando no modo uso-Compatibility (/OSF). Essas funções fornecidas pelo usuário devem corresponder a um protótipo de função definido específico, mas, caso contrário, podem ser implementadas de qualquer forma que seja conveniente ou útil para o aplicativo. Como alternativa, os aplicativos podem usar o pacote de gerenciamento de memória do RpcSs. A biblioteca de tempo de execução RPC da Microsoft fornece esse grupo de funções.

As seções a seguir descrevem as funções de gerenciamento de memória RPC.

-   [**\_alocar usuário de MIDL \_**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**usuário de MIDL \_ \_ gratuito**](/windows/desktop/Midl/midl-user-free-1)
-   [Pacote de gerenciamento de memória de RpcSs](rpcss-memory-management-package.md)

 

 